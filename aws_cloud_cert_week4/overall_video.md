# <ins> Summary </ins> #

- `First things first, AWS follows a shared responsibility model`

- `AWS is responsible for security of the Cloud and you are responsible for security in the Cloud`

# <ins> IAM </ins> #

- `With IAM`, `you have users, groups, roles, and policies`

- `IAM Users log in with a username and password, and by default, they have no permissions`.

- `Groups are groupings of users`

- `Roles are identities` that `you can assume` `to gain access to temporary credentials and permissions for a configurable amount of time`.

- `An IAM role is an identity that you can assume to gain temporary access to permissions`

- `When someone assumes an IAM role, they abandon all permissions that they had under a previous role and assume the permissions of the new role.`

- - `IAM roles are ideal for situations in which access to services or resources needs to be granted temporarily instead of long-term.` 

- `In order to` `give permissions to an identity`, you `need to create policies` that` either explicitly allow or deny a specific action in AWS`

- `IAM Policy` is a `document that grants or denies permissions to AWS services and resources.`

- `IAM policies provide you with the flexibility to customize users’ levels of access to resources.`

-  For instance, you can `allow users to access all the Amazon S3 buckets in your AWS account or only a specific bucket.`

- `You can assign permissions to users and groups in AWS Identity and Access Management (IAM).`

- With `IAM` also comes `identity federation`

-  If you have an `existing corporate identity store`, you `confederate/join` those` users to AWS using role-based access`, `which allows your users to use one login for both your corporate systems as well as AWS.`

- `One final point to remember about IAM is that you should make sure that you turn on multi-factor authentication for users, but especially for your root use`

- `Multi-factor authentication (MFA) is an authentication process that provides an extra layer of protection for your AWS account.`

- `root which has all the permissions by default and cannot be restricted`

- `The root user identity is the identity that is established when you first create an AWS account.`

- `You can update the AWS account root user password in the AWS Management Console.`


# <ins> AWS Organization </ins> #

- `With AWS, it's likely you'll have multiple accounts`

- `Accounts` are `commonly used to` `isolate workloads, environments, teams, or applications`

- `AWS organizations` `helps you manage` `multiple accounts in a hierarchical fashion`

- `Service control policies (SCPs) enable you to centrally control permissions for the accounts in your organization`. 

- `An SCP is not the best choice for granting temporary permissions to an individual employee.`


# <ins> compliance </ins> #

- `AWS uses third-party auditors to prove its adherence to a wide variety of compliance programs`

- `You can use the AWS Compliance Center to find more information on compliance `

- `AWS Artifact to gain access to compliance documents.`

- `The compliance requirements you have will vary from application to application and between areas of operation`

# <ins> Distributed Denial Of Service Attack or DDoS </ins> #

- `Then we talked about distributed denial-of- service attacks or DDoS attacks and how to combat them with AWS using tools like ELB, security groups, AWS Shield, and AWS WAF`

- As `network traffic comes into your applications`,` AWS Shield` uses a variety of `"analysis techniques "` to detect `potential DDoS attacks in real time and automatically mitigates them`


# <ins> AWS KMS (AWS Key Management Service) and SSL (Secure Socket Layer) </ins> #

- `We also talked about encryption. In AWS, you are the owner of your data and you are responsible for it's security`

- `That means you need to pay attention to encryption, in transit and at rest.`

# <ins> Summary </ins> #

- `There are lots of considerations when dealing with security in AWS.`

- `Security is AWS's top priority and will continue to be so`

- `Please make sure you read the "documentation" on "securing your AWS resources" , as it does vary from service to service.`

- `Use the least privilege principle when scoping permissions for users and roles in IAM.`

- `encrypt your data at every layer, both in transit and at rest` 

- `make sure you've used AWS services to protect your environment.`



