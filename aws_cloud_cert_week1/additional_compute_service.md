# <ins> Additinal Compute Machine </ins> #

- `EC2 instance` are nothing but the `virtual machine or virtual servers running on cloud` , hence `we can configure with minimum configuration` to make it as `up and running` on `AWS`

-  If you have applications that you want to run in Amazon EC2, you must do the following:

    - `Provision instances (virtual servers).`

    - `Upload your code.`

    - `Continue to manage the instances while your application is running.`


- we can use the `EC2` instance to make it as 

    - `Running basic web server`

    - Running `High performance computing cluster (HPC)`

- `EC2` instances are 

    - `Flexiable`

    - `Relieable`

    - `Scalable`

    - But we need to `Setup` and `Manage` the `fleet of instances` `over time `

-  when using the `EC2 instnces` we need to take care of 
    
    - `patching the instances when the application been deployed or software package been comes out`

    - we also need to setup the `scaling option` while choosing the `scaling group` option

    - we also have to `ensuring the articture are loosely coupled for the solution that been deployed to the EC2 instances`


- Even though this is very less compared to the `traditional on premises data center with physical server` but it can be considerate

- we have other computing options as well apert from `EC2 instance` as well where the `management of the compute can be done by AWS`

- for the `multiple serverless compute` where we don't need to know the `details about the underlying OS` then in that case we can use the `AWS Lambda serverless compute is one of the compute option from the multiple serverless compute option`

- in this case the `underlying infrastructure will be managed by AWS which is flexible , reliable and highly scalable` can do `provisioning and maintaince`

- in case of the `serverless compute` we do need to `put the code onto the lambda function`  and create and configure a `trigger`

- then these `trigger` can initiate the `service  ready to be run when trigger happened ` that will run the `code on underlying infrastucture`

- when `trigger` is detected then these services will be run `which will run the code on infrastruicture managed by AWS which is reliable and highly scalable`


- if we have `multiple nincoming triggers` and `multiple services` to be run then it can `create multiple lambda infrastructure handled BY AWS where the code can run on those infrastructure`

- but this will be suitable for `short running services` as the whole task should be completed in `15 mins`

- if we make the `web server response for a request` or ` backend expense Report calculation` which can completed in `15 min` then thse will be helpful

- for the `short running task` this process will be very helpful which is of `Quick timing`

- it can'r support the `long running process` such as `deep learning`

# <ins> AWS container Service </ins> #

- but if we want to access to the `underlying OS` and `efficiency` and `portablity` of the `compute` then we can go for `AWS compute service`

- `AWS container service` were divided into 2 parts 

    - `Amazon Elastic Container Service`

    - `Amazon Elastic Kubernetes Service`

- both of these `service` are `container` oracherstration tool 

- here we are using container service as `docker container` which will be using the `virtualization on the OS level` on which `software can be packaged`

- we can package the `software , dependency and configuration` needed for the `sodtware package to run`

- these container will run on top of the `EC2 instances` and `run on isolation from each other` same as the `virtual machine`

- we need to monitor the ` multiple container running on multiple EC2 instances (which is known as cluster)` for which we need the `container orchestration tool`

- for the `Aws Container Service` the `software packaged Docker container` and run on top of the `EC2 instance` which can act as a `host for the contaioner` and the `container should share the hardware resources with them`

- we can `multiple container where the software being packaged deployed on multiple EC2 instances` then in that case the `we need to manage the multiple container ovwer multiple instances` which is known as the `container orchestration`

- in this particular case the `we can use the own container orchestration tool which can be very difficult` or use the `Amazon ECS container orachestration tool` which can run `multiple container on a EC2 cluster with scale`

- in this case the `EKS` also used for thee `container orachestration but uses different tool with different feature`

- in order to `create process inside the docker container` then we need to use the `ECS/EKS` in demand 

- we can run the `Amazon ECS and EKS` on top of the `EC2 instances` which is optional


# <ins> AWS Farget Service </ins> #

