# <ins> Subnets and Network Access Control Lists </ins> #

- To learn more about the role of subnets within a VPC, review the following example from the coffee shop.

    - First, `customers give their orders to the cashier`. The` cashier then passes the orders to the barista`. This `process allows the line to keep running smoothly` as more customers come in. 

    - Suppose that `some customers try to skip the cashier line` and give their `orders directly to the barista`. This `disrupts the flow of traffic and results in customers accessing a part of the coffee shop that is restricted to them`.

    - `To fix this`, the `owners` of the `coffee shop` divide `the counter area by placing the cashier and the barista in separate workstations.`

    - The `cashier’s workstation is public facing `and `designed to receive customers.` The `barista’s area is private`

    - The `barista can still receive orders from the cashier but not directly from customers.`

- This is similar to how `you can use AWS networking services to isolate resources` and determine exactly how `network traffic flows into that resource.`

- In the coffee shop, 
    
    - `you can think of the counter area as a VPC`

    - `The counter area divides into two separate areas for the cashier’s workstation and the barista’s workstation` which can be considered as `subnet`
    
    - ` In a VPC, subnets are separate areas that are used to group together resources.`

# <ins> What is Subnets in AWS VPC </ins> #

- A subnet is a `section of a VPC in which you can group resources based on`

    - `security need`

    - `operational need`

- Subnets can be 
    
    - `public or private` 

    - `Public subnets contain resources that need to be accessible by the public`, such as an online store’s website.

    - `Private subnets contain resources that should be accessible only through your private network` such as a database that contains customers’ personal information and order histories. 

    - `In a VPC, subnets can communicate with each other.` 
    
    - For example, `you might have an application that involves Amazon EC2 instances in a public subnet communicating with databases that are located in a private subnet.`


# <ins> Network Traffic in a VPC </ins> #

- When a `customer requests data from an application hosted in the AWS Cloud` , this r`equest is sent as a packet.`

- A `packet` is a `unit of data sent over the internet or a network.` 

- `It (packet) enters into a VPC through an internet gateway`

-  `Before a packet can enter into a subnet or exit from a subnet, it checks for packet permissions`

- `These permissions indicate` 
    
    - who sent the packet 
    
    -  how the packet is trying to communicate with the resources in a subnet.

- The `VPC component that checks packet permissions for subnets` is a `network access control list (ACL)` , hence the `Network ACL is a VPC Component present at the subnet boundary`

# <ins> Network Access Control Lists (ACLs) </ins> #

- A `network access control list (ACL)` is a `virtual firewall` that `controls inbound and outbound traffic` `at the subnet level.`

- For example, step outside of the coffee shop and imagine that you are in an airport. In the airport, travelers are trying to enter into a different country. You can think of the travelers as packets and the passport control officer as a network ACL. The passport control officer checks travelers’ credentials when they are both entering and exiting out of the country. If a traveler is on an approved list, they are able to get through. However, if they are not on the approved list or are explicitly on a list of banned travelers, they cannot come in.

- `Each AWS account includes a default network ACL`

-  `When configuring your VPC, you can use your account’s default network ACL or create custom network ACLs. `

- By default, your account’s `default network ACL allows all inbound and outbound traffic`, but you `can modify it by adding your own rules`

- For `custom network ACLs, all inbound and outbound traffic is denied` until `you add rules to specify which traffic to allow.`

- Additionally, `all network ACLs have an explicit deny rule. `

- `rule ensures that if a packet doesn’t match any of the other rules on the list, the packet is denied. `

# <ins> Stateless packet Filtering </ins> #

- `Network ACLs perform stateless packet filtering.` 

- They `remember nothing and check packets that cross the subnet border each way: inbound and outbound. `

- Recall the `previous example of a traveler who wants to enter into a different country`. This is similar to` sending a request out from an Amazon EC2 instance and to the internet`.When a `packet response` for that `request` `comes back to the subnet,` the `network ACL does not remember your previous request`. The network ACL checks the `packet response against its list of rules to determine whether to allow or deny.`

- After a `packet has entered a subnet`, it must have its `permissions evaluated for resources within the subnet,` such as `Amazon EC2 instances. `

- `The VPC component that checks packet permissions for an Amazon EC2 instance is a  security group.`


# <ins> Security Groups </ins>

- A `security group is a virtual firewall` that controls `inbound and outbound traffic for an Amazon EC2 instance.`

- `By default, a security group "denies" all inbound traffic and allows all outbound traffic.`

- `You can add custom rules to configure which traffic to allow or deny.`

- For this example, suppose that you are in an apartment building with a door attendant who greets guests in the lobby. You can `think of the guests as packets `and the `door attendant as a security group`

-  As guests arrive, the door attendant checks a list to ensure they can enter the building. However, the door attendant does not check the list again when guests are exiting the building

- If you have `multiple Amazon EC2 instances within a subnet`, you can `associate them with the same security group or use different security groups for each instance. `


# <ins> Stateful packet Filtering </ins> #

- `Security groups perform stateful packet filtering`. They remember `previous decisions made for incoming packets.`

- Consider the same example of sending a request out from an Amazon EC2 instance to the internet. 

- When a `packet response for that request returns` to the `instance`, the `security group remembers your previous request`. 

- `The security group allows the response to proceed, regardless of "inbound security group rules". `




- Both `network ACLs and security groups` `enable` you to `configure custom rules for the traffic in your VPC`

- As you continue to learn more about `AWS security and networking,` make sure to understand the differences `between network ACLs and security groups.`