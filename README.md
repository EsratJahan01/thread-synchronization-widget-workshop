# thread-synchronization-widget-workshop
A multithreaded simulation in C demonstrating thread synchronization using semaphores, mutex locks, and FIFO queues to manage shared resources in an operating system environment.

# The Whimsical Widget Workshop (Thread Synchronization in C)

## Project Overview
This project demonstrates **thread synchronization in operating systems** using a real-world inspired simulation called *The Whimsical Widget Workshop*.

In this system, engineers work concurrently to build widgets while sharing limited resources. The project ensures safe and fair access to resources using synchronization mechanisms.

## Problem Scenario
- Engineers represent **threads**
- Tools represent **shared resources**
- Multiple engineers work simultaneously
- Only one engineer can use a resource at a time

The system ensures:
- No race conditions
- Fair resource allocation
- No deadlocks
- Proper thread synchronization

## Synchronization Techniques Used

### Semaphores
Each resource has its own semaphore initialized with value **1** to ensure only one engineer can access it at a time.

Functions used:
- `sem_init()` – initialize semaphore
- `sem_wait()` – request resource
- `sem_post()` – release resource
- `sem_destroy()` – clean up semaphore

### Mutex Locks
A mutex lock protects shared data structures such as waiting queues and logging output.

This ensures that only one thread modifies shared data at a time.

### FIFO Waiting Queue
Each resource maintains a **First-In First-Out queue** so engineers receive resources in the order they request them.

This prevents **starvation**.

## System Workflow
1. Engineers are created as threads.
2. Each engineer randomly selects required resources.
3. Engineers join the FIFO queue for those resources.
4. Resources are acquired using semaphores.
5. Engineers build widgets (simulated with sleep).
6. Resources are released for other engineers.

## Technologies Used
- C Programming
- POSIX Threads (pthread)
- Semaphores
- Mutex Locks

## Key Operating System Concepts Demonstrated
- Thread synchronization
- Mutual exclusion
- Resource sharing
- Deadlock prevention
- Fair scheduling

## Team Members
- Ahnaf Dewan
- Md Mahiruddin Chowdhury
- Bushramoni Neha
- **Esrat Jahan Jerin**

## Course Information
Course: **CSE325 – Operating Systems**  
Instructor: **Shatabdi Roy Moon**  
East West University
