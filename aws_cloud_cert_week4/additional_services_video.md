# <ins> Additional Security Services </ins> #

- With all the `comings and goings on in your coffee shop`, `you'll want to increase security to your "coffee beans, equipment and even money in the till" `

- `For your beans`, this `could be when they are sitting in your storeroom` or `even when you're transporting them between shops`

- After all, `we don't want unwanted visitors` `with access` `to our coffee beans` or `even running off with precious equipment.`

- `To start` off, let's chat about `how you can secure your coffee beans or your data` `whether it's at rest or in transit.`

- `For our beans, the simple way to do it would be to lock the door when we leave at night`

-  That's the `notion of encryption.`

-  `which is securing a message or data in a way that can only be "accessed by authorized parties."`

- `Non authorized parties are therefore less likely to be able to access the message or not able to access it at all.` 

- `Think of it as the key and door example`

- `If you have the key, you can unlock the door but if you don't, then you cannot unlock that door.`

-  `At AWS, this comes in two variations `
    
    - `encryption at rest`

    - `encryption in transit`

- `By at rest`, we `mean` `when your data is idle`. `It's just being stored and not moving`.

- For example, `server side encryption at rest` `is enabled` `on all DynamoDB table data`, and that helps `prevent unauthorized access`.

- `DynamoDB server side encryption at rest` also `integrates with AWS KMS`, or `Key Management Service` for `managing the encryption key that is used to encrypt your tables`.

- `That's the key for your door remember and without it, you won't be able to access your data.`

- `so make sure to keep it safe`

-  `Similarly, in transit means that the data is traveling between say A and B, where A is the AWS service and B could be a client accessing the service, or even another AWS service itself.`

- `For example, let's say we have a Redshift instance running`

- `we want to connect it with a SQL client.`

- `We use Secure Socket Layer or SSL connections to encrypt data`

- `we can use server certificates to valid and authorize the client`

- `This means that data is protected when passing between Redshift and our client.`

- And `this SSL functionality exists in numerous other AWS services, such as` 
    
    - `SQS` 
    
    - `S3` 
    
    - `RDS and many more`

# <ins> Amazon Inspector </ins> #

- `But speaking of other services, the next service we want to highlight is called "Amazon Inspector" `

- `Inspector` `helps` to `improve security and compliance` of `your AWS deployed applications` by `running an automated security assessment against your infrastructure`

- Specifically, `it helps to check on` 
    
    - `deviations of security best practices`
    
    - `exposure of EC2 instances`
    
    - `vulnerabilities` 
    
    - so forth

- The service consists of three parts,

    - `network configuration reachability piece`

    - `Amazon agent, which can be installed on EC2 instances`

    - `a security assessment service that brings them all together`

- `To use` it you `configure inspector options`, `run the service`

- `pops a list of potential security issues.` 

- The `resulting "findings"` `are` `displayed` in the` Amazon Inspector console`

- `they are presented with a detailed description of the security issue` and a `recommendation on how to fix it`

- Additionally, `you can retrieve findings` `through an API ` so `as to go towards the best practice of performing remediation to fix issues`


# <ins> Amazon guard duty </ins> #

-  `Another service` to mention is our `threat detection` offering known as `Amazon guard duty`

-  It analyzes 
    
    - `continuous streams of metadata generated from your account`

    - `network activity found in AWS Cloud trail events`

    - ` Amazon VPC Flow Logs `

    - `DNS logs`

- It uses `integrated threat intelligence` such as

    - `known malicious IP addresses`

    -  `anomaly detection ` 

    - `machine learning`

    to `identify threats more accurately`

-  `The best part is that it runs independently from your other AWS services`

- So it `won't affect` `performance or availability` `of your existing infrastructure and workloads`

- `There are so many other security services like advanced shield and security hub`

