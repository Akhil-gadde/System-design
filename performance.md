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
