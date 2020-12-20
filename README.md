# ex1
ex1 solution
## Project Number - Ex1

Ex1 is the second exercise in the OPP course of Ariel university.
this exercise will allow you to create an undirected and weighted graph and to get information such as the shortest path between nodes, which is calculated by the shortest weighted path,  
copy the graph, remove nodes, or edges, adding nodes, connection node, save and load graph and more.

## How To Installation

to use this exercise you need to import the .java files to your IDE and now you can use this.

## How To Usage

we have here two classes: Graph_DS, this class included NodeInfo class and Graph_Algo. there is an interface to each class that elaborates on each function.
in the implementation of each function, some comments will explain how the function works.

## Class Method

class methood: WGraph_DS (NodeInfo)
 
I have a few private items: key, Tag, node Id, Info. 
these items represent the characteristics of the node info. 
* empty contractor for node info to initializing each node. 
* nodeInfo 
* getKey -  Return the key (id) associated with this node, (each node_info has a unique key).
* getInfo - return the Info associated with this node.
* setInfo -  Allows changing the Info associated with this node.
* getTag - return the Tag associated with this node
* setTag - Allow setting the "tag" value for temporal marking a node.

class method: WGraph_DS 

I have a few private items: ID, HashMap <Integer, node_info> V (V- is a hash map for my vertical in the graph. each vertical represent with <key, the node info itself>),
HashMap <HashMap<Integer, HashMap<Integer, Double>> WEdge (WEdge- is a hash map for my edges weight between to connected nodes. each edge represent with <key_1,<key_2, weighted edge between key_1 to key_2>>),
MC, edgeSize. 
* empty contractor - to initialize the graph and his private items. 
* getNode - return the node_info by the node_id.
* hasEdge - return true if and only if there is an edge between node_1_ID and node_2_ID, and these two nodes exist nodes in my graph.
* getEdge - return the weight if the edge between node_1_ID and node_2_ID. In case there is no such edge, or both of these nodes do not exist in my graph, I will return -1.
* addNode - add a new node to the graph with the given key.  if there is already a node with such a key -> no action should be performed.
* connect - Connect an edge between node_1_ID and node_2_ID, with an edge with nonnegative weight. : if the edge node_1_ID - node_2_ID already exists - the method simply updates the weight of the edge.
* getV - this method return a pointer for a Collection representing all the nodes, verticals, in the graph.
* getV(int node_id) - This method returns a Collection containing all the nodes connected to node_id, ni.
* removeNode - Delete the node (with the given ID) from the graph - and removes all edges which start or end at this node.
* removeEdge -  Delete the edge who connect the two given nodes ID from the graph,
* nodeSize - return the number of vertices (nodes) in the current graph.
* edgeSize - return the number of edges in my current graph (unidirectional graph).
* getMC - return the Mode Count - for testing changes in the graph.

class method: WGraph_Algo

my weighted_graph g is a private item. 
* WGraph_Algo
* Dijkstra(int src, int dest) - this algorithm should find the shortest path between node src (start) to node dest (target). for that, I use a hash map, deleted list, and priority queue.
* init - Init the graph on which this set of algorithms operates.
* getGraph - return underlying graph of which this class works
* copy - Compute a deep copy of this weighted graph.
* isConnected - returns true if and only if there is a valid path from EVERY node to each other node.
* shortestPathDist - returns the length of the shortest path between src to dest, if there is no such path returns -1.
* shortestPath - returns the the shortest path between src to dest - is an ordered list of nodes: src--> n1-->n2-->...dest. if no such path returns null.
* save - Saves this weighted (undirected) graph to the given file name.
* load - This method loads a graph to this graph algorithm. if the file was successfully loaded - the underlying graph of this class will be changed (to the loaded one),
in case the graph was not loaded the original graph should remain "as is".
     
## Links

[Dijkstra algorithem - wikipedia](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm)

## Tests 

WGraph_DStest
WGraph_Algotest

## License

this exercise made by Moriya Bitton, email address - moria1109@gmail.com
