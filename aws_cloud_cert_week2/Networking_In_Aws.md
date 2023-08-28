# <ins>  Networking Aspect of AWS and VPC </ins> #

- Lets suppose in our `coffee shop` example which represent the `AWS cloud account` , we have `eager customer ` who want to communicate to the `barista` directly rather than the `cashier` up front which does not make very lot of sense as `barista` job is create `caffinated beverages` without worrying about `taking orders from customer`

- in this case we can use `Amazon VPC` which stands for `Amazon Virtual Private Cloud` which is an `logically isolated AWS cloud environment` where can `deploy our AWS resources` in a `virtual network` 

- these `AWS repurces` deployed onto the `virtual network as separate cloud` can be `public` if the `we want the services to have internet access ` or else `private` if we don't `want the services to have internet access` 

- in case of `DataBase or Backend Service` we can use the both the `public and private` Virtual Network which is known as `public or private subnet` having multiple range of `IP` in between them inside the `VPC`

- this will help in `sort` the `scenario` in the `coffee shop`

    - where we want `our customer to contact the cashier` which will be in a `public subnet` and we want our `customer to interact with the public subnet cashier`

    - the `barista` will be there in `private subnet` and `customer` will not have `direct access to the communicte to the AWS Resource (barista)` directly