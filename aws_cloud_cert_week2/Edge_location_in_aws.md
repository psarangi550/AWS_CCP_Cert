# <ins> Edge Location in AWS </ins> #

- The `AWS global infrastructure` Help to `serve our customer` in a better way

- Whenever we are selecting the `AWS Region` one of the `Key Business Factor` is to have `close proximity to the customer location`

- But `what if we have customer all around the World or Customer Location City where the AWS region is not available`

- Like  in the `coffee shop example` we have `Lets suppose our coffee shop in a new location / new city which is doing good` but if we want to `serve customer in different Area` then we don't need to create the `entire headquarter infrastructure` rather we can serve using the `satellite Store` in order to `deliver customer`

- similarly for IT solution if we have `customer based on mumbai` and `but the application/ data / content` present in `tokyo region` then we need not have to `customer request for the data from tokyo each time`

- rather than that we can have `copy of the Tokyo region inside the Mumbai region` or `we can cache a copy of the data from tokyo location into the mumbai location`

- this process of `caching copy of the data /video / content` from `one location to another location (near to your customer location )` help in getting the `customer serve in a better way` which is known as `Content Delivery Network or CDN's` in case of `AWS` it is known as `AWS cloud front`

- using the `AWS cloud Frot` which is a `CDN Service` we can deliver the `application/data/video/content/API to customer all around the world` with `High transfer Speed and low latency`

- The **AWS cloud front** uses the `AWS Edge Location all around the world` in order to `deliver the high quality data/video.app/api/content to all the user no matter where they are`

- The `AWS Edge Locations` are different from the `AWS regions` 

- we can push the `data/app/api from one AWS region` to multiple `AWS edge location near to your customer location all around the world` to `accelarate the communication to the customer and content delivery`

- Unlike the `AWS region` we can have multiple `Edge Location` in order to `communicate the data present in the AWS region to Edge Location` to communicate the `customer all around the World`

- the `AWS Edge Location` will not only work for the `AWS cloud front service` also provide support to `Aws Edge Location can run AWS Domain Name Service known as Route 53`

- This `DNS Name Service which is AWS route 53 ` will help in `redirect the direct customer` to the `correct web location` with `very low latency`

- But lets suppose we want the `AWS service` we want to available to `on premises data center inside their own building` then in that case `AWS Outposts` which can help in `installing the mini AWS region inside our data center which will be own and managed 100% by AWS by using 100% of AWS functionality but will remain isolated within our data center premises`

- This is not a `solution` most customer needs but of neede then thhose services are still there

- But if we have problem suchas `our data should not leave the premises` then in those cases we can use the `AWS Outpost` which will install the `AWS mini region which will be there managed and operated with 100% AWS functionality by AWS `  

- `AWS Region` are geographically `isolated areas` where we can store the `AWS serviuces` which will run the `enterprioses`

- `AWS regions` are constructed based on `Availabilty Zone or AZ` which can be `separated from each other by tens of miles with low latency` in order for `disster management`

- `We can run services` from `physically separated  Availabilty zones` but bind `application/content/data` together `logically unified`

- the `availabilty zone i.e AZ ` will help you too solve the `high availability` and `disaster recovery` without `any effert from our end`

- `AWS Edge location help the AWS cloud front` for the `content Delivery Network` to deliver the `content with low latency and high transfer speed` to `customer any part in the world`

- `An edge location` `is a site` that` Amazon CloudFront uses to store cached copies of your content` c`loser to your customers for faster delivery.`

- Suppose that your company’s data is stored in Brazil, and you have customers who live in China. To provide content to these customers, you don’t need to move all the content to one of the Chinese Regions.

- Instead of requiring your customers to get their data from Brazil, you can cache a copy locally at an edge location that is close to your customers in China.

- When a `customer in China` `requests one of your files,` `Amazon CloudFront retrieves the file from the cache in the edge location` and delivers `the file to the customer.`

- The file is delivered to the customer faster because it came from the edge location near China instead of the original source in Brazil.