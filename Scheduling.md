### if.05.01 TINF Operting Systems

# Assignment 8: Scheduling

1. **Multiple Queues**
A process on a system with Multiple Queues Scheduling needs 30 quanta to complete. How many times must it be swapped in, including the very first time (before it has run at all)?

| Run | 1 | 2 | 3 | 4 | 5 |
| -- | -- | -- | -- | -- | -- |
Q | 1 | 2 | 4 | 8 | 15 |
Acc | 1 | 3 | 7 | 15 | 30 |

It must be swapped in 5 times.
******

2. **Shortest Process Next**
A scheduler working with the {\em Shortest Process Next} Strategy has two processes in ready state and has to schedule one of these:

| Process Name | 1st run | 2nd run | 3rd run | 4th run |
| -- | -- | -- | -- | -- |
A | 50 msec | 150 msec | 300 msec | 85 msec |
B | 300 msec | 150 msec | 85 msec | 50 msec

Which process will be taken by the scheduler and why?

Algorithm to Estimate Time to Run for a Process  
E3: T0/8 + T1/8 + T2/4 + T3/2  

A3 = 50/8 + 150/8 + 300/4 + 85/2 = 82,45 msec  
B3 = 300/8 + 150/8 + 85/4 + 50/2 = 38,56 msec  

The scheduler will take process B first because the estimate time is shorter.
******

3. **CPU-bound and I/O-bound Processes**
	- Explain in a few words the terms CPU-bound and I/O-bound processes.  
  I/O-bound processes need low quanta but high priority
  (if the user clicks a mouse button then a process have to start immediately
  else the scheduler waits till a mouse button is clicked).      

	- Why is it important for the scheduler to distinguish between CPU-bound and I/O-bound processes?  
  CPU bound processes have no user interaction. They need high quanta but low priority.
  And I/O-bound processes have a high user interaction. They need low quanta but high priority.      
******

4. **Real Time Schedulable**
A soft real-time system has four periodic events with periods of 50, 100, 200, and 250 msec each. Suppose that the four events require 35, 20, 10 and *x* msec of CPUtime, respectively. What is the largest value of *x* for which the system is schedulable?

∑ Ci/Pi ≤ 1  
35/50 + 20/100 + 10/200 + *x*/250 ≤ 1  
0,7 + 0,2 + 0,05 + *x*/250 ≤ 1  
0,95 + *x*/250 ≤ 1  
*x*/250 ≤ 0,05  
*x* ≤ 12,5  

So 12,5 is the largest value for *x*.
