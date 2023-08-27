# <ins> How to Provision AWS Resources inside AWS global Infrastructure </ins> #

- we can `interact with AWS resources / services inside thwe AWS global infrastructure`  using the `API call`

- in `AWS` `every communication with the services` been done using the `AWS API calls`

- An `API` stands for the `Application programming Interface` which means that `there are certain predefined rules to communicate with AWS Services`

    - using the `API call` we can do the `provisioning , configuration and management of the AWS resources`

    - we can create the `AWS EC2 instance or create the AWS Lambda function` each of them having different `requestv for API call request to AWS`

    - we can interact with the `AWS services and Resources` through `API call` in `many dfferent ways` to `proviosionk, configure and manage`

        - `AWS management console`

            - `AWS management console` is of `browser based`

            - The `AWS Management Console` is a `web-based interface for accessing and managing AWS services`

            - `You can quickly access recently used services` and `search for other services by name, keyword, or acronym.`

            - `The console` includes `wizards and automated workflows` that can `simplify the process of completing tasks`.

            - this is the basic point to get started where we can access the `service` through `API` using a `Browser console`

            - this will be very easy to `visualize the AWS resources` the `provision , configuration and management` which is `easy to digest`

            - if we want to run an `EC2` service  then we can choose `multiple configuration in order to create EC2 instances`

            - But we need to `manually provision again another EC2 instance` if we need to `provision like earlier`

            - As here there are `multiple manual step to provision which can lead to human error`

            - this will be very useful for 

                - `Test Environment`

                - ` viewing monitoring service`

                - `working with non technical resouces`

                - `viewing AWS bills`

            - You can also use the` AWS Console mobile application` to `perform tasks such as` 
                
                - `monitoring resources`
                
                - `viewing alarms`
                
                - `accessing billing information`

            -  `Multiple identities` can `stay logged into the AWS Console mobile app at the same time.`

            - the `AWS management console` is great for `learning intial hands on` but manual in nature rather than `automated`

        - `AWS command Line interface or AWS (CLI)`

            - `To save time when making API requests, you can use the AWS Command Line Interface (AWS CLI).`

            - AWS CLI enables you to control multiple AWS services directly from the command line within one tool.

            - AWS CLI is available for users on `Windows, macOS, and Linux. `

            - if we are running a `production Environment` then this `point and click` `will not be very helpful`

            - if we want to provision multiple `EC2 instances` then we can do that using the `Amazon Command Line interface`

            - `Amazon CLI` will refer `AWS API service` from the `terminal of the user to prioivision , configure and management of resources`

            - we can use a `Script or programs` which can make those `API call to provision, configure and manage the resources`

            - using the `AWS CLI option` we can also `schedule the Script to interact with AWS resources at regular interval`

            - if we want to create the `AWS EC2 Intsance` using the `AWS CLI` nthen we can use the command as 

                ```
                    aws ec2 run-instances \
                    
                    --image-id <image id>  \
                    
                    --count <no of count of instancesa> \

                    --instance-type t2.micro \

                    --key-name <key name> \

                    --security-group-ids <securith group id> \

                    --subnet-id <subnet-id> \

                    --profile cpe 
                
                
                ```

            - By using `AWS CLI`, you can `automate the actions that your services and applications perform through scripts`

            - using the `AWS CLI` we can make the `action as scriptable and repeatable command to make the API call`

            - this will make less `suspectable to human error as we are not writing th code manually`

            - `automation` is really essential for a `successful cloud deployment`

            - For example, you can `use commands to launch an Amazon EC2 instance`, `connect an Amazon EC2 instance to a specific Auto Scaling group, and more.`

        - `AWS Software Development Kit or (SDK)`

            - we can also use the `AWS Software development Kit` i.e `AWS SDK` to interact with `AWS resources and the programing language` without to deal `Low Level API`

            -  `SDKs` make it `easier for you to use AWS services` `through an API` `designed for your programming language or platform`

            - `SDKs` `enable` you `to use AWS services` with `your existing applications or create entirely new applications that will run on AWS.`


            - here the `developer uses the AWS resources` without using the `low level API` and also manual `provision and configuration and management can be avoided`

            - `To help you get started with using SDKs, AWS provides documentation and sample code for each supported programming language`

            -  Supported programming languages include C++, Java, .NET, and more.

        - `other resources` such as `AWS cloud formation`



