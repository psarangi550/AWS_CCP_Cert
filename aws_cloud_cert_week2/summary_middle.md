# <ins> Overall Summary of AWS global infrastructure </ins> #

- `Logical cluster of data center` created the `Availability Zone`

- `Availabity Zone or AZ` creates the `AWS Regions` which been `distributed globally`

- We should `deploy infrastructure` atleast accross `2 availabilty Zones`

- there are few `AWS Regional Service` such as below deployed on `mutiple AZ or avialbility Zone`

    - `AWS ELB`

    - `AWS SNS`

    - `AWS SQS`

- We can use the `Edge location` to `deliver the content from the AWS region` to server the `customer with faster rate of transfer and low latency`

- `Edge devices` such as `AWS Outpost` which allow us to `run the AWS infrastructure i.e AWS mini region handled by AWS in the on premises data center`

- we can provision the `AWS resources and service` using the below option such as 

    - `AWS mnagement console`

    - `AWS CLI`

    - `AWS SDKs`

    - `management tool` such as 

        - `AWS BeanStalk`

        - `AWS cloudformation` where we can run the `infrastructure as code`


- this will help in getting `How globally Avialbility of AWS is ` and `How Easy to Set this up`


#NOTES

- `A Region consists of two or more Availability Zones.`

- For example, `the South America (São Paulo) Region is sa-east-1. It includes three Availability Zones: sa-east-1a, sa-east-1b, and sa-east-1c.`

- `Assigning custom permissions to different users` is a `feature that is possible in all AWS Regions.`

- `The AWS Command Line Interface (AWS CLI) is available in all AWS Regions.`

- `The level of support that you choose is not determined by Region. AWS Support plans are explored later in this course.`

- Amazon CloudFront is a `content delivery service. `

- `It uses a network of edge locations to cache content` and `deliver content to customers all over the world.` 

- `When content is cached, it is stored locally as a copy. This content might be video files, photos, webpages, and so on.`

- `AWS Outposts` is a service that `enables you to run infrastructure in a hybrid cloud approach.`

- `AWS Fargate `is a `serverless compute engine for containers.`

- `Amazon Simple Queue Service (Amazon SQS) is a service that enables you to send, store, and receive messages between software components through a queue`

-` An Availability Zone` is a `fully isolated portion of the AWS global infrastructure`.

- `A Region is a separate geographical location with multiple locations that are isolated from each other.`

- An `origin` is the `server` `from which CloudFront gets your files`. 

- Examples of `CloudFront origins include Amazon Simple Storage Service (Amazon S3) buckets and web servers.`