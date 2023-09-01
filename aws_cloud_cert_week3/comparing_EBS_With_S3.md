# <ins> Comparing Amazon EBS and Amazon S3 </ins> #

- **Amazon EBS**

- In the `block storage corner`, weighing in its `size is up to 16 tebibytes i.e 2^40 bytes each `

- `EBS` with a `unique ability to survive the termination of their Amazon EC2 instances. `

- They are `solid state by default` and `spinning platters`. They are `Elastic Block Storage`

- `HDD options` also available for `EBS` as well

- Each `storage class` `post` the `best dynamically distributed design `for `different storage demands`

- **Amazon S3**

- `Amazon S3` In the `regional object storage` corner `weighing in at unlimited storage`, with `individual objects` at `5,000 gigabytes in size`

- They `specialize` `in write once, read many`

- `They are 99.999999999 percent durable`

- They are `Amazon Simple Storage Service` or `Amazon S3`

- Each `storage class` `post` the `best dynamically distributed design `for `different storage demands`

- **Which is the best Storage class for Amazon S3**

- Round 1 Use-case:-

    - Let's say `you're running a photo analysis website where users upload a photo of themselves and your application finds the animals that look just like them`

    - You have `potentially millions of animal pictures` that all need to be `indexed` and `possibly viewed by thousands of people at once`

    - `This is the perfect use case for S3. `
    
    - `S3 is already web-enabled.`

    - `Every object already has a URL` that `you can control access rights to who can see or manage the image.`

    - It's `regionally distributed among 3 AZ i.e availability Zone`, which `means that it has 11 9's of durability`

    - `No need to worry about backup strategies. S3 is your backup strategy`

    - `Plus the "cost savings is substantial" overrunning  or spreading the "same storage load on EBS" `

    - `Amazon S3` with the `additional advantage of being serverless` i.e `No Amazon EC2 instances are needed`

    - `Sounds like S3 is the judge's winter here for this round`


- Round 2 Use-case:-

    - you have an 80-gigabyte video file that you're making edit corrections on. 

    - To know the best storage class here, we need to understand the difference between `object storage and block storage`

    - `Object storage` treats `any file` as a `complete discrete object`

    - Now, `this is great for documents, and images, and video files that get "uploaded and consumed as entire objects" `

    - But `every time there's a change to the object, you must re-upload the entire file.`

    - There are no `Delta updates` in case of `object storage`

    - `Block storage "breaks those files" down "to small component parts or blocks".`

    - This means in case of `Block Storage` for that `80-gigabyte file`, when `you make an edit to one scene in the film` and `save that change`, the `engine only updates the blocks where those bits live`

    - `If you're making a bunch of micro edits using EBS, Elastic Block Storage is the perfect use case.`

    - `If you were using S3, every time you save the changes, the system would have to upload all 80 gigabytes , that whole thing every time`

    - `EBS` clearly `wins` round 2

**Conclusion**
    
- This means if you are using `complete objects or only occasional changes, S3 is victorious.`

- If `you are doing complex read, write change functions then absolutely, EBS is your knockout winner.`

- `Your winner depends on your individual workload.`

- `Each service is the right service for specific needs.`

- `Once you understand what you need, you will know which service is your champion.`

