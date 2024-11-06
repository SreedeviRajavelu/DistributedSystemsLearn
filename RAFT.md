## Raft is for leader election and data replication 

Consensus involves multiple servers agreeing on values
- fundamental problem in fault tolerance 


Raft consensus algorithm uses leader based consensus protocol where a "leader" handles the task of data updates and replication

1) Leader election is a separate and mandatory step before the leader can get the data replicated 

2) Restriction that only the servers with the most up-to-date data can become leader
   
3) Linearizability: there is a total linear order of all operations. Even when there are concurrent operations, the state of the database must be a result of ordered, sequential execution of operations. Every operation takes place atomically.

Reference: https://www.yugabyte.com/tech/raft-consensus-algorithm/#:~:text=Raft%20is%20a%20consensus%20algorithm,Raft%20consensus%20algorithm%20in%20action
