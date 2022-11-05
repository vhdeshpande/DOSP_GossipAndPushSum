# Project 2: Gossip and Push Sum Algorithm
This project aims to analyze gossip-type algorithms using an Erlang actor model simulator to determine their convergence using various topologies. The topology defines how nodes are connected. Because the actors are operating asynchronously, this is also known as asynchronous gossip.
### Authors:
* Vaibhavi Deshpande
* Ishan Kunkolikar
### Pre-requisites:
* Erlang/OTP version - 25.1
### Steps to run:
Commands to start the algorithm:
``` 
c(gossipAndPushSum).
c(bitcoinMiningServer).
gossipAndPushSum:start_gossip ( number_of_nodes, topology, algorithm ).
```
Where ‘number_of_node’ is the number of nodes in the topology, ‘topology’ is the topology which includes full network, line, 2D grid, and Imperfect 3D and the algorithm includes gossip or push sum algorithm

### Implementation details:
* **Gossip Algorithm**: The gossip algorithm spreads the message across the network. Every node in the topology randomly selects and transmits the message to the node to which it is connected in the network. After receiving the rumour ten times, the nodes stop transmitting the message.
* **Push Sum Algorithm**: In the push sum algorithm, each node maintains two values- s and w. Upon receiving a message, it adds the received weights to its s and w and while transmitting the message the node sends half of its weights. Each node will terminate when its ratio of s/w does not change more than 10-10 for up to three iterations.

### Largest Number of Nodes for Gossip Algorithm:
1. Full – 1000
2. Line – 500
3. 2D Grid -700
4. Imperfect 3D – 700
### Largest Number of Nodes for Push Sum Algorithm –
1. Full – 500
2. Line – 100
3. 2D Grid -500
4. Imperfect 3D - 500
