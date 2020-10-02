# p2pPaxos
Demonstration of Paxos consensus protocol between distributed peers.

How it works:
Each node in network is instance of Node class. Connections between peers are made by NodeConnection class.
Each node has methods for sending and receiveing appropriate messages. Each node will run a NodeManager thread which manages node's participation in consensus in real-time.
for guide to paxos check "Paxos made simple" by Leslie Lamport:
https://www.cs.utexas.edu/users/lorenzo/corsi/cs380d/past/03F/notes/paxos-simple.pdf

In second section takes the network graph as input to start simulation. Uncomment net_graph line to see a simulation of sample given network.

## Input format should be:

<size_of_network> 
<nid> <timeout1> <timeout2> <timeout3> 
<nid> <delay> 
<nid> <delay> 
 ...

Size of network is number of nodes. Lines 2-4 must be given for each node. Line 2 contains timeouts for 3 phases of consensus. Next line will contain links to other peers in network and the link delay. After all links are in, next node can be defined simillarly. Input ends with entering empty line.

