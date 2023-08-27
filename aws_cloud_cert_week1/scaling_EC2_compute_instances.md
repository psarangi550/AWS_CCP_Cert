# <ins> How to Scale AWS EC2 instance </ins> #

- `Scalabity and Elasticity in AWS EC2`

    - how the `capacity` can `growor shrink` based on the `business need`

    - when we are using the `on premises data center where all physical server being deployed and application been hosted upon` then like `a real time 99% of the business out in the world` the `customer workload` vary over time that can be `24 hr period or weeks thats are busy oe other week not in demand`

    - if we are using the `own data center` what wiull be the `right amount of hardware to purchase`

    - when we are purchasing based on the `average customer work load` then it will not be a `problem` if we are not having `customer workload in peak hours`

    - But will be having the `hardware problem to provide the service` when we have `customer workload on the peak` which will be making th result

    - if we are purchasing the `hardware` based on the `p[ek customer workload` then for most of the `time` the `hardware can go idle` which will make the `average usage of the hardware in data center very low upto 10%`

    - By using the `AWS` we can `provision the hardware for the workload based on the customer workload demand for every hour or everyday`

    - we have both `customer happy as well as the Finance officer happy as we have the exact ROI that we need`\

    - quote by `werner volgue` that `plan for the failure then the failure will never going to happen`

    - lets take the `coffee` example in here 

        - lets suppose `morgan` taking the `coffe order` from the customer and `rudy` been performing the `backend service`

        - if the `order taking system been off i.e morgan being off` then  in that case we can create a ` new morgan` to take the order 

        - this will help in `making the hardware highly available without a single point of failure`

        - we can use the same concept for the `backend processing` and `create a New redundant Rudy here`

        - this will help to maintain the `hardware available for avaerage custom workload` 

        - But we need to see what will happen if we have `peak customer workload in that case ` :----->



- `Scalability involves` beginning` with only the resources` you need and` designing your architecture to automatically respond to changing demand by scaling out or in`

- As a result, `you pay for only the resources you use`. `You don’t have to worry about a lack of computing capacity to meet your customers’ needs`

- If you wanted the `scaling process to happen automatically`, which AWS service would you use? The AWS service that provides this functionality for Amazon EC2 instances is `Amazon EC2 Auto Scaling`.

- **Amazon EC2 Auto Scaling**

    - If you’ve tried to access a website that `wouldn’t load` and` frequently timed out,` the` website might have received more requests than it was able to handle.`

    - This situation is similar to waiting in a long line at a coffee shop, when there is only one barista present to take orders from customers.

    - `Amazon EC2 Auto Scaling` enables you to `automatically add or remove Amazon EC2 instances` in response to `changing application demand`

    - By automatically scaling your instances in and out as needed, you are able to maintain a greater sense of application availability.

    - Amazon EC2 Auto Scaling, you can use two approaches: 
        
        - `dynamic scaling `

            - `Dynamic scaling responds to changing demand`.

        - `predictive scaling`

            -  `Predictive scaling automatically schedules the right number of Amazon EC2 instances based on predicted demand.  `   
