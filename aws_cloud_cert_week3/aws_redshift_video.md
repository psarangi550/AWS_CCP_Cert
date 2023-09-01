# <ins> Amazon Redshift </ins> #

- We just spent a lot of time discussing the `kinds of workflow` that `require fast, reliable current data`

- `Databases that can handle thousands of transactions per second`

- `storage that is highly available` and `massively durable`

- But sometimes `we have a business need that goes outside what is happening right now. To what did happen.`

- This `data analysis is the realm` of a `whole different class of databases.`

- Sure, `you could use the one size fits all` `model of` `a single database for everything`

- But `modern databases` that are `engineered for high speed real time ingestion and queries` `May not be the best fit`

- Let me explain, in order to `handle the velocity of real time read write functionality`. `Most relational databases tend to function fabulously at certain capacities`, `how much content it actually stores`

- `The problem with historical analytics` ,  `the Data` `that answers questions like` ,  `Show me how production has improved since we started is that "data collection never stops"`

- In fact, `with modern telemetry` and the` explosion of IoT`, the ` "volume of data" will "overwhelm" "even the beefiest traditional relational database", it gets worse`

-  `"Not just the volume", but the "variety of data can be a problem" `

- You want to run `business intelligence or BI projects` against `data coming from different data stores` `like your inventory`. 
    
    - `Your financial `
    - `your retail `
    - `your sale systems. `

- A `single query` against `multiple databases` `sounds nice` `but traditional databases don't handle them easily.`

- Once `data` `becomes too complex to handle` `with traditional relational databases`. `You've entered the world of data warehouses.`

- `Data warehouses` are `engineered specifically for this kind of big data` where you are looking at `historical analytics as opposed to operational analysis` i.e here we are looking for the `historical analysis not the current operational analysis `

- Now` let's be clear`, `historical`, maybe `as soon as show me last our sales numbers across all the stores` i.e here we are not using the `current time but time before now time`

- The `key thing` is the `data is now set.` `before` we ran the `historical analytics ` like `show me last our sales numbers across all the stores`

-  We're not selling anymore `from the last hour because that is now in the past. `

- Compare that question to `how many bags of coffee do we still have in our inventory` `right now which could be changing as we speak.`

- `As long as your business question is looking backwards at all, then a data warehouse is the right solution for that line of business intelligence.`

- `Now, there are many Data Warehouse Solutions out on the market. `

- `If you already have a favorite one, running it on AWS, it's just a matter of getting the data transferred. `

- `But beyond that, there may still be a lot of undifferentiated heavy lifting that goes into keeping a data warehouse tuned, resilient and continuously scaling.`


- `Wouldn't it be nice if your data warehouse team could focus on the data instead of the unavoidable care`

-  `feeding of the engine Introducing Amazon redshift. `

- `This is data warehousing as a service`

-  It's `massively scalable redshift nodes in multiple petabyte sizes`, very common

- In fact in `cooperation with Amazon redshift Spectrum. You can directly run a single SQL query against exabytes of unstructured data running in data lakes`

- But `it's more than just being able to handle massively larger datasets.`

- `Redshift uses a variety of innovations`, `that allow you to achieve up to ten times higher performance Than traditional databases` when `it comes to these kind of business intelligence workloads.`

- I'm not going to go into details of how the magic works , We have whole classes that you or your data teams can take that explain how it is built and why it can return such improved results.

- The `key for you is to understand` that `when you need big data bi solutions`, `redshift allows` you to `get started` `with a single API call.`

- `less time waiting for results, more time getting answers.`

