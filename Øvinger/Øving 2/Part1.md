# Mutex and Channel basics

### What is an atomic operation?
> An atomic operation is a "hidden" operation for the other tasks of the program. It does not communicate with other tasks while executing.

### What is a semaphore?
> Like an integer, but after initialization, you can only decrement and increment. 
> When a thread decrements it, and the result is negative, the thread blocks itself and cannot continue until another thread increments it.
> When a thread increments it, if there are other threads waiting, one of the waiting threads gets unblocked

### What is a mutex?
> A mutex is a variable s.t only one thread can access it at a time.

### What is the difference between a mutex and a binary semaphore?
> Implementation wise, they are more or less the same. Their intended uses, on the other hand, differ. Mutex is used to lock a shared resource for a critical operation, whilst binary semaphores are used to signal when tasks are done or not (synchronization usage)

### What is a critical section?
> A crititcal section is the part of the program where typically mutexes are used to lock a resource s.t other processes do not interrupt a crucial task. It is the part of the program where processes can access the shared resources and disrupt other processes.

### What is the difference between race conditions and data races?
 > A data race happens when 2 instructions from different threads both try to access the same data at the same time, where atleast one tries to modify the data. A race condition is an error that occurs when the order of the instruction leads to the program being executed wrongly.

### List some advantages of using message passing over lock-based synchronization primitives.
> - No waiting for resources
> - Easier to scale than lock-based

### List some advantages of using lock-based synchronization primitives over message passing.
> - Simpler algorithms
> - No need to allocate message objects - less space usage.

