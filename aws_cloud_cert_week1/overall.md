# <ins> Overall Of Week1 </ins> #

- `cloud comuting` :- It is the `On demand Delivery of It Resources over internet with pay as you go pricing `

- we can request for `IT resources` such as 

    - `compute`

    - `Networking`

    - `Storage` 

    - `analytics`

    - `other`

- these type of `IT resources` are made available `on demand` based on the `request`

- we don't have to pay for the `upfront` we can ask for the `provision` and `pay the end of the month`

- `AWS` provide services in many category to `create a solution`

- using the `Amazon EC2 Service` we can `spin up and spin down EC2 instance which is otherwise known as EC2 instances `

- when we choose the `EC2 instance` we need to select the `instance family` which decide the `hardware configuration of EC2 instance run on`

    - `General Purpose`

    - `compute optimized`

    - `Memory Optimized`

    - `Accelarate computing`

    - `storage optimized`

- we can resize the `EC2 instances` vertically by `increasing the Storage and hardware` also we can `horizontally scale` using `EC2 Autoscaling service option` by add ing `new instances` to the `pool or fleet`

- `Amazon EC2 Auto Scaling service` help in `horizontally scale`  option 

- in order to `distribute the incoming traffic into those horizonally scaled Application` we can use the `ELB i.e Elastic Load Balacing`

- `EC2 instances` have `different pricing models`

    - `on-demand` :- this is `much flexible nand need no contract`

    - `spot instances` :- `which allow us to use the unused capacity with a discounted price`

    - `savings plan` :- `need to get into a contact for 1 or 3 years which provide discounted rate for certain usage of instance`, Here we can apply for `AWS Lambda` and `AWS Fargate` which are `serverless compute` as well as for `AWS EC2 instances`

    - `reserved instances` :- `need to get into a contact for 1 or 3 years which provide discounted rate for certain usage of instance`


- there are also `Messaging service` provided by `AWS` which are of 

    - `Amazon Simple Queue Service (SQS)` :- which help in `decouple the sysyem components` , `Messages will be there in the Queue untill processed/consumed or deleted`

    - `Amazon Simple Notification Service (SNS)`:- which help in `sending Messages in term of the email notification, text message, push notification, even http request`, Once the `Messages published it will sent to all the subscriber of that topic`

    - It does not use the message subscription and topic model that is involved with Amazon SNS.


- `AWS` have different type of `compute service` beyond the `virtual server` like `EC2 Service`

    - AWS container Service

        - `Amazon Elastic container Service (ECS)`

        - `Amazon Elastic Kubernetes Service (EKS)`

    - both of them are `container orchestration tool` which help in manage `multiple container ccross miultiple instances`

    - we can use the `ECS and EKS` ontop of the `EC2 instances` which is optional if we want we can use else we can use the service such as `AWS Fargate`

    - in case of `AWS Fargate` the `underlying architecture` will be managed by `AWS itself` we don't have the access to `see and access the underlying OS`

    - `AWS Lambda Serverlesss compute` on to which we can `upload the code as lambda function and create & confiugure a trigger based on event source`

    - When we are using the `AWS lambda` when the `code is actually running` not for `virtual server or container maintainance` which being handled by `AWS itself` 








