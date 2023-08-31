# <ins> Amazon Elastic File System (Amazon EFS) </ins> #

- Next up on the list of `storage services` is `Amazon Elastic File System` or what we call `EFS`

- `EFS` is a `managed file system.`

- It's extremely `common for businesses` `to have shared file systems across their applications`

- For example, `you might have multiple servers i.e EC2 instances running analytics` on `large amounts of data being stored in a shared file system`

- This `data traditionally has been hosted on premises`. 

- In this `on premises data center`, you `would have to ensure that the storage you have can keep up with the amount of data that you are storing`

- `Make sure backups are taken` 

- that the `data is stored redundantly i.e in a way unnecessary because it is more than is needed`, as well as `manage all of the "servers hosting that data"  `

- Luckily, `with AWS`, `you don't need to worry about buying all of that hardware` and `keeping the whole file system running from an operational standpoint`

- ` With EFS`, you can keep `existing file systems in place`, but` my AWS do all the heavy lifting of the scaling and the replication.`

- `EFS allows you to have multiple instances, accessing the data in EFS at the same time.`

- `It scales up and down as needed, without you needing to do anything to make that scaling happen.`

- `Well, you might be thinking, Amazon EBS also lets me store files that I can access from EC2 instances`

# <ins> Difference Between the AWS EBS and EFS </ins> #

- The answer is really simple.

- `Amazon EBS volumes attached to EC2 instances and are in "availability zone level resource" which is not a regional construct`

-  In order to `attach EC2 to EBS`, `you need to be in the same AZ`

- you can `save files on it you can also run a database on top of it or store applications on it. `

- `It's a hard drive.`

- If you `provision a 2 terabyte EBS volume` and `fill it up`, `it doesn't automatically scale to give you more storage. So that's EBS.`

- But in case of `EFS` , Amazon `EFS` can have `multiple instances reading and writing from it at the same time`

- but `it isn't just a blank hard drive that you can write to.`

- It is a `true file system for Linux`

- `It is also a regional resource which is a regional construct`

- `meaning any "EC2 instance in the region" can write to EFS file system`

- `As you write more data to EFS, it automatically scales. No need to provision anymore volumes`