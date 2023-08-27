# <ins> Moving Parts inside AWS Region</ins> #


- `Availablity Zone` :- 

    - A `Region` is a `geographical area that contains AWS resources.`


    - `AWS` has `multiple data center` which construct a `AWS region` across all the `all part of world`

    - `All of the data or application should load ` with in the `AWS Region` that we have selected

    - But that does not mean all the `data load and run application` should run over `single building` where the `failure is unavoidable` for `number of reason`

    - if we want to make the `application` inside the `AWS region` to be `disaster proof` then we need  `not to run all the application inside a single building`

    - `AWS regions` are not a `single location building`

    - `AWS` called the `single datacenter or group of data center` as the `availablity zone or AZ`

    - An `AWS Availability zone i.e AZ` is a `one or more discrete datacenter` with `redundant power, Networking and connectivity `

    - `An Availability Zone `is a `single data center or a group of data centers within a Region`

    - When we launch an `EC2 instance` it will launch a `Virtual Machine on the physical server hardware installed on one of the Availability Zone or AZ Data center`

    - hence we can say that `Each AWS Region` consist of `one or more AZ or availabilty zone which are isolated and physically separated ` within the `geographic region`

    - But the `Availabity Zone or AZ` are `not right next to each other `, because `if a large scale disaster happend` then we can loose all the `data and application and connectivity` available on that specific `Availability Zone`  will be lost

    -  `Availability Zones` are `located tens of miles apart from each other.` This is `close enough to have low latency (the time between when content requested and received) between Availability Zones`.

    - However, if a disaster occurs in one part of the Region, they are distant enough to reduce the chance that multiple Availability Zones are affected.

    - we need to plan the `Availabilty Zone` as per the `disaster recovery planning`

    - if we are running one `EC2 instances` then that will be runninng the `virtual machine over the hardware thats been present in a single availabiltry zone`, hence its recomended to `run the multiple EC2 instances` accross `multiple availablity zone or AZ within AWS region` in case of `large scale disaster`

    - with the `speed of light` is the way we can `still separate the Availabilty Zone far away from each other` with `single digit low latency i.e time to send and receive data `

    - when thee `low latency` will increase the `speed of light tell you to stop and not to move further to avoid the low latency`

    - hence with the `single digit low latency` the `AZ or availabilty zone` can be `10 of miles away with just single digit low latency`

    - As the `Availabity Zones` are Far from each other `in case a disaster happend ` our entitre application will not be `shut down` only the part of the `application can face capacity down for some of the application` we can also spin more `capacity of the application by scaling the rest of the Availabilty Zone `

    - `AWS` always recomend to run accross `2 availability Zone of the Same region to be fail proof` while spinning the `EC2 instnces`

    - We need to deploy our `application` accross the `2 different Availabilty Zone inside the Same AWS Region` to make it as `disaster proof`


-  `Many of the AWS Services` are `regional construct` which can run accross `all the Availability Zone` of the `AWS region` such as `AWS ELB Service`

- `Regional construct AWS Servies` `run synchronously` accross all the `Availabilty Zone Or AZ` without we put any `additional effort`

- `ELB Service` is a `AWS regional construct` which runs on `multiple AWS availabilty zone synchronously` for all the `communicating to All EC2 instances running on multiple availabity zone for your application`

- hence `regional construct service` such as  `AWS ELB Services` are highly avialble as they are `running synchronously` over the `multiple AZs`

- when we plan for the `AWS Service` which are `Regional construct` then we havbe these `high availabilty box checked for that`


# <ins> Running Amazon EC2 instances in multiple Availability Zones </ins> #

- **Amazon EC2 instance in a single Availability Zone** :-

    - Suppose that you’re running an application on a single Amazon EC2 instance in the Northern California Region. The instance is running in the us-west-1a Availability Zone. 
    
    - `If us-west-1a were to fail, you would lose your instance.`

- **Amazon EC2 instances in multiple Availability Zones** :- 

    - A best practice is to run applications across at least two Availability Zones in a Region. In this example, you might choose to run a second Amazon EC2 instance in `us-west-1b.`

    - f `us-west-1a` were to fail, your application would still be running in` us-west-1b.`


# NOTE:-

- A` data center` that an `AWS service uses to perform service-specific operations `which is known as `Edge`

- `AWS Outposts` is a `service` that you can `use to run AWS infrastructure, services, and tools in your own on-premises data center in a hybrid approach`.