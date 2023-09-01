# <ins> Instance Stores and Amazon Elastic Block Store (Amazon EBS) </ins> #

- When `you are using Amazon EC2` to `run your business applications`, `those applications need access to CPU, memory, network, and storage`

-  `EC2 instances give you access to all those different components` and right now, let's focus on the `storage access`

- `As applications run`, they will oftentimes `need` access to `block level storage.`

- You can think of `block level storage` as a `place to store files` 

- `a file` being a `series of bytes that are stored in blocks on disk (which is a series of block)`

- When a `file is updated`, the `whole series of blocks aren't all overwritten`. `Instead, it updates just the pieces that change` which `makes it an efficient storage type (block level storage)` when `working with applications like databases, enterprise software, or file systems`

- When you use your `laptop or personal computer`, `you are accessing block level storage.` `All block level storage is, in this case, is your hard drive.`

-  EC2 instances have hard drives as well. There are a few different types

- When you `launch an EC2 instance`, `depending on the type of the EC2 instance` you launched, `it might provide you with "local storage" called "instance store volumes" `

- These volumes are physically attached to the host your EC2 instance is running on top ,  you can write to it just like a normal hard drive.

- `The catch here` is that `since this volume is attached to the underlying physical host`, if `you stop or terminate your EC2 instance`, `all data written to the instance store volume will be deleted.`

- The reason for this is that if you start your instance from a stopped state, it's likely that EC2 instance will startup on another host.a host where that volume does not exist. 

- Remember, EC2 instances are virtual machines and therefore the underlying host can change between stopping and starting an instance

- `Because of` this `ephemeral or temporary` `nature of instance store volumes`, `they're useful in situations` where` you can lose the data being written to the drive`, such as       
    - temporary files 
    
    - scratch data 
    
    -  data that can be easily recreated without consequence

-  All right. I'm telling you not to write important data to the drives that come with EC2 instances. I'm sure that sounds a bit scary because obviously, you'll need a place to write data that persists outside of the life-cycle of an EC2 instance

-  We don't want our entire database getting deleted every time you stop an EC2 instance

- Don't worry, this is where a service called `Amazon Elastic Block Store`, or EBS, comes into play

- `With EBS`, `you can create virtual hard drives` that we call `EBS volumes` that `you can attach to your EC2 instances`

- `These are separate drives from the local instance store volumes` and they `aren't tied directly to the host that your EC2 is running on.`

- This means that the data that you write to an EBS volume can persist between stops and starts of an EC2 instance

- EBS volumes come in all different sizes and types

    - How this works is you define the size, type, and configurations of the volume you need

    - Provision the volume

    - attach it to your EC2 instance

- From there, you can configure your application to write to the EBS volume and you're good to go

- If you stop and then start this EC2 instance, the data in the volume remains.

- Since the use case for EBS volumes is

    - to have a hard drive that is persistent , that your applications can write to

    -  it's probably important that you back that data up in EBS volume

    - EBS allows you to take incremental backups of your data called snapshots

    - It's very important that you take regular snapshots of your EBS volumes

    - This way, if a drive ever becomes corrupted, you haven't lost your data and you can restore that data from a snapshot.



