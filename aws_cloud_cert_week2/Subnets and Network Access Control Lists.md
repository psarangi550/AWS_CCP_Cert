# <ins> Subnets and Network Access Control Lists in AWS VPC </ins> #

- The `Virtual Private Cloud or VPC` is a `harden fortess where nothing can go in and out unless explicit permission`

- with the  help of `Internet Gateway` Doorway `we can allow public internet traffic` into the `VPC`

- But this `only cover the permimeter` which should be considered while considering the `One of the Network Security Aspect` While discussing the `IT Startergy`

- But there are again multiple `AWS Tools` available for `Network Security layer from various aspect`

    - `Network Hardening`

    - `Application Security`

    - `User Identification`

    - `Authentication and Authorization`

    - `Distibuted Denial of Service Prevension or DDoS prevension`

    - `Data Integrity`

    - `encryption`


- we can use these tools to `lock our infrastructure With Tighter Security`

# <ins> Various Aspect of Network Hardening </ins> #

- When we use the `AWS VPC` we divide the `AWS resources` into multiple `Subnet` which will help in define the `Gateway whether to Access the AWS Resources publicaly by using the internet gateway` or `Not providing Access to the AWS Resources by keep it in private subnet and not providing Internet Gateway`

- But `Subnet` can also help in `incoming traffic permission` which can interact with the `AWS Resources` 

- Over the `internet` the `messages were coming as packets`

- `Every Packets` that crosses the `Subnet Boundary` will be checked for the `traffic permission` by the `Network Access control List or Network ACL or NACL`

 - the subnet allow that `packets traffic into the subnet where the AWS Resources are available` based on the ` whether the packet has the permission to enter to to the Subnet and Leave the Subnet or Not based on Who Send the Request and How that packet want to communicate` using the `Network Access Control List` known as `Network ACL or NACL`

- This `incoming packet traffic` will be verified at the `subnet permiter / boundary ` by the `Network ACL` which only allow the `Approved Traffic Permission based on the packet permission to go in out of the subnet boundary` disapproving the `traffic which are not on the List or explicitly denied`

- This Particular check will happen at the `Subnet boundary` by the `Network ACL` while the `packets going in and out at the subnet boundary`

- the  `harmful traffic` will be `prevented` before it can reach to the `Subnet` such as `Request to gain Administrative permission for the AWS Resouce inside the subnet` which can helpful in `preventing the hacks` , if we can' touch the we can't hack 

- this is similar to have a `Passport Officer` which will check the `Available List of Passenager which have the  Approved Passport` , if `Having a Valid Approved Passport` then `Network ACL` will allow the `traffic packet` into the `subnet in order to interact with the AWS Resources` else `discard it`

- if a `traffic request` came in that does not mean `it will only checked while going in and not checked while getting out` but the `traffic will be checked in while going into the subnet where the resource reside and also while coming out`

- if a `traffic have both permission to go in and out` then this will allow it else it will `not allow the traffic to go out even`

- similarly `When the Passport Will be checked in while going into the VCountry and coming out of the Country` similarly the `incoming traffic packet` will be checked in `both the in and out at the subnet boundary`

- but the `Network ACL or passport officer` will check the `traffic of the packet` while covering the `Subnet Perimeter` not checking `whether the Traffic packets` reaching to the `AWS resources inside the subnet which is inside the VPC`

- This seems Like a `Great Security Feature` but however there are few unanswered question as well 

- `Network ACL` only check the `incoming packet at the subnet boundary while in out` but does not check whether those `approved packets reaching tto the Permitted AWS Resource or not`

- In order to `check whether the Traffic packets` approved by the `Network ACL` coming to the `Subnet reaching the particular AWS Reosucres or not`

- Here we need to validate `There can be multiple AWS Resources present inside the Same subnet such as Multiple EC2 instances inside the subnet of the AWS VPC`

- the `traffic packet` which passes the `Network ACL` need to `go to specific EC2 Instance based on the host and Ports thats are allowed based on Securithy group Rules ` then in that case we need to take care of the `instance label Network Security and Network Access control`

- to answer the `instance label Network Security and Network Access Control ` we need the `Security Group` which will be associated with the `specific EC2 instances`

- in that we need to use the `Security Group` which been associated with each `EC2 instances` and allow `traffic onto the specific EC2 instances` based on the `Security Group` permission which allow `specific type of request on specific port of the EC2 instances and who can send request or to which port the request can be sent to and what type of traffic allowed on the AWS resource i.e EC2 instance`


- By default while creating the `EC2 instance ` A `Security Group` is associated with it but `which will allow no connection traffic ` which is ok from the `security aspect but will not be very helpful from the user interaction from internet traffic`

