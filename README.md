[Libtask](https://swtch.com/libtask/): a Coroutine Library for C and Unix 
write event-driven programs without the hassle of events!
available for FreeBSD, Linux, OS X, and Solaris

*Author*: **Russ Cox**

> Libtask is a simple coroutine library.  It runs on Linux (ARM, MIPS, and x86),
FreeBSD (x86), OS X (PowerPC x86, and x86-64), and SunOS Solaris (Sparc),
and is easy to port to other systems.

Libtask gives the programmer the illusion of threads, but
the operating system sees only a single kernel thread.
For clarity, we refer to the coroutines as "tasks," not threads.

Scheduling is cooperative.  Only one task runs at a time,
and it cannot be rescheduled without explicitly giving up
the CPU.  Most of the functions provided in task.h do have
the possibility of going to sleep.  Programs using the task
functions should #include <task.h>.

