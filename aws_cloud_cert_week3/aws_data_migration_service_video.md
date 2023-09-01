# <ins> AWS Database Migration Service (AWS DMS) </ins> #

- We've been `talking about databases` and the `various database options on AWS`

- But `what happens` if `you have a database` `that's on premises or in the cloud already`

- Does that mean you have to `start from scratch? Or does AWS have a magical way to help you migrate your existing database?`

- Thankfully `AWS offers a service` called `Amazon Database Migration Service`, or `DMS`, `to help customers do just that`

- `DMS helps customers` `migrate existing databases` `onto AWS ` `in a secure and easy fashion`

- You `essentially migrate data between a source and a target database.`

- The `best part is that the source database remains fully operational during the migration, minimizing downtime to applications that rely on that database`.

- Better yet is that `the source and target databases don't have to be of the same type`

- `These migrations are known as homogeneous`

    - `can be from MySQL to Amazon RDS for MySQL`

    - `Microsoft SQL Server to Amazon RDS for SQL Server`

    - `even Oracle to Amazon RDS for Oracle`

- The process of `data migration` is fairly straight forward

- Since 
    
    - `schema structures `
    
    - `data types`
    
    - `database code `
    
    is compatible between source and target

-  the `source database `can be located 
    
    - `on premises `
    
    - `running on Amazon EC2 instances`
    
    - `it can be an Amazon RDS database`

- The target `itself can be a database` in `Amazon EC2 or Amazon RDS`

- `In this case` you `create a migration task` with `connections to the source and target databases.`

- Then start the migration with the click of the button , `AWS database migration service` takes `care of the rest.`

- `The second type of migration occurs when source and target databases are of different types`

-  This is called `heterogeneous migration` and `it's a 2-step process`

-  Since the `schema structures, data types, and database code` are `different` `between source and target`

- we `first need to convert them using `the `AWS schema conversion tool`

    - This will convert the `source schema and database code` to` match that of the target database`

    - `The next step` is then to `use DMS`` to migrate` `data from the source database to the target database.`

    - `But these are not the only use cases for DMS.`


# <ins> Other Use Case of AWS Database Migration Service (AWS DMS) </ins> #

- Others include

    - Others include `development and test database migrations`

        - `Development and test migration` is `when` `you want to develop this to test against production data`, but `without affecting production users.`

        - `In this case` you use `DMS` `to migrate`` a copy of your production database to your dev or test environment`. Either `once off or continuously.`

    - database consolidation

        - `Database consolidation` is `when` you have `several databases` and `want to consolidate them into one central database`

    -  even continuous database replication

        - Finally, `continuous replication` is `when` `you use DMS to perform continuous data replication`

        - This could be for `disaster recovery or because of geographic separation`

            

