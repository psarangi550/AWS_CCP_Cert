# <ins> Instance Stores and Amazon Elastic Block Store (Amazon EBS) </ins> #

- Instance stores

    - `Block-level storage volumes` behave like physical hard drives.

    - An `instance store` provides `temporary block-level storage` for an` Amazon EC2 instance`.

    - An `instance store` is `disk storage` that is `physically attached to the host computer for an EC2 instance`

    - therefore has the same lifespan as the instance. When the instance is terminated, you lose any data in the instance store.

    - An Amazon EC2 instance with an attached instance store is running.All data on the attached instance store is deleted.

# <ins> Amazon Elastic Block Storage (Amazon EBS) </ins> #

- `Amazon Elastic Block Store (Amazon EBS)` is a `service` that `provides block-level storage volumes that you can use with Amazon EC2 instances`. 

- `If you stop or terminate an Amazon EC2 instance, all the data on the attached EBS volume remains available`

- To create an EBS volume, you define the configuration (such as volume size and type) and provision it. After you create an EBS volume, it can attach to an Amazon EC2 instance.

- Because EBS volumes are for data that needs to persist, it’s important to back up the data. You can take incremental backups of EBS volumes by creating Amazon EBS snapshots.

# <ins> Amazon EBS Snapshots </ins> #

- An `EBS snapshot` is an `incremental backup`.

- This means that the first backup taken of a volume copies all the data

- For subsequent backups, only the blocks of data that have changed since the most recent snapshot are saved.

- Incremental backups are different from full backups, in which all the data in a storage volume copies each time a backup occurs.

- `The full backup` `includes` `data` `that has not changed since the most recent backup.`



