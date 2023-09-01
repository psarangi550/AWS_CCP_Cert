# <ins> Amazon DynamoDB </ins> #

-  At its most basic level, `DynamoDB is a database`

- It's a `serverless database`, `meaning` `you don't need to "manage the underlying instances or infrastructure powering it." `

- With `DynamoDB`, `you create tables.`

- A `DynamoDB` `table is just a place where you can store and query data`

-  `A table in DynamoDB is a collection of items` and `where each item represents a data record`

- `Data is organized into item` in `Dynamo DB` and  `items have attributes.` 

-  `Each item can have a different structure`, `similar to MongoDB documents within a collection.`

- `Attributes are just different features of your data.`

- `If you have one item in your table or 2 million items in your table, DynamoDB "manages the underlying storage" for you.`

- `You don't need to worry about the "scaling of the system up or down"`

- `DynamoDB "stores this data redundantly" across "availability zones" `

- DynamoDB stores this data redundantly across "availability zones"  ` near the data across multiple drives under the hood for you`

- `This makes the burden of "operating a highly available database" much "lower" `

- DynamoDB,` beyond being massively scalable, is also highly performant`

-` DynamoDB has a millisecond response time`

-` Dynamo DB useful in case When you have applications with potentially millions of users`, having `scalability and reliable  and lightning-fast response times is important`

- `Now, DynamoDB isn't a normal database in the sense that it doesn't use the very widely used query language, SQL `

# <ins> Problem With Relational Database </ins> #

- `Relational databases`, like a `standard MySQL database`, require that you have a `well-defined schema` in place `that might consist of one or many tables that might relate to each other`

- `You then use SQL to query the data`. This `works great for a lot of use cases` and `has been the standard type of database historically`

- However, `these types of rigid SQL databases` `can have "performance and scaling issues" when "under stress" `

- The `rigid schema` also `makes it so that you can not have any variation in the types of data that you store in a table.`

- It `might not be the best fit for a dataset` `that is a little bit less rigid and is being accessed at a very high rate`

- `This is where non-relational or no SQL databases come in`


# <ins> Advantage of Non Relation or No-SQL Database </ins> #


- `DynamoDB is a non-relational database.`

- `Non-relational databases` `tend to have` `simple flexible schemas`, `not complex rigid schemas` `laying out multiple tables that all relate to each other.`

- `With DynamoDB, "you can add and remove attributes from items in the table" at any time.`

- `Not every item in the table has to have the same attributes`

-  `This is great for datasets` `that have some variation from item to item.`

- `Because of this flexibility, you can not run complex SQL queries on it.`

- `You would write queries` `based on a small subset of attributes that are designated as keys`

- `Because of this, the queries that you run on non-relational databases tend to be simpler` and` focus on a collection of items from one table, not queries that span multiple tables`

-  This `query pattern`, along with `other factors`, including the way `that the underlying system is designed`, allows `DynamoDB to be very quick in response time and highly scalable.`

# <ins> Things To Remember </ins> #

- `DynamoDB is a non-relational NoSQL database`

- It is `purpose-built`, meaning `it has specific use cases`, and `it isn't the best fit for every workload out there`

- `It has millisecond response time`

- `It is fully managed`

- `it's highly scalable`

- `One awesome example is on Prime Day in 2019`. Across the `48 hours of Prime Day`, there were` 7.11 trillion calls to the DynamoDB API,` peaking at `45.4 million requests per second`

- `That's insanely scalable.`

- `All without the underlying database management.`