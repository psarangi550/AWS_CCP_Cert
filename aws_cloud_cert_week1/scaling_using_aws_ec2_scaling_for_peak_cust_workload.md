# <ins> How to Scale the Hardware using the AWS EC2 Auto Scale for peak customer Workload </ins> #

- there are 2 ways to handle the `growing demand`

    - `scale up`

        - `scaling up` means `adding more power to the machine i.e instances that are running` which is not always helpful

        - but in case of the `some cases` this might be benifial

        - as the `it really depend on the customer request or customer workload`


    - `scale out`

        - we can create `more instances` which can server the `customer workload`

        - if we are increasing the `no of instances based on the customer workload` we also have to increase the `backend processing for the space`

        - so that the `order taking should not be greater than the order serving`

        - if the `order taking is more than the order making` then we need to create the `backlog for the same`

        - we can `decouple the system` where we have `right amount of power for each part of the process ` rather than `over provisioning to solve the separate problem`

        - for each `part of the process  we can provide right amount of power to handle the request by decopuling the system`

        - once the `customer workload been handled` all the `extra power used for each part of the processes can be switched off i..e stop the instance`

        - we can `add instances based on demand` and `decommision  them as it got cleared ` by using the `AWS EC2 auto scaling`

        - every day based  on the `customer workload` the instances can be spunned 

    
- In the cloud, `computing power is a programmatic resource`, so you can take a more flexible approach to the issue of scaling

- `By adding Amazon EC2 Auto Scaling to an application`, you can` add new instances to the application when necessary` and` terminate them when no longer needed`.

- Suppose that you are` preparing to launch an application on Amazon EC2 instances.` When `configuring the size of your Auto Scaling group`, you might `set the minimum number of Amazon EC2 instances at one`. This means that at all times, there must be at least one Amazon EC2 instance running.

- When you `create an Auto Scaling group`, you can `set the minimum number of Amazon EC2 instances`. The `minimum capacity is the number of Amazon EC2 instances` that `launch immediately after you have created the Auto Scaling group`. In this example, the Auto Scaling group has a minimum capacity of one Amazon EC2 instance

- Next, you can `set the desired capacity at two Amazon EC2 instances even though your application needs a minimum of a single Amazon EC2 instance to run`.

- Note: `If you do not specify the desired number of Amazon EC2 instances` in an Auto Scaling group`, the desired capacity defaults to your minimum capacity.`

- The third configuration that you can set in an Auto Scaling group is the maximum capacity. For example, you might configure the Auto Scaling group to scale out in response to increased demand, but only to a maximum of four Amazon EC2 instances.

- Because Amazon EC2 Auto Scaling uses Amazon EC2 instances, you pay for only the instances you use, when you use them. 

- You now have a cost-effective architecture that provides the best customer experience while reducing expenses.
        

