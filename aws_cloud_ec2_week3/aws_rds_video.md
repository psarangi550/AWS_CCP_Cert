# <ins> Amazon Relational Database Service (Amazon RDS) </ins> #

- You're storing `data about your coffee` shop in `various systems`'

- but you're `finding that` you `need to maintain` `relationships between various types of data`. By `relationships`, I mean, if say, `a customer orders the same drink multiple times, maybe you want to offer them a promotional discount on their next purchase`

- You need `a way to keep track of this relationship somewhere`

- In this case, it's `best to use a relational database management system or RDBMS.`

- Essentially, it `means we store data in a way such that it relates to other pieces of data. `

- For example, if we had a `customer entry or record`, `we store that in a customer table`. We then could have an `entry for their physical address`, which we store in a corresponding `address table`

- We then `relate the two via a common attribute and can query the data that is housed in both tables`

- The most `common way to query` the data is by `writing queries in SQL`. This `runs on a variety of database systems.`

- Speaking of `database systems`,` what are some of the more well-known ones that AWS supports?` Well, there's `MySQL, PostgreSQL, Oracle, Microsoft SQL Server, and many more.`

- If you have an `on-premises environment`, you're `probably running one of those and they're most likely housed in your data center.`

- But is there a way to easily move them to the Cloud? 

    - Well, the simple answer is yes.

    - You `can do` what `we call a lift-and-shift` and `migrate` your `database to run on Amazon EC2.`

    - This means `you have control over the same variables you do in your on-premises environment`, `such as OS, memory, CPU, storage capacity, and so forth`

    - It's a `quick entry to the Cloud ` and you `can migrate them using standard practices` or `using something like database migration service`

- The `other option for running your databases in the cloud` is to `use a more managed service called Amazon Relational Database Service or RDS`

- It `supports all the major database engines, like the ones we mentioned earlier`, but `this service comes with added benefits.`

- These include

    - `automated patching`

    - `automated backup`

    - `automated redundancy`

    - `automated failover`

    - `automated disaster recovery `

    which need to manage iof we are not using the `AWS RDS Service`

- This makes it an `extremely attractive option to AWS customers as it allows you to focus on business problems and not maintaining databases.`

- Which if you're a `database admin`, can be `pretty time-consuming and difficult`

- How do we make it `even easier for you to run database workloads on the Cloud?` 
    
    - Well, we `go one further and have them migrate or deployed to Amazon Aurora`
    
    - it's our` most managed relational database option` and `comes in two forms`, 
        
        - MySQL
        
        - Postgres

-  its price is one-tenth the cost of commercial-grade databases , That's a pretty cost-effective database

- The `other benefits are things like` 
    
    - `your data is replicated across facilities`

    - `you have six copies at any given time`

    - You can also `deploy up to 15 read replicas`

    - `you can offload or dump your reads and scale performance`

    - Additionally, t`here's continuous backups to S3 so you always have a backup ready to restore.`

    - You also get `point-in-time recovery`, you can `recover data from a specific period`

