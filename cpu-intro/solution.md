# Assumption
- IO takes 5 time units.

# Answers
1. The chance of an instruction being usage of CPU on both processes is 100%. So the CPU utilization is 100$.

2. Takes the first processes 4 time units to finish its instruction. Then execution of the second process begins. Takes 1 time unit to issue IO, 5 to finish IO, and 1 to complete IO.   

In total it takes 11 time units.

3. 1st process takes 1 time unit to run IO. OS switches execution to 2nd process, runs for 4 time units. Then 1st process is still blocked since IO is not finished. Then IO is completed in 1 time unit.  

In total it takes 1 + 4 + 1 + 1 = 7 time units. Order does matter due to context switching.

4. Then the result will be the same as in question 2.

5. Result will be the same as in question 3.

6. First the 1st process issues an IO 
2nd process uses CPU for 5 time units.
IO done for 1st but execution not switched to 1st. Then 3rd, 4th processes take 10 time units to finish.
Then the final 2 IO of 1st takes 14.

CPU utilization: 21/31

7. First the 1st process issues an IO 
2nd process uses CPU for 5 time units.
IO done, execution switched back to 1st. Then 1 for IO finish, then another for start.
Switch to 3rd. 5 time units.
IO done, execution switched back to 1st. Then 1 for IO finish, then another for start.
Switch to 4th, 5 time units.
IO done, execution switched back to 1st. Then 1 for IO finish.

Total: 1 + 5 + 1 + 1 + 5 + 1 + 1 + 5 + 1 = 21 
CPU utilization: 21/21

Running the process that issues the IO immediately might be a good idea since we can run other processes while waiting for IO to finish, instead of having to run for IO and wait separately.
