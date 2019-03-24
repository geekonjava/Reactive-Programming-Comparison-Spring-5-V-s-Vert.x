# Reactive-Programming-Comparison-Spring-5-V-s-Vert.x
Benchmark the performance of the described frameworks: For article: http://www.tellmehow.co/reactive-programming-comparison-spring-5-v-s-vert-x

##The performance test will simulate:
- 100 concurrent users
- 50,000 requests

The performance tests which I have executed have been performed on a machine with the following parameters:

| | |
| ------------ | ------------ |
| **OS**  |  **Fedora 27** |
|  **CPU** | **Intel(R) Quad Core(TM) i5 @ 2.67GHz**  |
| **Memory**  | **8GB DDR3**  |


## Results
### Vert.x
> Starting the test
Waiting for possible Shutdown/StopTestNow/Heapdump message on port 4445
summary + 49725 in 00:00:09 = 5345.0/s Avg: 11 Min: 0 Max: 499 Err: 0 (0.00%) Active: 14 Started: 100 Finished: 86
summary + 275 in 00:00:00 = 4583.3/s Avg: 1 Min: 0 Max: 11 Err: 0 (0.00%) Active: 0 Started: 100 Finished: 100
**summary = 50000 in 00:00:09 = 5339.6/s Avg: 11 Min: 0 Max: 499 Err: 0 (0.00%)**
Tidying up …
… end of run

### Spring 5
> Starting the test
Waiting for possible Shutdown/StopTestNow/Heapdump message on port 4445
summary + 5298 in 00:00:03 = 2085.0/s Avg: 26 Min: 0 Max: 454 Err: 0 (0.00%) Active: 100 Started: 100 Finished: 0
summary + 44702 in 00:00:10 = 4517.2/s Avg: 15 Min: 0 Max: 535 Err: 0 (0.00%) Active: 0 Started: 100 Finished: 100
**summary = 50000 in 00:00:12 = 4020.3/s Avg: 16 Min: 0 Max: 535 Err: 0 (0.00%)**
Tidying up …
… end of run

The results on my machine show that Vert.x can handle 50 000 requests 3 seconds faster than Spring 5.

**NOTE:** The Vert.x application is built on top of its latest stable version which is 3.4.2, while Spring 5 is in a release candidate phase.
