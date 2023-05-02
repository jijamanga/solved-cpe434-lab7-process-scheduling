Download Link: https://assignmentchef.com/product/solved-cpe434-lab7-process-scheduling
<br>
A multiprogramming operating system allows more than one process to be loaded into the executable memory at one time and allows for the loaded process to share the CPU using time multiplexing. One of the reasons for using multiprogramming is that the operating system itself is implemented as one or more processes, so there must be a way for the operating system and application processes to share the CPU. The scheduler is responsible for allocating the processor resources to the individual processes. There are different classes of scheduling that can be implemented for this purpose like Round-robin, Priority and First Come First Serve.

<h1>Important Terms</h1>

<strong>Quantum Time​</strong>: It is the amount of time a process is allowed to run. After a process is run for Quantum time, the scheduler chooses another process to run interrupting the currently running process in ​<em>preemptive scheduling​</em>. Based on the scheduling algorithm, the interrupted process will again be allowed to run.

<strong>Turn Around Time​</strong>: It is the total amount of time taken by a process to complete its execution. Turn around time includes the time actually a process is run on the CPU plus the time it waits.

<strong>Burst Time​</strong>: Time required by a process to complete. This is the actual time the process requires CPU for completion.

<strong>Wait Time​</strong>: Time a process waits. Mathematically, ​<em>Wait Time = Turn Around Time – Burst Time </em>

<h2>Assignment 1</h2>

<strong>Round-robin scheduling ​</strong>algorithm is one of the simplest scheduling algorithms, where each process gets a small unit of CPU time (​<em>time quantum​</em>) . Write a program that implements this scheduling. Find the scheduling order, average waiting time for the processes and turn-around time (to each process) when round-robin scheduling is applied.

Your program will accept as input following items:

Number of processes, ​<em>n  </em>

Quantum Time Unit

Id and Burst Time for each of ​<em>n ​</em>processes

You will create a structure as follows (This is just a hint, you may choose to do it in any way you like):

<table width="591">

 <tbody>

  <tr>

   <td width="591">struct ​process​{int ​pid​; ​//Process IDint ​burst_time​; ​//CPU Burst Time  int ​working_time​; ​//Time this process executed, ifworking_time==burst_time, process is complete  int ​t_round​; ​//turn around time, time needed for the process to complete ​}</td>

  </tr>

 </tbody>

</table>







You can assume that all the processes arrive at the same time.

<u>Your output must be clear that shows the order of execution. One sample example with quantum</u> <u>time 10ms is shown below. In addition you must also print the turn around time and wait time for</u> <u>each of the processes (you can create another table). Calculate and print average wait time also​</u>.

<table width="588">

 <tbody>

  <tr>

   <td width="94"><strong>Time  </strong></td>

   <td width="98"><strong>10ms  </strong></td>

   <td width="99"><strong>10ms  </strong></td>

   <td width="99"><strong>10ms  </strong></td>

   <td width="99"><strong>10ms  </strong></td>

   <td width="99"><strong>10ms </strong></td>

  </tr>

  <tr>

   <td width="94"><strong>PID  </strong></td>

   <td width="98">1</td>

   <td width="99">2</td>

   <td width="99">3</td>

   <td width="99">1</td>

   <td width="99">2</td>

  </tr>

 </tbody>

</table>







<h2>Assignment 2</h2>

<strong>Priority based-scheduling ​</strong>is one of the scheduling algorithms in which processes are allocated to the CPU on the basis of an externally assigned priority. The key to the performance of priority scheduling is in choosing priorities for the processes. Write a program that implements this scheduling. Find the scheduling order, average waiting time for the processes and turn-around time (to each process) when Priority scheduling is applied(assume that a processes are Non Preemptive)

Your program will accept as input following items:

Number of processes, ​<em>n  </em>

Id, Priority and Burst Time for each of ​<em>n ​</em>processes

You will create a similar structure, but this time you will have priority for each of the processes.




<table width="592">

 <tbody>

  <tr>

   <td width="592">struct ​process​{int ​pid​; ​//Process ID  int ​priority​;int ​burst_time​; ​//CPU Burst Time  int ​working_time​; ​//Time this process executed, ifworking_time==burst_time, process is complete  int ​t_round​; ​//turn around time, time needed for the process to complete ​}</td>

  </tr>

 </tbody>

</table>







You must display the result in tabular form as in the previous assignment.

<h2>Topics for theory</h2>

Round Robin Scheduling

Priority Based Scheduling

Preemptive vs Non Premptive Scheduling