# <ins> Regions </ins> #

- To understand `AWS Global Infrastructure` we need to understand  `fundamental of business need`

    - we need to our application for  business which can be for 

        - `content to be stored `

        - `data to be analyzed`

        - `application to be run`

        - basically `stuff` to `live and operate somewhere`

    - `Business need to run the application` in their `own data center`

    - But with the help of `AWS` company can run the `application` inside the `data center` managed by `AWS` which is not `own by the business`

    - but the `fundamental problem with data center` is that `event can occure` in which we can `lost conection` to `data center building`

    - if we are running our `own data center` we need to look to answer the question `how to handle if a disaster strike in the building`

    - we could run a `second Data center` but the `real estate can be problem` and also we need to handle the `expenses on`

        - `duplicate electricity`

        - `duplicated employee`

        - `duplicate hardware`

        - `duplicate heating and cooling system`

        - `duplicate security`

    - `Most of the cases` we need to `store the backup data` and expecting/hoping the `disaster never happen`

- in case of `AWS` the `datacenters were planned in a group known as ` regions , when the disater strike by building for a `Large group of data center or region` then

- in `AWS` cases the `regions were created` where `business traffic need it` it can be in `located in`

    - `Paris`

    - `Tokyo`

    - `San Paulo`

    - `Dublin`

    - `Ohio`

- inside the `region` which is a `large group of data center` we have all the `compute and storage inside the multiple data centers inside the region` to run `your application`

- Each `region connected to another region` using the `high speed fibre network controlled by AWS` which is a `global operation from corner to corner if needed to be`

- `Businesss Owner` need to make sure which `region` they want to `run their business`

- `Each region is isolated from another region` so that `no data can be tranfered in and out between the region` until we explicitly provide `permission to  export the data`

- we might have `compliance requirement (by goverment) that the data should not leave a specific region` which comes in `AWS` out of the `box`

- `data in one region will not leave the region untill the  permission provided explicitly`

- we need to provide the `permission and right user credetional explicitly` in order to `move/export the data in and out betweeen one region to another region explicitly`

- `regional data sovrinity` is the key to `develop the region on AWS` where `data being subjected to the local law or statutes of the country where the region lives`


- `data lives inside the region` are `subjected to local law ot statutes of the region where it lives in`

- while choosing the `data` inside the `AWS region` we need to take care of `4 key Business factor` while choosing the `AWS region`

- When `determining the right Region` for your ser`vices, data, and applications`, consider the following` four business factors`. 

    - `compliance`

        - Depending on `your company and location`, you might need to `run your data out of specific areas`

        - before anything we need to look for the `compliance requirements` whether the `data inside the region should be available within the country regionor not`

        - if so we need to choose that specific `region`

        - `Most Business` were not run by such `compliance requirements or regulatory control`

        - if we don't have `compliance requirements or regulatory control` then we can look for other option

    - `proximity`

        - then we need to choose as per the `proximity` i.e how close the `region is to the business need`

        - `Selecting a Region` that is `close to your customers` will help you to `get content to them faster.`

        - because if we are choosing some other region there might be case of `latency` as the time could be taken to `send and receive the data`

        - this process of `time taken send and receive the data` is known as `latency`

        - because `quantum network spped` still `long way away`

        - if `most of the customer is based on singapore` then `we should choose the region as singapore`

        - we can choose other region but can `cause some delay while send and receive data time` which is known as `latency`

        - locating `region` near the `customer base` is usually the best call

        -  For example, `your company is based in Washington, DC, `and many of your `customers live in Singapore`. You might consider` running your infrastructure in the Northern Virginia Region` to be `close to company headquarters`, and `run your applications from the Singapore Region.`


    - `feature availablity`

        - sometimes the `closest region` might not have `all the feature you need`

        - `AWS` deploy multiple `new feature or services` in a year which can take `few days` in order to `build the hardware for those service` in that `region`

        - may be `due to the hardware requirement for the brand new service` for that `all services not available on all region`

        - but it's a `good assumption` that we can have `that those services will be available on the region eventually`

        - lets suppose the `Amazon Bracket` which is used for the `quantum computing platform` might not be `available in all region`

        - But we can run these `service` in those region `where hardware for that service already being build on`

    - `pricing`

        - Even though the `hardware being` same from `one region to another region` but their `pricing being different to operate the region`

        - The `hardware component on Brazil San Paulo` being higher due to `Tax Rules in Brazil` , which can be `50% more to run` compared to the `oregano united state`

        - then in that case we can choose `some other region where we can get it for cheap`

        - Each `region` has a different `pricing sheet`

        - if `price is the primary motivation` then we can `run the application in a region which is cheaper compare to the specific region`

        - Suppose that you are `considering running applications in both the United States and Brazil`. The way Brazil’s tax structure is set up, `it might cost 50% more to run the same workload out of the São Paulo Region compared to the Oregon Region`. You will learn in more detail that several factors determine pricing, but for now know that the` cost of services can vary from Region to Region.`



