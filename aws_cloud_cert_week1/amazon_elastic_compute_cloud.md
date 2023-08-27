# <ins> Amazon EC2 </ins> #

- the  `Amazon EC2` known as the `Amazon Elastic compute cloud`

- We can deliver the `product /data /  resources` using the `vclient server model` using the `raw computing ` to the `enduser`

- We need the `server` to power up the `Business or Application ` where we need the `raw compute capacity for the server which provide raw compute speed to hosted application`

- when woprking with the `AWS` those `server are virtual` in nature 

- the `server we use to gain the access` to the `virtual server` is called as `EC2` 

- using `EC2` for `compute` will be off 

    - `highly flexible `
    - `cost effective `
    - `quick` 

    - compared to the ` physical server` deployed `on premises` on the `data center`

    - the `time and money` it took to `up and run` with `on premises resources i.e datacenter with physical server` is very high as compare to the `EC2` server which handle the `virtual server`

    - when we are using our `own fleet of physical server on the data center` then we need to think about `multiple` things

        - what type of server we want 

        - How many server that we want 

        - we need to purchase thar upfront 

        - we need to wait `multiple weeks or days` for the `vendor` to `deliver` them

        - then we need to take them to the `data center we own` and then install and  `rack and stack and wire them` 

        - we need to make sure `they are secured and powered up` and the we can be able to use the `own physical server onthe data center` can be used for computing

        - then we can `host the application onto those powered up server`

        - once we by the `physical server` we are stuck with them whether to use them or not 

    - with the `EC2` it will more simpler with below point

        - `AWS` `built and secured `the `datacenter` already 

        - `AWS` already bought the sever that we need on top of the `data center` and get them `racked and stacked and wired` and even make it `powered on`

        - these server as well `online and ready to be used` to be `hosting the application` into it 

        - `AWS` constantly operating a the `massive amount of compute capacity` , we can use the `whatever portion of the capacity when we need it`

        - we can request for the `EC2 instance with specific capacity` that we want and `they can be launch and boot up and ready to be used within minutes`

        - once done we can able to `stop and terminate the EC2 instances`

        - here we are not `stucked in with the server that we don't need or want` unline `physical server on premises data center`

        - the `usage of the EC2 instances` can vary over time but we only need to `pay for what we use` in case of `AWS EC2 instance`

        - we need to only pay for the `running instances` not for the `stopped or terminated instances`

        - `EC2` runs on top of the `physical host machine that are managed by AWS` using the `virtualization technology`


- when we spin a `EC2 instance` we are not taking the `entire host to yourself` we are sharing the `host` with `with multiple other instances` which is `known as virtual machine`

- these `virtual machine` being managed by the `hypervisor` which is running on the `physical host machine that are managed by AWS` and also share the `resources for the underlying virtual machines i.e host that can be shared with multiple instances of EC2`

- `the ideas of sharing the resources between the virtual machine from the host machine ius known as multitenancy`

- the `hypervisor running on the host machine managed by AWS ` is responsible of `multitenancy`

- `Hypervisor` segregate the `virtual machine which been sharing the resource` from one another accross multiple instance 

- `EC2 instances` are secure even though they are sharing resources from the same Hypervisor which is `secure in nature`

- One `EC2 instance` will not be aware about the `Another EC2 Instance` even though they shared the `physical resources` from the same host `managed by hypervisor`

- we can `create the New instances and take them off at will` but we can also `provide individual instance configuration for the same as well`

- we can choose the `operating system` while `selecting each individual EC2 instances` whether `Windows or Linux`

- we can spin thousand of `instances` from the `with differen t operating system` for `different application in the business`

- we can also choose what type of software we want to run using the `EC2 instances`

    - internal business application 

    - simple web app / complex web app

    - databases

    - third party software

    - Enterprise software packages 


- `EC2 instances` are resizeable in nature `we can start with the small capcity instances and later we can provide more CPU and Memory to the instances`

- this particular process of upgrading the `CPU and Memory` is known as `vertical scaling of application`

- we can make out instance `bigger or smaller ` based on the `requirement that we have`

- we can also control the `networking aspect of EC2` instance as well 

    - what `type` of `request` will make to the `server`

    - whatever server `publicly accessible ot privately accessable` that can be decided by us only 

    - `virtual machine` is not a `new concept` but with the help of `AWS EC2` that became much easier ansd much cost effective 

    - here using the `EC2` we can get the `server` using the `compute as a service model CaaS`





