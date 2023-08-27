# <ins> How to Provision AWS Resources inside AWS global Infrastructure Part-2 </ins> #

- The below services are `do it yourself type provision ways of managing the AWS Resources and Services`

    - `Aws Management console`

    - `AWS CLI`

    - `AWS SDKs`

- There are other way to manage the `AWS Resources and Services` using the `Management Tool` such as 

    - `Aws Cloud Formation`

    - `Aws Elastic BeanStalk`

# <ins> AWS BeanStalk </ins> #

- Instead of `Provisioning EC2 instance` through 

    - `point and click using the AWS Management console`

    - `writing command to make API calls from CLI`

    - `Writing program to provision the AWS Service / resource and environment`

    - using the `AWS Elastic BeanStalk service` we can just provide the `  application code which we want to run` and `configuration for EC2 instance provision and networking and Scaling and using the Elastic Load Balancer ` which takes the `configuration and application code` and `build out the AWS environment for the same`

    - using the `AWS BeanStalk Service` we can save the `environment configuration` so that same `AWS environment can be redeployed very easily`

    - using the `AWS BeanStalk Service` we don't have to `provision and manage the AWS service and resources separately` from the `application code` rather we can do it `together` having the `access and visisbilty to the underlying resources such as the AWS environments `

    - `AWS BeanStalk service` help in `focus on the Business application code` rather than the `underlying infrastructure` for the same 

# <ins> AWS Cloud Formation </ins> #

- we can also use the `AWS cloud formation Service` for `Automated and Repeatable cloud deployment`

- `AWS cloud Formation` is a `infrastructure as code tool` used to define `wide verity of AWS resources` in a `declared way of JSON and YAML text based document` in the form of `cloud formation template` which need to be `deployed`

- `These declared JSON and YAML cloud formation Template` define `What we want to build resources rather than How to build those resources`

- the `cloud formation will define what resources we want to build` and `cloud formation engine will help in getting those details from the cloud formation template in declared JSON and YAML format to build those resources`

- The `cloud formation enginee` will call out the `API` based on the `cloud fomration template` in order to `build those resources`

- `AWS cloud formation` not only support only `EC2 instances` but support `verity of AWS Services and Resources` such as 

    - `Storage`

    - `Databases`

    - `Analytics`

    - `Machine Learning`

- once we define the `AWS resources` inside the `cloud formation template using declared JSON or YAML format` then `AWS cloud formation Engine` will parse those info written in the `cloud fomration template` and `begine provision those resources using API call in parallel`

- `AWS cloud formation Engine` will help in manage all the `backend APi call to the AWS services and Resource on the background`

- we can run the `same cloud fomation template` on `multiple account` or `multiple Availabity Zone or AZ or Multiple AWS region` to deploy and Provision `the same identical environement accross different places`

- There is less chances of `Human Error` as all the `services will be dployed based on the cloud formation template parsed by the AWS cloud formation enginee and making multiple APi call on the backend ` which is an `automated process`


- we can use the `management tool` such as 

    - `AWS ElasticBeanStalk`

    - `AWS CloudFormation`

    - in order to perform the `provision / configuration and managemenbt of AWS Resources and Services`


**AWS Elastic Beanstalk**

- `With AWS Elastic Beanstalk`, you `provide code and configuration settings`, and `Elastic Beanstalk deploys the resources necessary to perform the following tasks:`

    - `Adjust capacity`

    - `Load balancing`

    - `Automatic scaling`

    - `Application health monitoring`


**AWS CloudFormation**

- With `AWS CloudFormation, you can treat your infrastructure as code`. 

- This means that `you can build an environment` by `writing lines of code` instead of using the `AWS Management Console to individually provision resources.`

- AWS CloudFormation `provisions your resources` in a `safe, repeatable manner, enabling you to frequently build your infrastructure and applications` without having to perform manual actions or write custom scripts. 

- `It determines the right operations to perform when managing your stack `and `rolls back changes automatically if it detects errors.`

