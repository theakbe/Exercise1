# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > *Concurrency means that several tasks are making progress at the same time in one core. While parallelism is that one task is split up into several subtasks which are computed in parallel on multiple cores.*
 
 ### Why have machines become increasingly multicore in the past decade?
 > *Because of increasing demands for higher machine speed which can handle multiple operations at once. Also, the improvement of clock speed rate has slowed down, and therefore machines have become increasingly multicore.*
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > *Concurrency helps solve problems which consist of multiple smaller problems.*
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > *It makes it easier to split the program into several smaller parts, which can make the programmer's job easier and more structured. Then again you will also have to synchronize all the parts, which can be difficult.*
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > *Processes are usually independent, while threads work as subsets of the processs. Green threads are "user-level threads", threads that are scheduled by a runtime library or virtual machine and not by the kernel. Coroutines are similar to threads, but they provide concurrency and not parallelism.*
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > *pthread_create() and threading.Thread() create threads, while go creates a coroutine.*
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > *The GIL allows only one thread to hold the control over the Python interpreter, which means it limits the use of multicores.*
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > *Eventlet / tasklet*
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > *This function changes the max number of CPUs that can execute tasks simultaneously.*
