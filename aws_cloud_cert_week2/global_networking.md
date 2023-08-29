# <ins> Global Networking </ins> #

- Here we need to discuss `How your customer interact with AWS infrastructure on Which your application been hosted on` rather than `discussing how you are interacting with your AWS infrastructure`

-  when the `customer request for the website which been hosted on the AWS cloud` then they `just have to make the request to specific website on the browser and Specific page will be displayed`

- for the `website request` AWS uses `2 service` named as 

    - `AWS Route 53 Service` :-

        - `AWS Route 53 Service` is  a `DNS Service` which stands for the `Domain Name Server` which is a `translator` which `translate the website Name into IP address i.e Internet Protocol that the computer can understand` which can also refer as the `translation service`

        - `AWS Route 53` service is `Highly available and scalable`

        - When a `customer request for a webpage` like `https://aws.amazon.com` then the `the request comes to the Route53 Service` which then `translate the website Name into the IP address` which can render the `Webpage on the customer Web Browser`

        - `AWS Router 53 Service` also can `direct the traffic request to multiple endpoint` based on the `several routing Policy` and few of the `Routing Policy are of `

            - `Latency Based Routing Policy`

            - `Geo location DNS`

            - `Geo Proximity Routing Policy`

            - `Weighted Round Robin Routing Policy`

        - in case of `Geo Location DNS` whenever the `direct the traffic request based on Customer Location` `based on that geographic location of customer comes into consideration` request redirect to that `customer geographic location where the traffic been coming `

        - hence the `Traffic` coming from the `Seattle region` then the `request traffic redirect to the North America region to deliver the website from that location `

        - if the `customer request been coming from dublin` then `redirect to the Ireland Region to deliver the Website content accordingly`

        - we can also register `our custom domain name` while using the `AWS Route 53 Service` to use `our own purchased domain over the AWS cloud`

        - we can `buy the domain name` and manage it in the `AWS Route 53 Service`

    - `AWS Cloud Front Service` :- 

        - Another Service which can be very useful to ` speed up the deliver website asset to the customer` will be of `AWS Cloud Front Service`

        - The `AWS Cloud Front Service` uses the `Edge Location to deliver content to customer with low latency and high transfer Rate all around the World`

        - these `Edge Location` are `as close as possible` to the `customer location` to help deliver the `content very Fast`

        - it uses the `CDN or Content Delivery Network is a Network  Which help in Delivering the Edge Content on to the customer based on the geographic location of the Customer All Around the World`

        - the `CDN` is a part of the `Edge Location which deliver the Edge content to the customer as close as possible all around the World`

        - In this case if the `customer location / user  in seattle and the AWS cloud present in North America (Oregon region)` then in that case the `content will be delivered from the North America (Oregon) region where the Application been deployed with Website Asset such as images and gif in AWS CLoud front`

        - But Lets suppose we have also the `customer in ireland who is website data in that case making a call to North America Hosted AWS cloud can take long latency which is not favorable` in that case we can create a `AWS CloudFront CDN Network based on the Edge Location Near dublin ireland and Put all the static pages such as AWS and GIF into that AWS cloud Front cache Which is a duplication of the website Which is hosted in North America where the content being same but the content being deliver from ireland rather than North America (oregon region)` so it can deliver the Website content Faster with very Low Latency  







