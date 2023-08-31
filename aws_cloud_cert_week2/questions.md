# <ins> AWS Questions for Week2 </ins> #

- `Amazon Virtual Private Cloud (Amazon VPC)` is a service that `enables you to provision an isolated section of the AWS Cloud`. 

- `In this isolated section, you can launch resources in a virtual network that you define.`

- A `subnet` is a `section of a VPC` in `which you can group resources` based on `security or operational needs`

- Subnets can be public or private.

- Public subnets contain resources that need to be accessible by the public, such as an online store’s website.

- `A public subnet is a section of a VPC that contains public-facing resources.`

- Private subnets contain resources that should be accessible only through your private network, such as a database that contains customers’ personal information and order histories.

- A` private subnet is a section of a VPC `in `which you can group resources that should be accessed only through your private network`. `Although it is private`, `it is not used for establishing a connection between a data center and AWS.`

- DNS stands for Domain Name System, which is a directory used for matching domain names to IP addresses.

- A `virtual private gateway` enables you to `create a VPN connection between your VPC and a private network`, `such as your company’s data center`. `Although this connection is private and encrypted, it travels through the public internet, not through a dedicated connection.`

- `Security groups are stateful`

- A `security group` is a `virtual firewall` that `controls inbound and outbound traffic for an Amazon EC2 instance.`

- `This means that they use previous traffic patterns and flows when evaluating new requests for an instance.`

- `By default, security groups deny all inbound traffic`, `but you can add custom rules to fit your operational and security needs.`

- `AWS Direct Connect is a service that enables you to establish a dedicated private connection between your data center and VPC.  `

- **Edge Location**

- An `edge location` `is a site` `that Amazon CloudFront uses` to `store cached copies of your content for faster delivery to customers.`

- **AWS CloudFront**

- `Amazon CloudFront is a content delivery service.` It `uses a network of edge locations` to `cache content and deliver content to customers all over the world.`