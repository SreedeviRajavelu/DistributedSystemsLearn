## Raft is for leader election and data replication 

Consensus involves multiple servers agreeing on values
- fundamental problem in fault tolerance 


Raft consensus algorithm uses leader based consensus protocol where a "leader" handles the task of data updates and replication

1) leader election is a separate and mandatory step before the leader can get the data replicated 

2) Restriction that only the servers with the most up-to-date data can become leader

Reference: https://www.yugabyte.com/tech/raft-consensus-algorithm/#:~:text=Raft%20is%20a%20consensus%20algorithm,Raft%20consensus%20algorithm%20in%20action
