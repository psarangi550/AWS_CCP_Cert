# <ins> User Permission and Access </ins> #

- `In the coffee shop, every employee has an identity`

- `They come into work in the morning, and they log into the system to clock in`

- `use the registers, and manage the systems running the coffee shop day-to-day`

- `We have the cash register and a computer is helping run the whole operation`

- `Each person has unique access to these systems based on who they are.`

- ` If I have Rudy at the register taking orders `

- `Blaine in the back checking on the "inventory levels on the computer" `

- `they have two different logins and two different sets of permissions`

- `Rudy can run the cash register, but if you went to log into the inventory system, he wouldn't be allowed to do that.`

- `You will want to scope your user's permissions in AWS  in a similar way`

- `When you create an AWS account, you are given what is called the root account user.`

-` This root user is the owner of the AWS account`

- `has permission to do anything they want inside of that account.`

- `This is like being the owner of the coffee shop. In this situation`

- `let's say I am the owner of the coffee shop. `
    
    - `I can come into the shop and use my credentials to work the register, work the inventory system, or any other system in the coffee shop.`

    - `I cannot be restricted.`

- `With the AWS root user, you can access and control any resource in the account`

- You can 
    
    - `spin up databases`

    - `EC2 instances `
    
    - `block-chain services`
    
    - `literally whatever you want`

- `Because that user is so powerful, we recommend that as soon as you create an AWS account and login with your root user, you turn on multi-factor authentication or MFA, to ensure that you need not only the email and password but also a randomized token to log in.`

- `That is great, but even with MFA turned on, in reality, you don't want to use the root user for everything.`

- `I as the coffee shop owner, don't give my level of access to all employees.`

- `Rudy on the cash register cannot access the inventory system, remember`

- You i.e `root or owner` `control` `access` in a `granular way` by `using the AWS service`, `AWS Identity and Access Management, or IAM.`'

# <ins> IAM User </ins> #

-  `In IAM, you can create IAM users.`

- `When you create an IAM user, by default, it has no permissions.`

- `The user can't even log in to the AWS account at first`

- `It has absolutely zero permissions`

- ` It cannot launch an EC2 instance. It cannot create an s3 bucket`

- `You have to explicitly give the user permission to do anything in that account`

- Remember, by default, all actions are denied

- You have to explicitly allow any action done by any user

- You give people access only to what they need and nothing else.

- This idea is called the least privileged principle

- `The way that you grant or deny permission` is to `associate` what is called an `IAM policy to an IAM user`

- An IAM policy is a JSON document that describes what API calls a user can or cannot make

- Let's look at this quick example.

    - In this example, you can see we have a `permission statement`

        - `with Effect as "Allow" `

        - `Action as "s3:ListBucket"`

        - `Resource as "unique ID of the S3 Bucket"`

        ```
            IAM POLICY JSON
            ---------------

            {

                "Version": "2012-10-17", // date
                "Statement" :{
                    "Effect": "Allow/Deny", // Allow or Deny
                    "Action":"s3:ListBucket", // (can be a List) ANY AWS API call (which is to the s3 Bucket in this case)
                    "Resource": "arn:aws:s3:::coffee_shop_report" // Resources to Render on Specific API Call here it is the unique ID for the s3 bucket which the API call been happening in Action section (can be a List)
                }

            }
        
        
        ```

- If I attach this policy to a user and that user could `view the bucket` `coffee shop reports` , but can't perform no other actions on this `AWS account `

- There are only two potential options through the Effect on any policy

    - `Allow`

    - `Deny`

- For `Action`, you `can list any AWS API call`

- `Resource`, `you would list what AWS resource that specific API call is for`


# <ins> IAM Group </ins> #


- Now, as a `business person`, `you wouldn't need to write these policies`, but `they are used all over in your AWS accounts`

- `One way to make it easier to manage your users and their permissions` is to `organize them into IAM groups`

- Groups are, well they are groupings of users

- You can attach a policy to a group and all of the users in that group will have those permissions. 

- If you have a bunch of cashiers in the coffee shop, instead of individually granting them all access to the register

- instead you can grant all cashiers access, then just add each individual cashier to the group.

- Same idea with groups in IAM

<br/> <br/>

- All right. So far with IAM, you have the root user. They can do anything.

- You have users which can be organized into groups.

- You also have policies, which are documents that describe permissions that you can then attach to users or groups.

- There is `one other major identity` in `IAM`, and `it's called a role`


# <ins> IAM Role </ins> #

- `To understand` the `idea of roles`, let's `think about the coffee shop`

    - As we know, Blaine works in the shop,

    - depending on the staffing of the shop day-to-day

        - he might work the register

        - he might work the inventory system 

        - he might be the one cleaning up at the end of the day with access to no systems

    - `I as the owner`, `have the authority` to `assign these different roles to Blaine`

    - once `granted` the `different roles` His `responsibilities and access` are `variable and change` from `day-to-day`

    - `Just because he worked on tracking inventory in the system yesterday, doesn't mean that he should be at any time`

    - `His "role at work changes" and is temporary in nature`

    - `The same type of idea exists in AWS`

    - You can `create identities` in `AWS` that are `called roles`

    - `Roles have associated permissions` which help in  `allow or deny specific actions`

    - these `roles can be assumed for temporary amounts of time`

    -  It is `similar to a user, but has no username and password.`

    - Instead, `it is an identity` that you can assume `to gain access to temporary permissions` i.e it can `gain access to temporary permission`

    -  You `use roles to `
            
        - `temporarily grant access to AWS resources to users`

        - `temporarily grant access to AWS Resource to external identities`

        - `temporarily grant access to AWS Resource to  applications`

        - `temporarily grant access to AWS Resource to  other AWS Service`


    -  When the `identity` is `role` then it `abandon` all the `previous permission  it has` consider only the `permission of that role`


- `You can actually avoid creating IAM users for every person in your organization by federating users into your account. `

- This means that they `could use their regular corporate credentials` `to log in to AWS` by `mapping their corporate identities to IAM roles.`

- AWS IAM, `authentication and authorization` as a service.


