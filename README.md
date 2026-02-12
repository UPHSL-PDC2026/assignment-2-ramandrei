# Assignment 2: Simple Distributed Message-Passing Coding Exercise
## Code Output Screenshots in Google Colab

<img width="609" height="366" alt="image" src="https://github.com/user-attachments/assets/960866a9-5db0-4f42-a10a-b3dcaaa3fcc2" />

<img width="537" height="488" alt="image" src="https://github.com/user-attachments/assets/01697639-061d-4b36-9bf7-ada572f0dca6" />

<img width="513" height="456" alt="image" src="https://github.com/user-attachments/assets/9b2a564a-a525-4733-a1b2-c1536661f8e5" />

<img width="377" height="476" alt="image" src="https://github.com/user-attachments/assets/c53cb522-72b1-43aa-9cc0-d489713e0691" />

<img width="492" height="251" alt="image" src="https://github.com/user-attachments/assets/39b9e961-47bb-4f41-b87a-368c8bc609a5" />

## Guide Questions:

**1. Why is message passing required in distributed systems?**

  Message passing is required in distributed systems because each process runs in its own separate memory space and cannot directly access the memory of other processes. For a system to share data or do tasks simultaneously, processes must send and receive messages directly. This ensures controlled and clear communication between nodes, even if they are in different machines just connected through a network. It also improves scalability since processes do not rely on shared memory hardware.

**2. What happens if one process fails?**

  If one process fails, the communication with that failed process may stop, which can cause the program to crash. But this can still depend on how the errors are handled based on the situation. In MPI, if a worker process fails, the master process may wait for a message that will never arrive, which could mean that it will wait for a long period of time. Some MPI implementations terminate all processes when one fails. To get back from a process failure, fault tolerance mechanisms are usually added to detect and recover from such failures. 

**3. How does this model differ from shared-memory programming?**

  In message passing interface, each process has its own private memory and communicates by sending messages. On the other hand, shared-memory programming allows multiple threads to access the same memory space directly. Shared-memory systems rely on synchronization mechanisms to avoid conflicts. Since processes do not share the same memory in MPI, it avoids direct memory conflicts. Distributed systems using message passing can run on multiple machines, whereas shared-memory programming is usually limited to a single system. This makes message passing more suitable for large-scale distributed environments.
