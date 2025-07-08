Performance is measured by 
1. Workload and
2. Hardware

Every **performance problem** is the result of some **queue building** somewhere.
* Example: Network socker queue, DB IO queue, OS run queue , **Traffic Jam**

**Reasons** for the queue buildup
* Inefficient slow processing(Algorithmic) - **Efficiency**
* Serial resource access(single thread execution) - **Concurrency**
* Limited resource capacity(Hardware capacity) - **Capacity**

**Efficiency**
It is measure in terms of single request processing

![image](https://github.com/user-attachments/assets/0ea3ac47-6812-4469-a6f6-95786604008a)

Important things to check
* Efficient Resource Utilization
  1. IO - Memory, Network, Disk
  2. CPU
* Efficient Logic
* Efficient data storage
* Caching

**Concurrency**
![image](https://github.com/user-attachments/assets/349a5637-4b4d-485a-97b9-54ab81d624e4)
* Hardware
* Software
  1. Queuing
  2. Coherence.

System Performance Objectives
* Minimize Request-Response Latency(time of each request)
* Maximize Throughput(Rate of request processing)

Performance Measurement Metric
* Latency
* Throughput
* Errors
    1. Functional correctness should be avoided.
* Resource Saturation
  1. Affects- Hardware capacity Required
  2. Desired- Efficient utilzation of all system resources.
* Tail latency- It is the percentage of requests(say 1-5 percentile) having the latency greater than a specific latency. Such a latency is called tail latency.
<img src="https://github.com/user-attachments/assets/f8e7a34d-8d2f-4ed5-ad02-acf3d9023df4" width="400" height="300" />



**Network Latency**
TCP - Transmission control protocol is the basic protocol to transfer data in segments between two networks.

It uses a 3-way handshake for the network establishment and the segments are numbered for the receiver to rearrange them correctly.

SSL/TLS connection
it is security layer over the TCP.
HTTPS uses this layer.

**Memory Access Latency**
1. Finite Head memory
2. Large Heap memory
3. GC Algorithm
4. Finite buffer memory in the database(any rewrite happens using this buffer memory).


Things to check
1. Avoid Memory Bloat
2. Weak/soft References(Ex: this reference tells the Garbage collector to prioritize its collection in case of unusage)
3. Multiple smaller Processes(this is better than a single big process)
4. Garbage Collection Algorithm( suitable algo for live process and batch process.

In buffer storage.
* Normalization
* Compute over storage

**Disk Latency**

Normalization: It is the management of data base to reduce the redundancy and maintain data integrity.
Ex: using relations with foreign keys in tables.

It is always better to read data in sequential fashion than random fashion
Ex: there is a cost associated for a disk seek,
so in terms of sequential read, there will be a single disk seek, reducing the disk latency by many folds.



**CPU Latency**

* Context switching
it can affect a lot for the latency
For a multithread OS, 
when there are two processes, after the process 1 completed, state of completion will be save in PCB1 and then the state will be restored from PCB2
This will result in wastage of time.


Ways to reduce context switching
* Efficient algorithms and Efficient Queries
* Batch IO(grouping different read or write IO operations can reduce context switching) and Async IO( IO of logging can be asynchronous, it can be added to another thread)
* Single Threaded model(Not clear)
* Thread pool size should be simple-> when there is a large thread pool, the CPU do a lot of context switching which affect latency.
* 





