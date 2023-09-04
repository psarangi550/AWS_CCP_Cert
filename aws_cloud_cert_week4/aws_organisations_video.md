# <ins> AWS Organizations </ins> #

- With your first `foray/raid`  into the `AWS Cloud`, `you` `most likely` `will start with one AWS account and have everything reside in there` , Most people start this way

- but `as your company grows` or `even begins their Cloud journey`, it's `important to have a separation of duties.`

- For example

    - `you want your developers to have access to development resources`

    - `your counting staff able to access billing information`

    - `even have business units separate`  i.e `development Business Unit and accounting Business Unit` so that `they can experiment with AWS services `
    
    without affecting each other

- You `start to add more accounts for each person`, `whoever needs to onboard`, and `before you know it, you end up with a tangled bowl of AWS accounts spaghetti`

- Not as tasty as you might imagine.

-  For example, `you'll then have to keep track of account A, F, and G` `while` maybe `account B has the wrong permissions` and `account C has billing and compliance info.` 

# <ins> What is AWS Organizations </ins> #

- `One way to install order` and to `enforce` `who is allowed to perform certain functions in what account` is to `make use of an AWS service called AWS Organizations.`

- The `easiest way to think` of `Organizations` is as a `central location to manage multiple AWS accounts`

- You can `manage`

    - `billing` 

    - `control access`

    - `compliance`

    - `security` 

    - `shared resource` `across` the `AWS Account`


- Let's outline some of the main features of AWS Organizations, shall we? 

    - The first is `centralized management of all your AWS accounts.`

    - Think of `all those AWS accounts` we had,` A, B, C, F, G.` Now, `you can combine them into an "organization"` that `enables us to manage the accounts centrally`

    - Next up is `consolidated billing` for `all member accounts.` 

    - `This means you can use the primary account of your organization to consolidate and pay for all member accounts`

    - `Another advantage of consolidated billing is bulk discounts, cash money indeed`

    - The next feature is that you can `implement` `hierarchical "groupings of your accounts" ` to meet `security, compliance, or budgetary needs.`

    - This means `you can "group accounts into organizational units" or OUs` `like business units or BUs.`

    -  For example 
        
        - `if` you have `accounts` that `must access only the AWS services that meet certain regulatory requirements`, `you can put those accounts into one OU`

        - if you have `accounts that fall under the developer OU`, you `can group them accordingly.`

    - One of the `last main features will touch upon` is that `you have control over the AWS services and API actions that each account can access.` 

    - As an administrator of the primary account of an organization, you can use something called `service control policies or SCPs`

    - specify the `maximum permissions for member accounts` `in the organization` that we have `build by using the hierarchical grouping `

    -  you can `restrict a which AWS services, resources, and individual API actions `
        
        - `the users can enrolls`
        
        - `each member account can access`.