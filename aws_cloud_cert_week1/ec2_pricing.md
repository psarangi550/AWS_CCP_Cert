# <ins> Amazon EC2 pricing </ins> #

- for `Amazon EC2` as the `instance` belong to `different instance family` we have `multiple billing options available`

- With Amazon EC2, `you pay only for the compute time that you use `

- Amazon EC2 offers a variety of pricing options for different use cases.

    - For example, `if your use case can withstand interruptions, you can save with Spot Instances.`

    - You can also save by `committing early and locking in a minimum level` of use with `Reserved Instances`

- there are `couple of purchase option available for EC2 instaces`

    - `on-demand` (Most people familar)

        - `On-Demand` Instances are `ideal for short-term, irregular workloads that cannot be interrupted`

        - `No upfront costs or minimum contracts` apply. 

        - The instances` run continuously until you stop them`

        - we need to `pay` for the `duration` that `EC2 instance runs for`

        - this can be below depeding on the `EC2 instance type or operating System We choose`

            - `per-sec` basis

            - `per-mins` basis

        - `no long term commitment` or  `upfront pyment` needed while using the `on-demand` type of `EC2 instance`

        - this will be `useful` while we are `getting started` and `want to spin up the server` to play around with the `Workload that we have`

        - we don't need the `prior contract` or `communication with AWS ` while using th `on-demand` EC2 instances pricing

        - this can set a `baseline` for the `average workload usage` which can help in fetch which type of `EC2 instance pricing ` that we want 

        - `Sample use cases` for ` On-Demand Instances` include `developing and testing applications and running application`s that `have unpredictable usage patterns`

        - On-Demand Instances are `not recommended` for `workloads that last a year or longer` because these workloads `can experience greater cost savings` using `Reserved Instances`.

    
    - `savings plan`

        - `saving plan` offer `low prices` on the `EC2 innstances usage` in exchange of the `commitment` that `consistent amount of compute usage` measured in `dollar/hour` for a `1 or 3 years plan`

        - this `savings plan` on `EC2 instances` can provide `72% percentage saving on AWS compute usage `

        - this can lower prices on the `EC2 instances usage` regardless whether 

            - `instant family` of `EC2 instance`

            - `Opering System` of `EC2 instance`

            - `Size` of `EC2 instance`

            - `Aws region`of `EC2 instance` 

        - this can be applied onto the `AWS Fargate` and `AWS Lambda usage` which has `serverless compute option`

        - `Any usage up to the commitment` is charged at the `discounted Savings Plan rate` (for example, $10 an hour). `Any usage beyond the commitment` is `charged at regular On-Demand rates.`

        - `AWS Cost Explorer`, a `tool` that `enables you to visualize, understand, and manage your AWS costs and usage over time.`

        -  If you are `considering your options for Savings Plans`, `AWS Cost Explorer` can analyze your `Amazon EC2 usage over the past 7, 30, or 60` days

        - `AWS Cost Explorer` also `provides` `customized recommendations for Savings Plan` , These recommendations estimate how much you could save on your monthly Amazon EC2 costs, based on previous Amazon EC2 usage

        - show also `the hourly commitment amount in a 1-year or 3-year Savings Plan.`

    
    - `reserved instances`

        - `Reserved Instances are a billing discount applied to the use of On-Demand Instances` in your account

        - you can purchase Standard Reserved and Convertible Reserved Instances for a 1-year or 3-year term


        - thse are suited for `steady state workload` or `ones with predictable usage`

        - this provide the `75%` discount `verses` the `on-demand pricing ` 

        - we are qualified for the `discount` one we `commit for 1 /3 years of term`

        - we can pay as well for 3 `payment options`

            - `All upfront` :- we need to `pay full amount `while we `commit for the same`\

            - `partial upfront` :- we need to pay for the `portion of the amount` when we commit for `1 or 3 years`

            - `no upfront` :- `we don't have to pay anything` at the beginning when we commit for `1 or 3 years`


        - we can also  Scheduled Reserved Instances for a 1-year term. You realize greater cost savings with the 3-year option.

        - At the end of a Reserved Instance term, you can continue using the Amazon EC2 instance without interruption. However, you are charged On-Demand rates until you do one of the following:

            - terminate the instance.

            - Purchase a new Reserved Instance that matches the instance attributes (instance type, Region, tenancy, and platform).

    
    - `spot instances` :-

        - Suppose that you have a background processing job that can start and stop as needed (such as the data processing job for a customer survey). 
        
        - You want to `start and stop the processing job without affecting the overall operations of your business`

        - If you make a Spot request and Amazon EC2 capacity is available, your Spot Instance launches.
        
        -  However, if you make a Spot request and Amazon EC2 capacity is unavailable, the request is not successful until capacity becomes available. The unavailable capacity might delay the launch of your background processing job.

        - After you have launched a Spot Instance, if capacity is no longer available or demand for Spot Instances increases, your instance may be interrupted

        -  This might not pose any issues for your background processing job.

        - However, in the earlier example of developing and testing applications, you would most likely want to avoid unexpected interruptions. Therefore, choose a different EC2 instance type that is ideal for those tasks.

        - `Spot Instances` are `ideal` `for workloads` with `flexible start and end times`

        - here it allow `to request spare Amazon EC2 computing capacity` for upto `upto 90% off the on-demand price `

        - But here the `catch is` AWS can `reclaim the instances back at any time they need`

        - But `gives a 2 mins working to finish the work and save state`

        - we can also resume  later if needed 

        - `spot instances` is a place where the `Workload can be interupted`

        - if we have `batch workload` then we can select the option as `spot instanes`


    - `dedicated hosts`

        - these are `physical host` dedicated for your `EC2 usage`

        - these are used for `meeting certain compliance requirements ` 

        - in this case noody will share the `host` possession of that 

        - You can use your `existing per-socket, per-core, or per-VM software licenses` to help` maintain license compliance`

        -  You can purchase

            -  On-Demand Dedicated Hosts

            - Dedicated Hosts Reservations.

        - this is the `most expensive` EC2 instance that we covered  tll now 

        



    

