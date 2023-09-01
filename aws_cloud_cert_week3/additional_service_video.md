# <ins> Additional Database Services </ins> #

- Before `we wrap up databases and storage`, I want to look back to the topic that we started all this with

- `Choosing the right database, choosing the right storage platform`, to `fit your business needs`,

-  `rather than` `forcing your data to fit your databases requirements`

- `No matter what a database vendor might try to tell you`, `there is no one size fits all database for all purposes`

-  We've `covered quite a few database flavors already`, but `they're even more databases, AWS offers for special business requirements` that` we don't have time to cover`

-  `But it's worth just knowing they're there in case you need them`

- For example, `we talked about DynamoDB`, and that's `great for key value pair databases`

- `But what if you need more than just small attributes? What if you need a full content management system?`

# <ins> Amazon Document DB Database </ins> #

- Introducing `Amazon DocumentDB`, `great for` 
    
    - `content management `

    - `catalogs`

    - `user profiles`

# <ins> Amazon Neptune Database </ins> #

-  Now, `what if you had a social network that you wanted to track`

    - Well those `social webs`, `who is connected to who is very clunky to manage in a traditional relational database`

    -  so `Amazon Neptune`,` a "graph database" ` engineered for 
        
        - `social networking `
        
        - `recommendation engines `

        - `also great for fraud detection needs. `

        - `perhaps you have a supply, chain that you have to track with assurances that nothing's lost.`

    
- you have `banking or financial records` `that require 100 percent immutability`

- `some people will tell you, "Oh, that's what block chains all about.`

- Well, perhaps. Now `if you do need a blockchain solution`, wouldn't you know `it we offer Amazon Managed Blockchain,` but that's probably not what you really need here

- It `solves part of the equation`, but `adds a huge decentralization component`, that's` not what financial regulators want to see.`

- What you really need is an` immutable ledger. `

# <ins> Amazon QLDB or Quantum Ledger Database </ins> #

- `Amazon QLDB`, or `Quantum Ledger Database`, an `immutable system of record` `where any entry can never be removed from the audits`


- `Databases by themselves are great, but if there was a way to make them faster, wouldn't that be greater`

- `you know I wouldn't be saying that if there weren't some accelerator options that can be used in a number of unique scenarios.`

- `Starting with adding caching layers on top your databases, that can help improve the read times of common requests from milliseconds to microseconds.`


# <ins> Amazon ElastiCache </ins> #

- `Amazon ElastiCache`, can provide those `caching layers without your data team needing to worry about the heavy lifting of launching, uplift and maintenance.`

- `It comes in both Memcached D and redis flavors`

- `if you're using DynamoDB, try using DAX, the Dynamo DB Accelerator`

- `A native caching layer designed to dramatically improve read times for your non-relational data.`

- ` The key thing to understand is AWS wants to make sure that you're using the best tool for the job.`

