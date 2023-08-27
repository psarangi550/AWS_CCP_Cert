# <ins> Amazon SNS Service </ins> #

- `Amazon Simple Notification Service (Amazon SNS)` is a `publish/subscribe` service

- Using `Amazon SNS topics, a publisher publishes messages to subscribers. `

- This is similar to the coffee shop; the cashier provides coffee orders to the barista who makes the drinks.

- In` Amazon SNS,` `subscribers can be web servers, email addresses, AWS Lambda functions, or several other options`. 

- the subscriber in the `SNS Topic` can be as below

    - `Web Server`

    - `email addresses`

    - ` mobile notification push`

    - `AWS Lambda functions`

- we can `Publishing updates from a single topic`

- Suppose that the coffee shop has a single newsletter that includes updates from all areas of its business. 

- The `Single News Settler` includes topics such as `coupons, coffee trivia, and new products.`

-  All of these topics are grouped because this is a single newsletter. All customers who subscribe to the newsletter receive updates about coupons, coffee trivia, and new products.

- After a while, some customers express that they would prefer to receive separate newsletters for only the specific topics that interest them. The coffee shop owners decide to try this approach.

- Now, instead of having a single newsletter for all topics, the coffee shop has broken it up into three separate newsletters. Each newsletter is devoted to a specific topic: coupons, coffee trivia, and new products.

- Subscribers will now receive updates immediately for only the specific topics to which they have subscribed.

- It is possible for subscribers to subscribe to a single topic or to multiple topics. For example, the first customer subscribes to only the coupons topic, and the second subscriber subscribes to only the coffee trivia topic. The third customer subscribes to both the coffee trivia and new products topics.