- But we can `manipulate the Security Group` that allow traffic `dedicated host and port to the particular EC2 instance building` which can accept `specific type of incoming traffic on specific port`

- if the `EC2 instance` expect the `EC2 hosting a web browser` then we can sent `frontend http request or web request to the specific port` but will not allow the `OS/Admin` level request 

- if the `Network ACL` is the `passport office which check the passport on in and out` then `Security Group` is the `Secrity Group is a building security` which check the `incoming traffic allowed host and port` and if the `host and ports and request type` are allowed then it will allow the `traffic to iunteract with building or EC2 instances` but will not check `While traffic or request been going out`

- the `security group` will allow only `approved traffic by the instance and allow all traffic to go out from the instance of the subnet`

- there are 2 different kinds of `tools for Network Security one from subnet perimeter which is Network ACL and other from the instance label which is of Security Group`


# <ins> Dfiiference Between the Network ACL and Security Groups </ins> #

|Security Group               |      Network ACL              |
|-----------------------------|-------------------------------|
| Security Group is Stateful i.e when a incoming traffic comes in then it will check the `Approved traffic from the Security Group` from its memory in order to allow it                             | But where as the Network ACL is stateless which will not remember the `incoming Traffic at the subnet boundary in and out` and always checks for permission each time the `request came in`  |      


# <ins> Understanding Stateless and Stateful Nature of Network ACL and Security Groups using the Round Trip Of packets in Same VPC but in different SubNets </ins>

- Lets suppose we have 2 different `EC2` instances which reside in 2 different `Subnet` inside the `Same AWS VPC`

- Here one `EC2` instances send `packets traffic` from `one instances to another instances` which reside in `different subnet under Same VPC`

- the `traffic management` for this `packet transfer` will not open the `content of the packet` rather it don't have the `access to open the packet` but check whether `packet` has the `packet sender name listed in the Permitted Access List`

- in this case the `When the packet` leaves the `EC2 instances` then it need to `get through the Security Group of the EC2 Instance which is for Instance Network Security` , By default the `Security Gateway` allow all the `outbound traffic` hence the `packet` can `leave` the `EC2 instances`

- once the `packet leaves the EC2 instance security Group` then it reaches to the `NetWork ACL of the same subnet of the AWS Resource i.e EC2 instance that in` then the `NetWork ACL of of the Same Subnet` check whether the `packet sender has the name in the Access List to leave the subnet or not and Target Subnet is in the List or not` , if it has the permission then it will allow the same 

- if the `packet sender name and Traget subnet is on the List of the Sender Network ACL` does not meand that should be present in the `Destination Network ACL List` , it will be checked in both the `Source and Destination Network ACL` in order to be `allowed`

- The the packet has to go through the `NetWork ACL of the other subnet it want to reach to` as the `Network ACL are stateless in nature` then again the `packet` get checked whether they are `permitted to the destination subnet or not by checking the approved List` if the Name is in the `packer sender Name in Approved List` then it will be allowed else it will be blocked

- Every `EC2 instance ` has their `separate Security Group for Network Security`

- Once the `packet` through the `Network ACL` of the `destination subnet` then it will met with the `Security group of the Destination AWS Resource or AWS EC2 instance` then the `Security group check the packet traffic from its list` if the name already on the List then allow it 

- Even if the `packet been through the Network ACL` that does not means it will through the `Security Group of the AWS Resource` and vice versa

- It need to go through both the `Security check with the Network ACL and Security Group Engine`

- The `returning journey of the Packet` by using the `return traffic pattern` where we can see the `stateful and stateless nature of Network ACL and Security Group`

- When the `packet returned from the destination subnet` as the `EC2 instance Security Group allow all the outbound traffic packet can come out of the Destination AWS Resource`

- But when it reaches again to the `Destination Subnet` then as the `Network ACL at that subnet boundary` is `stateless in nature` it will validate the `packet been permitted to leave or not from the subnet boundary using the Approved List which check the ingress and egress rules on the Approved List of Packet Entry` if you are on the `You are not Leave List` then it will not allow to return it

- The again the `packet` has to `face the Network ACL of the Source Subnet` as the `Network ACL is stateless` and `check been happening for the ingress and egress List of Approved Packet` if the `packet name in the approved List` it will allow the connection

- Then packet go to the `Security Group of the Source EC2 Instance or AWS Resource` as the `Security Group are stateful that it saves the Approved List of Packets into its memory unlike the Network ACL hence it recognizes the packet` hence the packet been allowed to the `EC2 Instance back again`

- if you are thinking `those many number of check additional Network Overhead` then all those operation `traffic management` happens with in a `fraction of seconds instantly`

- `Good Network Security` Take help of both the `Network ACL and Security Group` for `traffic management`






