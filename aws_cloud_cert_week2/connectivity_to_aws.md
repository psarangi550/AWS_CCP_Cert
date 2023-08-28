# <ins> Connectivity to AWS </ins> #

- A `VPC or virtual private cloud` is `essentially your OWN private network` inside the `AWS cloud`

- we can define the `private IP ranges` for the `AWS Resources` inside the `AWS VPC which is a pivate Network` , we can put like `AWS Reosurces such as AWS EC2 instances and AWS ELB inside the AWS Virtual Private cloud` # range of IP can assign to AWS Resources inside the AWS VPC

- we can't simply throw the `AWS resources into the AWS VPC which is a virtual private network` and then `move on` , but rather we need to put `AwS resources` inside `different subnets` # we need to divide the AWS Resources inside the VPC into multiple subnets

- `subnet` are the `chunk of IP address inside the VPC` that allow us to `group the AWS resource together inside the VPC` # grouping AWS Resources

- `subnet along with networking rules` control `whether the AWS resources are publicly available or privately available` #manage resource whehter public or private

- we can also control `what traffic will get the access to the VPC at all`, for `some VPC` we want the `internet facing AWS resources` that the `public` can be to use or reach to those resources from `outside` such as `public website as AWS respurces inside the VPC`

- However in `other scenarios` we don't want to `provide access to the AWS resources` iff the `user been logged into the private network` suchas `internal sevices such as HR application or Backend Database`

- **Accessing Public Facing AWS Resources inside VPC**

    - if we want to `allow the public request or traffic from outside internet` to the `publicly facing AWS resources` into and out of the `VPC which is a Virtual Private Network` then we need to `set the Internet Gateway For the Same` which is known as `IGW` inside the `Your VPC `

    - the `Internet Gateway or IGW` is a `doorway` to the `public internet` which allow `anyone from anywhere to access the AWS Resources from the VPC`

    - think about the `coffee shop` we can't enter to the `coffee shop` without the `front door available` , then people can `go in and out of the coffee shop` using that `door way`

    - `the front door of the coffee shop` is just like the `internet gatway doorway` without that `no one reach to the VPC as it is virtual private Network`

- **Accessing Private AWS Resources inside VPC**

    - we don't want `anyone from anywhere` to reach to the `AWS Resources` inside the `VPC i.e virtual Private Network`

    - here in this case we don't want a `Internet Gateway` attached to the `VPC` which allow the `public internet to the virtual private Network or VPC`

    - instad we need a `Private Gateway` associated to the `AWS VPC` which allow only those `user which been coming from Approved Network` not from the `Public internet`

    - this `Private gateway doorway` is known as the `Virtual Private Gateway` which been associated with the `AWS VPC` in order to restrict the `public internet` and allow only `user from approved Network` to access the `AWS Resource inside the AWS  VPC`

    - this allow us to create a `VPN connection` between the ` private network of the on premises data center  and the AWS VPC` or `internal corporate network and your VPC`

    - this is simlar to the analogy as 

        - Lets Support there is a `private bus route` going from `my building` to the `coffee shop`

        - if we want to get to the `coffee shop` from the `building` then we first need to `access the badge and enter the correct credetional to authenticate` in order to access the `secret private bus` which been leading to the `coffee shop` which is available to `my building member only to use`



    - if we want to `eastabilished an encrypted VPN connection` to the `internal AWS Resource inside the VPC` so that only `authenticated user with Approved Network can use this` then we need to associate a `Virtual Private Gateway` to the `AWS VPC`

    - if we want to provide a `encrypted VPN connection` to the `AWS resources inside the AWS VPC` so that `authenticated and Approved User can access` the `AWS resources` then we need to use the `Virtual Private Gateway` associated to the `AWS VPC`



    - Lets come back to the `coffee shop` examples with the `secret bus route`

        - But the `problem` now is `even though its secret` but it uses the `open public road` to get to the `coffee shop` which can caught in the `traffic Jam or slowed down` based on the `normal public traffic`

        - The same can also happen to the `VPN connection` ,

            - Even though the `VPN connection` using the `Virtual Private Gateway` is 

                - `encrypted `

                - `privately connected` to the `private network of on premises DC or internal corporate Neteork`

            - But `VPN connection` still using the `same public internet` which being used by the `regular public internet` which can `slow down the traffic` based on `bandwidth` used by oother user



    - Lets come back to the `coffe shop` example again

        -  if we don't want to caught up in the `traffic` then we can introduce a `magic door` which can `directly access the coffee from the coffee shop to the my building room`

        - similarly `AWS Direct Connect Service` can provide `private dedicated fibre connection shared by No-One else  between the Virtual Private Gateway and on-premises Data-center or Internal corporate Network ` directly  which can go in `without worrying about the bandwidth of public internet`

        - we need to work with the `AWS Direct connect Partner` to `established the connection` from the `internal corporate network or on-premises data center to AWS VOC using Virtual Private Gateway`

        - `AWS Direct connect` priovide the `Directr physical dedicted fibre connection` between `internal corporate network or on-premises data center to AWS VOC using Virtual Private Gateway`

        - here in this case we are considering the `high speed and High Privacy or encryption` in order for the `communication` which is `more reliable and less susecptable to slow down`

        - here we want the `lowest amount of latency and highest amount of secrity and shared by no one else rather than authenticated user in encrypted way` while considering connecting a `private network of internal corporate network or on premises Data center to the AWS VPC using the virtual Private Gateway`

        - this will help in `getting high regulotory compliance need by your company/ business` with `less potential bandwidth issue`


- One `VPC` can have `multiple type of Gateway Attached` lets suppose one 

    - `Internet Gateway`

    - `Virtual Private Gateway`

    for different `AWS resources` in the `AWS VPC` , but the `subnet` for those resource will be also `different` but residing inside the same `AWS VPC`

- 






