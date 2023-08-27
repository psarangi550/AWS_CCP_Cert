# <ins> Messaging and Queueing in AWS </ins> #

- In the `coffee shop` example there are `order taking` which is known as `cashier` and `order making` which is known as `barista`

- when  `cashier` got the order it will `write the order` and deliver it to the `barista` to make the order , this will work well when the `cashier and barista` are in `sync` , but lets suppose the `barista` not available then in that case `cashier` takes the order but there were no one to `receive the order` then the `cashier` stuck with the order as there re `no barista` which can lead to `drop the order` if the cashier need to serve next customers

- this can lead to fail in `receiving the order` even `completing the order` as well

- this is known as the `tighly coupled system` when `one application` send messaage to another `application` to be processed , where a `single point of failure` can lead to `cause the problem in other system eventually in the whole system` which is the `hallmark trade of tighly coupled architecture`

- but we need to make our architecture as `lossely coupled` which is `loosely coupled` where `single point of failure` will not cause the `cascading failure`

- for that we can create some kind of `buffer` such as `ordering board` where we can enlist the `order` and barista can refer to that which is known as `Messaging and Queuing`

- similarly when we are 2 application which communicate with each other if one of application is unavbaiable which can cuse the ` whole system to fail`

- we can intoduce the `messaage queue` which `hold the request` like a `buffer` and `pass on to the other appllication` in order to process that `request`

- even though we have `one of the application` unavailable we have the `request` piled on without failing the `first application`

- once the `application been backed on` then those `p[ending request` can be processed 

- for this `AWS` provide 2 Services which can help in this `loosely couple` architecure 

    - Amazon Simple Queue Service (SQS)

    - Amazon Simple Notification Service (SNS)

- the `Amazon SQS` is just a `message queue` which can  

    - send message
    
    - store message

    - receive message

    between software component over any volume between Two application 

- this will work `if other services` should not be available

- this will help in `not loosing message`

- in the `coffee example` the `order` are` messages/request ` and `order board` is the `Message Queue` same as `Amazon SQS`

- the `data` that reeside inside the `message` are known as the `payload` and it is `protected` untill the `delivery`

- `Amazon SQS` provide the `platform` where messages can be `stored` until `they are processed` where the `underlying infrastructure` handled by `AWS` itself

- `Amazon SQS` provide the `oppertunity to host the Message Queue where the infrastructure been handled by AWS which make it more reliable` where `messages can be stored until they are delivered especially payload which is the (data under the payload)`

- the `Amazon SNS` which can perform 2 action 

    - send message to to the incoming service

    - also send notification to `endpoint/endpoint` which can be `Amazon SQS service` , `http /https web hooks` , `AWS lambda function`

    - we can also send notification to mobile using the `mobile push / email /sms`

- here the `Amazon SNS` works on the `publish subscribe model` which is known as the `pub-sub` model

- the `SNS topic` is just a `channel` we can communicate `messages` from `one service` to `another service` which can be `configured`

- once the `application been process the request` we can send the `messages` to a `topic/channel` which can `fan out the info` all the `subscriber of the topic`




