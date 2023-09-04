# <ins> Amazon CloudWatch </ins> #

- `Now we're making lots of coffee`, `serving customers`, and `everything seems to be going spiffy/smart in our coffee shop`

- But as we `run` `espresso machines` `more and more`, `use mugs`, `constantly open and close the fridge` , `we want to be able to make sure we're alerted to something which might have gone all right`

- May be an `espresso machine` `needs to be cleaned or repaired`.

- The point is, `as a business owner`, you `need` `visibility` into the `state of your systems`

    - `Are things running well?`

    - `Do you see a degraded customer experience?`

    - `Are you frequently delivering the wrong drink to customers?`

    -  `or is everyone getting their orders as expected ?`

- `You have all questions about the success of your operations`.

- The `same idea` `applies` to `systems built on AWS`

- You need a way to `monitor` the `health and operations ` of your solutions.

- `Luckily, you don't need to build out your own monitoring platform,  We have done this for you`

- `Introducing Amazon CloudWatch`

# <ins> Amazon CloudWatch </ins> #

- `CloudWatch` `allows` you `to monitor your AWS infrastructure and the applications` `you run on AWS` `in real time`

- It `works by` `tracking and monitoring metrics`.

- `Think of` `metrics` `as` `variables` `that are tied to your resources`.

-  For example, 
    
    - `the amount of espressos made by an espresso machine`

    - `the CPU utilization of an EC2 instance.`

- Let's take a customer approach for our coffee shop

    - `Say we have an espresso machine and it needs to be cleaned after it makes 100 espressos`

    - `CloudWatch allows us to create a custom metric called espresso count`

    - `once it hits 100`

    - `we want to alert staff to clean the machine`

    - Well, with `CloudWatch`,` you can accomplish this by creating` what is called a `CloudWatch alarm`

    - `You set a threshold for a metric`

    - `when` that `threshold is reached`, `CloudWatch` can `generate an alert` and `trigger an action`

    - `This means` we can `alert on the custom metric`, in this case `hitting 100`, and `then perform an action even better.`

    -  `CloudWatch alarms are integrated with SNS`

    - `We can then send an SMS to the manager to say, clean the machine`

    - You can create `all sorts of custom alarms` `for metrics ` `from all different types of AWS resources`.

-  Now, `what if we want to aggregate all those metrics in a single pane of glass`

- Well, `we can use CloudWatch's dashboard feature`

- `Think of a dashboard as a screen` which `lists outs metrics in near real time`.

- `In our case, we can create a CloudWatch dashboard, which will show us all our espresso machines and the espresso counts so we can proactively monitor them.`

- `These dashboards would auto-refresh when they're open so we can see an up-to-date view of our resources`

# <ins> Benefits of Using Amazon Cloudwatch </ins> #

- Finally, what are the benefits of using a service such as CloudWatch

    -  Well, the first one is that you can have access to all your metrics from a central location

    -  `This` `enables` you to `collect metrics and logs from all your AWS resources, applications, and services that run on AWS and on premises service`, `helping you break down silos` `so that ` y`ou can easily gain system-wide visibility`

    - `You can also get visibility` `across` `your applications, infrastructure and services`

    - `which means` you `gain insights across your distributed stack`  , so you can ` "correlate and visualize metrics and logs" to quickly pinpoint unresolved issues`

    - `This in turn means you can reduce meantime to resolution or MTTR, and improve total cost of ownership or TCO`

    - `In our coffee shop, if the MTTR of cleaning our espresso machines is shorter, then we can save on TCO with them.`

    - `This means` `freeing up important resources` `like developers` `to focus on adding business value`

- Lastly, `you can drive insights` to `optimize applications and operational resources ` 

- for example, `aggregating usage across an entire fleet of EC2 instances to derive operational and utilization insights `


- `Now our staff can focus on serving coffee` `versus` `constantly cleaning machines before they are due to be cleaned`




