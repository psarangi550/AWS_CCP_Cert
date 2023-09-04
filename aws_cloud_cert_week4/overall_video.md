# <ins> Summary </ins> #

- `First things first, AWS follows a shared responsibility model`

- `AWS is responsible for security of the Cloud and you are responsible for security in the Cloud`

# <ins> IAM </ins> #

- `With IAM`, `you have users, groups, roles, and policies`

- `IAM Users log in with a username and password, and by default, they have no permissions`.

- `Groups are groupings of users`

- `Roles are identities` that `you can assume` `to gain access to temporary credentials and permissions for a configurable amount of time`.

- In order to `give permissions to an identity`, you `need to create policies` that` either explicitly allow or deny a specific action in AWS`

- With `IAM` also comes `identity federation`

-  If you have an `existing corporate identity store`, you `confederate/join` those` users to AWS using role-based access`, `which allows your users to use one login for both your corporate systems as well as AWS.`

- `One final point to remember about IAM is that you should make sure that you turn on multi-factor authentication for users, but especially for your root use`

- `root which has all the permissions by default and cannot be restricted`

# <ins> AWS Organization </ins> #

- `With AWS, it's likely you'll have multiple accounts`

- `Accounts` are `commonly used to` `isolate workloads, environments, teams, or applications`

- `AWS organizations` `helps you manage` `multiple accounts in a hierarchical fashion`


# <ins> compliance </ins> #

- `AWS uses third-party auditors to prove its adherence to a wide variety of compliance programs`

- `You can use the AWS Compliance Center to find more information on compliance `

- `AWS Artifact to gain access to compliance documents.`

- `The compliance requirements you have will vary from application to application and between areas of operation`

# <ins> Distributed Denial Of Service Attack or DDoS </ins> #

- `Then we talked about distributed denial-of- service attacks or DDoS attacks and how to combat them with AWS using tools like ELB, security groups, AWS Shield, and AWS WAF`

# <ins> AWS KMS (AWS Key Management Service) </ins> #

- `We also talked about encryption. In AWS, you are the owner of your data and you are responsible for it's security`

- `That means you need to pay attention to encryption, in transit and at rest.`

# <ins> Summary </ins> #

- `There are lots of considerations when dealing with security in AWS.`

- `Security is AWS's top priority and will continue to be so`

- `Please make sure you read the documentation on securing your AWS resources , as it does vary from service to service.`

- Use the least privilege principle when scoping permissions for users and roles in IAM.

- encrypt your data at every layer, both in transit and at rest 

- make sure you've used AWS services to protect your environment.