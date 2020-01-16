# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency means multiple computations are happening at the same time but in no specific order. ex: Multiple computers in a network, multiple applications running on the same computer.

 Parallelism is different techniques to make programs faster by performing several computations at the same time. To use parallelism one require hardware with multiple processing units. 

 The difference between Concurrency and Parallelism is that Concurrency means computations happening at the same time, and complete in overlapping time periods, but in no specific order. On the other hand Parallelism is when multiple tasks, or several parts of a unique task run at the same time, by using a multi-core processor.
 
 ### Why have machines become increasingly multicore in the past decade?
 > In the past decade the rate of clock speed improvement has slowed and the solution is machines with multi-core processor with the use of parallelism to increase overall performance.

 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > When you want to increase the performance of your program, concurrency is a possible solution.
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > With concurrent programming one have to think different, and take concern of how to divide your program in to smaller parts. This makes the programming more complex, but it allows developers to create software that would not be possible without concurrency.

 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > A process is an instance of a running program that is isolated from the other processes on the same machine. A process has it's own private section of the machine's memory.
 A thread is the unit of execution within a process. A process can have one or many threads.
 Green threads are threads that are scheduled by a virtual machine instead of natively by the underlying OS.
 Coroutines are a generalization of subroutines. Coroutines are used for cooperative multitasking where a process give away control periodically to enable multiple applications to be run simultaneously.

 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > "pthread_create()" starts a new thread in the calling process, "threading.Thread()" is a constructor which creates a new thread, "go" automates the downloading, building, installation and testing of Go packages and commands. Creates coroutine.
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > The Pythons Global Interpreter Lock (GIL) is a lock that allows only one thread to hold the control of the Python interpreter. This means that only one thread can be in a state of execution at any point in time.
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > A workaround for the GIL is to use a parallel execution technique other than shared memory threading, i.e. Use the multi-processing module.
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > "func GOMAXPROCS(n int) int": GOMAXPROCS set the maximum number of CPUs that can be executing simultaneously and returns the previous setting. If n < 1, it does not change the current setting. The number of logical CPUs on the local machine can be queried with NumCPU.
