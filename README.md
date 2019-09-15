# Buddy-System-Memory-Management
A simulation of the buddy system algorithm for memory management.

## Authors
Dina Adib Fouad  
Michael Khalil   
Rana Amr Afifi  

## Algorithm Description
The Buddy System is implemented using a binary tree; each node of the tree has an int `size` where the actual memory size=2^size. All nodes of the same level have equal memory sizes. 

At the start of the program, the root has `size = 10` and whenever a process requests a memory of particular size, it first checks that this memory is available in a linked list that points to all free memory spaces. 
If there's a free space, the process is allocated to it. 
If not, and there exists a memory size greater than the requested size, this memory is splitted until a memory of the required size is created. 

## Assumptions
1. If there's a process that could not be allocated at time x, the following process is run at time x+1 
2. If there's only 1 process in the queue, no switching time is computed and the process is left to run normally until it finishes or until another process arrives. In such case, the log is updated only once with the starting and stopping time of this single process. 
3. If new processes arrive while a process is running, they are pushed in the ready queue once the process finishes and then the process that was running is pushed.
