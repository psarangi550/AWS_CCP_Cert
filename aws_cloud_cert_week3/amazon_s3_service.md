# <ins> Amazon Simple Storage Service (Amazon S3) </ins> #

-  `Amazon Simple Storage Service, or Amazon S3` which is a `storage service` and its `simple`

- `Most businesses` have `data` that `needs to be stored` somewhere. F`or the coffee shop`, this could be `receipts`, `images`, `Excel spreadsheets`, `employee training videos`, and `even text files, among others`

- `Storing these files` is `where` `Amazon S3 comes in handy` because ` Amazon S3 is a data store` that `allows` you `to "store and retrieve" a "virtually unlimited amount of data" at any scale`

-  `Data is stored as objects` , but `instead of storing them in a file directory, you store them in what we call buckets.`

- `Think` of a `file sitting on your hard drive. That’s an object.` And `think of a file directory. That’s a bucket`

- The `maximum object size that you can upload is 5 TB`

-  You can `also version the objects` to `protect them from accidental deletion`, What this means is that `you always retain the previous versions of an object`, like a `paper trail`.

- Firstly `You can even create "multiple buckets" and "store those buckets across different classes or tiers of data" `

- Secondly You can then `create permissions to limit who can see or even access objects.`

- we can even `stage the data` between `different Tiers`

- These `Tiers offer` `mechanisms` for `different storage use cases`

- `such as data that needs to be accessed frequently compared to, audit data that needs to be retained for several years`

- Let's go through the notable ones. 

    - **S3 Standard** 

    - The `first storage class` is called `S3 Standard` and `comes with 11 nines of durability`

    - That means an `object` `stored in S3 Standard class or Tier ` `has a 99.999999999 percent probability` that `it will remain intact after a period of one year`,That's pretty high.

    - This is because `data or object` is `stored in at least three facilities` , So `multiple copies reside across locations`

    - Furthermore, `data or object` is `stored` in `such a way that` `AWS can sustain the concurrent loss of data in two separate storage facilities`

    - `Another useful way to use Amazon S3 is static website hosting`

    - where a `static website is a collection of HTML files and each file is akin/similar to a physical page of the actual site`

    - You can do this by `simply uploading all your HTML`, `static web assets`, and` so forth` `into a bucket` and` then checking a box to host it as a static website.`

    -  You can then `enter the bucket's URL and bam! Instant website`

    -  we say static, `but that doesn't mean you can't have animations and moving parts to your website.`

    -  That’s a pretty awesome way to start up that coffee blog

        
    - **S3 Standard-Infrequent Access or S3 Standard-IA**
    
    - It’s used for `data that is accessed less frequently` but `requires rapid access when needed`

    - This means it's a `perfect place to store backups, disaster recovery files, or any object that requires long-term storage.`

    - **S3 Glacier Flexible Retrieval**

    - `S3 Glacier Flexible Retrieval` Another `storage class or tier` lends `itself to that example we had earlier about audit data`

    - `if we need to retain data for several years` for `auditing purposes`. And` we don't need it to be retrieved very rapidly`

    - Well, then you can use S3 Glacier Flexible Retrieval to archive that data.

    - To use `S3 Glacier Flexible Retrieval`, you can `simply move data to it`, or` you can create vaults and then populate them with archives`

    - if you have `compliance requirements` around `retaining data` `for, say, a certain period of time`, you can `employ an S3 Glacier vault lock policy` and `lock your vault` where the `data will be saved as archives inside the vault with vault policy`

    - While defining the `vault lock policy` You can `specify controls such as write once, read many, or WORM(Write Once Read Many)`, inside `vault lock policy` and `lock the policy from future edits.`

    - `Once locked, the policy can no longer be changed`

    - You also have `three options for retrieval` data from the `S3 Glacier Flexible Retrieval`

        - These range from `minutes to hours`

    -  you have the `option of uploading directly to S3 Glacier Flexible Retrieval` or using `S3 Lifecycle policies.`

    - **S3 Lifecycle policies**
    
    -  we mentioned lifecycle policies up until this point

    - But they are `policies you can create that can move data automatically between tiers`

    - For example, say `we need to keep an object in S3 Standard for 90 days,` and then `we want to move it to S3 Standard-IA for the next 30 days.` Then after 120 days total, `we want to move it to S3 Glacier Flexible Retrieval`

    - `with Lifecycle policies`, `you create that configuration without changing your application code`, and `it will perform those moves of object for you automatically`


- `There are also other storage classes` like below that you can use.
    
    - `S3 One Zone-Infrequent Access `
    
    - `S3 Glacier Instant Retrieval`
    
    - `S3 Glacier Deep Archive` 