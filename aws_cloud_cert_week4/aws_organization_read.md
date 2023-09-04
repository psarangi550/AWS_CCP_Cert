# <ins> AWS Organizations </ins> #

- `AWS Organizations`

    - Suppose that `your company has multiple AWS accounts`

    - You can use `AWS Organizations` to `consolidate and manage multiple AWS accounts` ` within a central location`

    - When you `create an organization`

        - `AWS Organizations automatically creates a root`

        - `which is the parent container for all the accounts in your organization.`

    - In `AWS Organizations`, you can `"centrally control permissions for the accounts in your organization"` `by using` `"service control policies (SCPs)"` i.e it `handle` the `permission of the account within the AWS Organization using the service control policies or SCP`

    - `SCPs enable` you to `"place restrictions on the AWS services, resources, and individual API actions"` that `"users and roles in each account can access".` that means we can restrict the `AWS Service/Resource saying user can access only Limited AWS Services that been provisioned `

    - `In AWS Organizations, you can apply service control policies (SCPs) to the organization root, an individual member account, or an OU`

    - `An SCP affects all "IAM users, groups, and roles within an account", including the "AWS account root user".` 

    - `You can apply IAM policies to IAM users, groups, or roles. You cannot apply an IAM policy to the AWS account root user.`

    - `Consolidated billing` is `another feature of AWS Organizations`


# <ins> Organizational Units </ins> #

- In `AWS Organizations` , you can `group accounts into organizational units (OUs) `, to make it `easier to manage accounts` with `similar business or security requirements`

- When you `apply a policy to an OU`, `all the accounts in the OU automatically inherit the permissions specified in the policy. ` 

- By `organizing separate accounts into OUs`

    - `you can more easily isolate workloads or applications that have specific business and  security requirements`

    - For instance, `if your "company has accounts that can access only the AWS services that meet certain regulatory requirements", you "can put these accounts into one OU".`

    - `"Then, you can attach a policy to the OU"`

    - `blocks access to all other AWS services that do not meet the regulatory requirements.`


# <ins> Example: AWS Organizations </ins> #

- `Review an example of how a company might use AWS Organizations:`

    - `Imagine that your company has separate AWS accounts for `
        
        - `the finance `

        - `information technology (IT)`

        - `human resources (HR)`

        -  `legal departments`

    - `You decide to "consolidate these accounts into a single organization" so that "you can administer them from a central location" `

    - `When you create the organization, this establishes the root.`

    - `While designing your organization`, you consider the` business, security, and regulatory needs of each department`

    - `You use this information to decide which departments group together in OUs`

    - Lets suppose

        - `The finance and IT departments have requirements that do not overlap with those of any other department.`

        - `You bring these accounts into your organization to take advantage of benefits such as consolidated billing`

        - `you do not place them into any OUs.`

    - Lets Suppose

        - `The HR and legal departments need to access the same AWS services and resources`

        - `so you place them into an OU together.`

        - `Placing them into an OU enables you to attach policies that apply to both the HR and legal departments’ AWS accounts.`

        - `Even though you have placed these accounts into OUs`, you can continue to provide access for `users, groups, and roles` through `IAM`.

        - `By grouping your accounts into OUs, you can more easily give them access to the services and resources that they need`

        - `You also prevent them from accessing any services or resources that they do not need.`

    