- `AWS Fargate` is a `serverless compute platform` which will run the `ECS/ELK` without the hassel to `run on the EC2 services`

- if we want to use the `AWS container service` don't want to use the `underlying OS` then we can go for the `AWS Farget Solution`

- in this case the `we will not be haivng the access to the EC2 instance ans those will be handled by AWS itself`

- but we can `start/stop/restart` processes inside the `docker container` using the `ECS/EKS service with FARGATE`



- if we want to host `traditional application` with full access to the `underlying system` then we need `Amazon EC2 instances`

- if we want `serverless compute` without the `hassel of Underlying infrastructure` for `quick computing/ short running app/service-oriented application or event driven application` then we can use the `AWS Lambda services`

- if we want the `container workload service` with `ECS and EKS` ontop of the `EC2 instance` we can use the `ECS and EKS service`

- but if we want the `ECS and EKS` without the `EC2` then we can use the `AWS Fargate Solution`

- we need to choose the `container service whether ECS or EKS` followed by the `whether we want to run on platform such as EC2 or Fargate which is serverless which being managed by AWS`



# <ins> What is Serverless </ins> #

- The term “serverless” means that your code runs on servers, but you do not need to provision or manage these servers. 

- With serverless computing, you can focus more on innovating new products and features instead of maintaining servers.

- `Another benefit of serverless computing` is the `flexibility to scale serverless applications automatically`.

- Serverless computing can adjust the applications' capacity by modifying the units of consumptions, such as throughput and memory. 

- Based on the `throughput and memory. ` Serverless computing can adjust the applications' capacity

- An AWS service for serverless computing is AWS Lambda.

- `AWS Lambda` is a `service that lets you run code without needing to provision or manage servers`. 

- While using AWS Lambda, you pay only for the compute time that you consume , harges apply only when your code is running

- You can also `run code for virtually` or `any type of application or backend service`, `all with zero administration`. 

- For example, a` simple Lambda function might involve automatically resizing uploaded images to the AWS Cloud`. 

- In this case, `the lambda function triggers when uploading a new image. `


# <ins> Steps for AWS Lambda </ins> #

- `You upload your code to Lambda. `

- Y`ou set your code to trigger from an event source,` `such as AWS services, mobile applications, or HTTP endpoints.
`
- `Lambda runs your code only when triggered.`

- `You pay only for the compute time that you use.`

- In the previous example of` resizing images, you would pay only for the compute time that you use when uploading new images. `
 
- `Uploading the images triggers Lambda to run code for the image resizing function.`


# <ins> Containers </ins> #

- In AWS, you can also build and run containerized applications.

- Containers provide you with a standard way to package your application's code and dependencies into a single object

- You can also `use containers for processes and workflows` in which there are` essential requirements for security, reliability, and scalability.`

- Suppose that a company’s application developer has an environment on their computer that is different from the environment on the computers used by the IT operations staff. 

- The developer wants to ensure that the application’s environment remains consistent regardless of deployment, so they use a containerized approach

- This helps to `reduce time spent debugging applications and diagnosing differences in computing environments.`

- When running c`ontainerized applications, it’s important to consider scalability.`

- Suppose that `instead of a single host with multiple containers`, you have to `manage tens of hosts with hundreds of containers`

- Alternatively, you have to manage possibly hundreds of hosts with thousands of containers. `At a large scale, imagine how much time it might take for you to monitor memory usage, security, logging, and so on.`

- `Amazon Elastic Container Service (Amazon ECS) and Amazon Elastic Container Service (Amazon ECS)` is a `highly scalable`,` high-performance container management system` that enables you to `run and scale containerized applications on AWS`

- `Amazon ECS supports Docker containers.` Docker is` a software platform that enables you to build, test, and deploy applications quickly`

- AWS supports the use of open-source Docker Community Edition and subscription-based Docker Enterprise Edition

- `With Amazon ECS`, you can `use API calls` to `launch and stop Docker-enabled applications.`

