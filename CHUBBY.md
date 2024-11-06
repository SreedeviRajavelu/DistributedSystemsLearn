# Chubby Lock Service
- distributed lock manager

- to manage access to shared resources in a distributed environment

## In essence:

Chubby maintains a small number of lock files
which can be used by various distributed systems to synchronize their operations and & ensure consistent access to shared resources 

Clients can request locks on these files, which helps in coordinating actions and preventing conflicts in distributed systems 

## Master-replica architecture:

One chubby server acts as master, handling all client lock requests and maintaining a consistent state, while several replicas provide redundancy fault tolerance
This setup ensures that even if 1 master server fails, one of the replicas can take over seamlessly

Clients interact with Chubby using a simple API to open and close lock files, read & write small amounts of data, and acquire or release locks

When a lock is acquired by a client, other clients are prevented from making conflicting changes, thus maintaining consistency across the distributed system. 

### Advantages

+ coordination & synchronization
+ fault tolerance
+ reliability
+ scalability

Reference: https://www.linkedin.com/pulse/chubby-lock-service-enabling-robustness-distributed-systems-n-gr8ac/
