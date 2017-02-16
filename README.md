Q1. Explain what is a cluster and what is a hadoop cluster
Ans:
Cluster:
-In a computer system, a cluster is a group of servers and other resources that act like a single system and enable high availability,load balancing and parallel processing.
-In personal computer storage technology, a cluster is the logical unit of file storage on a hard disk.
-A cluster is managed by the computer's operating system.
-Any file stored on a hard disk takes up one or more clusters of storage.
-A file's clusters can be scattered among different locations on the hard disk.
-The clusters associated with a file are kept track of in the hard disk's file allocation table(FAT).
-When a file is read, the entire file is obtained and we aren't aware of the clusters it is stored in.
-Since a cluster is a logical rather than a physical unit, the size of a cluster can be varied.
-The maximum number of clusters on a hard disk depends on the size of a FAT table entry.
-In fact, many operating systems set the cluster size default at 4,096 or 8,192 bytes.


Q2.What is meant by a Rack and explain the rack arrangement in a hadoop cluster
Ans:
Rack:
-A Node is simply a computer.
-This is typically non-enterprise, commodity hardware for nodes that contain data.
-Storage of Nodes is called as rack.
-A rack is a collection of 30 or 40 nodes that are physically stored close together and are all connected to the same network switch.
-Network bandwidth between any two nodes in rack is greater than bandwidth between two nodes on different racks.

Rack arrangement in hadoop cluster:
-A Hadoop Cluster is a collection of racks.
-A default Hadoop installation assumes all nodes belong to the same rack.
-A simple policy is to place replicas across racks.This prevents losing data when an entire rack fails and allows to make use of bandwidth from multiple racks when reading a file.
-On multiple rack cluster,block replications are maintained with a policy that no more than one replica is placed on one node and no more
than two replicas are placed in the same rack with a constraint that number of racks used for block replication should be always less than total number of block replicas.
