# <ins> AWS EC2 instance Type </ins> #

- There are different type of `EC2 instances`

- `EC2` instances are `like the employee inside the coffee shop` , which responsibilty to serve the `client request`

- if we want to server `multiple customer` we need more number of `employee` in the coffee shop , they all can't of `cashier type`

- we need `someone` to `mkae the drink like barista` and `handle the food` nd someone to do `cool latte art`

- if we want to perform `different task` we need `different skillset` , which `can't be handle by a single person `

- like different `Employee to serve different purpose in coffee shop` we have different `EC2 instance which serve different purpose` while deploy to `AWS environment`

- Each `Amazon EC2` instance type is grouped under `an instance family` and `optimized for certain Task`

- `AWS EC2 instance` of `various type` based on `different storage/CPU/Memory)/networking capacity`

- Amazon EC2 instance types are optimized for different tasks

    - When selecting an instance type, consider the `specific needs of your workloads and applications`

- the `AWS EC2` instance been grouped on the below `instance family` such as 

    - **General Purpose**

        - provide `good lavel` off

            - compute 

            - memory

            - network traffic 

        - which can be used as the `web service` or `code repo` or `gaming server` or `backend server for enterprise application` or `small and medioum DB` 

        - Suppose that `you have an application` in `which the resource needs for compute, memory, and networking are roughly equivalent`. You might consider running it on a `general purpose EC2 instance`

    - **Compute Optimized**

        - `Compute optimized instances` are ideal for `compute-bound applications` that benefit from `high-performance processors`

        - Like g`eneral purpose instances`, you can use `compute optimized instances` for workloads such as `web, application,` and `gaming servers.`

        - useful for 

            - compute intensive Task such as `gaming`

            - High Performance computing (HPC)

            - scientific modelling 

        - compute optimized applications are ideal for 

            - `high-performance web servers`

            - `compute-intensive applications servers`

            - `dedicated gaming servers`

            - You can also use `compute optimized instances` for `batch processing workloads` that `require processing many transactions` in a `single group`

    - **Memory Optimized**

        - Memory optimized instances are designed to `deliver fast performance for workloads that process large datasets in memory`

        - In computing, `memory is a temporary storage area` , It holds all the` data and instructions` that a `central processing unit (CPU) needs` to be `able to complete action`

        - Before a `computer program or application is able to run`, it is `loaded from storage into memory`.

        - This` preloading process gives the CPU direct access to the computer program`

        - useful for 

            - Memory intenstive Task 

        - Suppose that you have a workload that requires large amounts of data to be preloaded before running an application. 

        - This scenario might be a high-performance database or a workload that involves performing real-time processing of a large amount of unstructured data.

        -  In these types of use cases, consider using a memory optimized instance

        - `Memory optimized instances` `enable you` to `run workloads with high memory` needs and `receive great performance from CPU after interacting with the program`.


    - **Accelarated computing** 

        - useful for

            - floating point number calculatiuon

            - Graphics processing 

            - Data Pattern Matching  

        - utilizes the `hardware accelators`

        - Accelerated computing instances `use hardware accelerators, or coprocessors`, to `perform some functions more efficiently` `than is possible in software running on CPUs`

        - `In computing, a hardware accelerator` is a `component` that can` expedite data processing`

        - `Accelerated computing instances` are `ideal for workloads `such as `graphics applications, game streaming, and application streaming.`

    - **Storage optimized**

        - workload which required  High performance for locally stored data 

        - `Storage optimized instances` are `designed` for` workloads that require high, sequential read and write access to large datasets on local storage.`

        - useful for 

            - `data warehouse application`

            - `distributed file system`

            - `high-frequency online traction processing system (OLTP)`

        - In `computing`, the term `input/output operations per second (IOPS)` is a `metric that measures the performance of a storage device`.

        - It indicates how many different `input or output operations a device can perform in one second`

        - `Storage optimized instances` are `designed to deliver` `tens of thousands of low-latency, random IOPS to applications`

        - You can think of `input operations as data put into a system`, such as `records entered into a database.` An `output operation is data generated by a server`
        
        -  An example of output might be the `analytics performed on the records in a database`

        -  If you have an application that has a high IOPS requirement, a storage optimized instance can provide better performance over other instance types








    


