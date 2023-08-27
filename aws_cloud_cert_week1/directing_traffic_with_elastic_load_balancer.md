# <ins> Directing Traffic With Amazon Elastic Load Balancer </ins> #

- even though we solve the `scaling problem` which can handle `large customer workload` with `Amazon EC2 Auto scaling` but we still have the `traffic problem`

- Lets Take the `coffee example` into the consideration 

    - Even though we have many instances of `morgan` which is `order taking instances` or `barista` in a `coffee shop` but customer keep pile on `one morgan` which create `uneven distribution of customer per line` and hence other `order taking instances are idle doing nothing`

    - this happens because `customer /client request` comes in but does not know `where to route the order`

    - in that case we can `use a host at the gate` which look into the `cashier / order taking instance/barista` and count the `no of customer per line` and redirect the `customer/client request` to specific `order taking lines` which is `least in number` to server better and `evenly distribute the loads accross order taking instances `

    - As the `host at the gate always have a look on the cashier` it will redirect the customer where the `number of customer per order taking system` are very less for `even distribution` among the cashier

    - the same idea reflect on the `EC2 instances` as well , when we have multiple `EC2 instances with same program running in each instances` the `client request still be going to one EC2 instances` making the other as `idle` as the `client request does not know to which instances to go to`

    - we need to make sure the `Even distribution of Workload` accross all the `EC2 instances` , make sure not `one of been backed up` where the rest all are `sitting idle`

    - Hence we need to `route` the `customer request` to `individual  EC2 instances` to `process the request evenly`

    - this process of `evenly distibuting the customer request load known as load balancing`

#  <ins> What is Load Balancing </ins> #

- The `load balancer` is an `appliocation` which takes in the requests and `route them to individual instances` to be get `processed`

- there are `off the shelf outside load balancer` which works great with AWS

- But if we are using the `outside off shelf load balacer` then the ` your operation Team` need to handle 

    - `manage`
    - `update`
    - `scale` ---> `scale out more EC2 instances `
    - `failover`
    - `availablity`

- here we need to redirect the customer request to a `Scalable System` which is 

    - `high performance`
    - `cost efficient`
    - `Highly available`
    - `Automatically Scalable`

- After we redirect the customer request to the `Scalable System` then we can just forgot about it after setting it  which can be done using the `Elastic Load Balancing` or `ELB`

- this `ELB` can perorm the `undifferenciated heavy lifting` of `load balancing`

- `ELB` handles the `traffic  for a customer request` which is a `regional construct` hence making it  as `highly available` which can manages the `load balances` accross any `EC2 instances`

- as `ELB` runs on the `regional label` not on the `individual EC2 instances ` which make its `service` as `Highly available `

- `ELB` is `automatically scalable ` which can handle additional `throughput` if the `customer workload traffic increses` without the change in `hourly cost`

- when the `customer workload traffic is high` then `Fleet of EC2 instances come online` because of the `EC2 auto scaling` based on the `group they are in` then `EC2 Autoscale service` will send an `notification to ELB` to evenly `distibute the customer workload`

- Oncve the `EC2 instance fleet been online AWS EC2 auto scaling` will help in `notified to ELB` 

- once the works of the` additional fleet of EC2 Instances`completed then `ELB first stop all new traffic` and `wait for the existing customer request to complete` so tht `EC2 instances can be free `

- Then the `EC2 Auto Scaling` can turn off the `instances without disrupting the existing consumer`

- `ELB` not only used for external traffic

    - lets think of `ordering Tier` which is the `fronntend` and corresponding `Production Tier` which is the `backend`

    - in both the `front and backend` tier `multiple instances were running ` where `Each frontend or ordering Tier` know about the `Backend or production Tier`

    - Lets suppose a `New Backend instance` added then that `instance` will send notification to `Each front end or orering Tier` instances letting them know that they are `available`

    - this can get more complecated if we have `multiple no of instances` getting added and sensdingnotification to each `instances of other node`

    - we can solve the `backend traffic chaos` with `ELB` as well

    - as `ELB` is `regional construct` which will be on `regional label` hence each request will go  in with `single URL` for all `frontend instances`

    - then the `ELB` get all the request from the `frontend` and redirect to the `backend` which has `least amount of outstanding request`

    - once the `Backend Instances` increased the the `AWS EC2 Auto scaling` will will let the `ELB know` and `ELB will redirect the request for that`

    - here `with the use of ELB` the `frontend instances` does not have to know how many `backend instances` been running 

    - this make it the `decoupled architecture` of the system

- the `backend` communication for which `ELB` is just one method for the same 


- `Elastic Load Balancing` is the` AWS service` that `automatically distributes incoming application traffic across multiple resources`, such `as Amazon EC2 instances`. 

- `A load balancer` acts `as a single point of contact `for `all incoming web traffic to your Auto Scaling group`

- This means that as you add or remove Amazon EC2 instances in response to the amount of incoming traffic

- these incoming requests route to the load balancer first. Then, the requests spread across multiple resources that will handle them

- For example, if you have multiple Amazon EC2 instances, Elastic Load Balancing distributes the workload across the multiple instances so that no single instance has to carry the bulk of it. 

- Although `Elastic Load Balancing and Amazon EC2 Auto Scaling` are `separate services`, they `work together to help ensure that applications running in Amazon EC2 can provide high performance and availability. `


# <ins> Example: Elastic Load Balancing </ins> #

- **Low-demand period**

    - Here’s an example of how Elastic Load Balancing works. Suppose that a few customers have come to the coffee shop and are ready to place their orders. 

    - If only a few registers are open, this matches the demand of customers who need service. The coffee shop is less likely to have open registers with no customers. In this example, you can think of the registers as Amazon EC2 instances.

- **High-demand period**

    - Throughout the day, as the number of customers increases, the coffee shop opens more registers to accommodate them. 

    - Additionally, a coffee shop employee directs customers to the most appropriate register so that the number of requests can evenly distribute across the open registers. You can think of this coffee shop employee as a load balancer. 


