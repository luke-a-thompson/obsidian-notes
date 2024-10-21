<https://www.youtube.com/watch?v=zCEYiCxrL_0>
<https://www.youtube.com/watch?v=VDzrvhgyxsU>
Edges can be anything
* e.g. E --edge-- F - The edge could be that E is below F, that E is above F, etc
	* It's a modelling decision
* Invariant to graph shuffling - I.e. does not matter which edge comes first
* *Degree* - The number of edges connected to a node

Classification
* Output 'h' at time step > BCE loss > update gradients ('W')> update GNN

# Understanding Graphs
## Graph Representation & Matrices
### Adjacency Matrix (*A*)
*  N = Nodes
	* A = N x N
* 2D matrix
* Types
	* Weighted, undirected
		* Weighted - Provide wieght
		* No weight - Provide negative 1
		* If A > B is 12, then B > A must also be 12
	* Weighted, directed
		* If A > B is 12, then B > A **not** necessarily 12
	* Unweighted, Directed
		* One-hot encoded for connections
		* If A > B is True, B > A must also be True
	* Unweighted, Undirected
		* If A > B is True, B > A **not necessarily** True
### Incidence Matrix
* Matrix describing which nodes are connected by edges
	* Nodes - Rows
	* Columns - Edges
* Undirected Graph
	* Node & edge connected > 1; else 0 ![[Pasted image 20231215182508.png]]
* Directed Graph
	* Node connected in outward direction > -1
	* Node connected in inward direction > 1
	* Node unconnected > 0 ![[Pasted image 20231215182748.png]]
### Degree Matrix or Diagonal Matrix (*D*)
* **Matrix in which the entries outside the main diagonal are all 0**
* **Diagonal value of a matrix which shows total number of connections**
	* Outward connection from node *x* returns to self > counted as 2
	* Node connected from edge > 1; else 0![[Pasted image 20231215182957.png]]
### Laplacian Matrix (*L*)
* Measure smoothness of a matrix
	* Only possible for undirected graphs
* L = {D - A}![[Pasted image 20231215192229.png]]
## Algorithms
### Bag of Nodes
* The algorithm - Weisfeiler-Lehman Kernel
	* **Iteratively aggregate information from a node's neighbours**
	1. Set initial label for each node (e.g. degree)
	2. Iteratively assign new label to each node using hashed labels from the neighbourhood
	3. After K iterations > information gathered about K-hop neighbourhood
	4. Use any bag of nodes metrics to summarise new labels
* Popular in cheminformatics
### Graph Walking
* Traverses all connected nodes
* **Random Walk**
	* Randomly traverse the node along connected edges*

# Understanding Graph Neural Networks
## Convolution in Graphs - Node Embeddings
* See [[Convolutional Neural Networks]]
* Cannot apply conventional CNN methods on GNN as they require fixed grid & structured data - Not present in GNN
### Graph Feature Matrix
* Feature matrix X = {N (nodes) x M (features)}*
* Analogy to [[Convolutional Neural Networks#Locality, Aggregation & Composition]]
	* Locality - Contribution of all neighbours to given node
	* Aggregation - Perform locality at all nodes one by one
	* Composition - Layer stacking
	* **Encoder function - Performs above 3**
### Node Embedding
* Helps represent graph as a vector > aids "convolution"
* Process
	1. Select a node
	2. Find connected neighbours - Based on neighbour hop depth
		* Node embedding space - Space in which each node has its embedding generated
	3. **Aggregation** - Convolute each connection to neighbours
	4. Perform for each node
		![[Pasted image 20231215232617.png]]
		![[Pasted image 20231215232713.png]]
* Advantages
	* Represent nodes as vectors
	* Shows network topology of Graph
	* Similar nodes have similar embeddings
	* **Used for prediction***
### Sum Aggregation
* Takes range of values > returns single value summarising the feature info of the set
* Determines GNN expressivity *
### Message Passing
* Allows information passing between nodes
* Messages are a function of the node, the neighbour and the connecting edge
* Process
	1. **Computation** - Each node in the graph computes a *message* (hidden state) for its neighbours
	2. **Aggregation**
		* Aggregate hidden states (& possibly edges) of neighbouring nodes and node itself
		* Aggregation function is permutation invariant (e.g. mean)
		* Nodes aggregate all the messages they receive using a permutation invariant function (i.e. invariant to the order of message reception)
	3. Update
		* Nodes update their attributes as a function of it's current attributes & aggregated messages
	* Repeat over several propagation layers
		* Nodes learn the complex structure of the graph based on info from their neighbours 
	* Find representation vector of entire graph by pooing over representation vector of each node at their last iteration
		* **This final whole-graph representation is used to estimate molecular properties**
	![[Pasted image 20231215235500.png]]
### Training
* <https://youtu.be/VDzrvhgyxsU?si=YWTvra91M26Xuffj&t=5879>
* **Training mask**
	* Regularisation method
	* Binary vector - 1 for nodes included in computation, 0 for excluded
	* Likely the nodes with ground truth values*
### Invariant Vs Equivarient GNNs
Invariant
* Output unchanged when input nodes permuted
* I.e. independent of input representation
Equivarient
* Output **changes in the same way** as input when input nodes permuted
* I.e. input permuted > output permuted identically*

## Types
### Scalar-Vector Type GNN
* Each node, edge embedding is a tuple of scalar features, geometric vector features
* Scalar features - Rotationally/translationally invariant properties
* Vector features - Predictably rotationally/translationally variant properties*

Principal Neighbourhood Aggregation for Graph Nets
* Novel architecture - Multiple aggregators + degree-scalers
* Degree scalers
	* Generalisation of sum aggregation > allows amplification/attenuation of signal based on degree of each node
	* Allows accounting for different degrees of each node when aggregating information from neighbouring nodes
	* **Allow different weighting of info coming from different nodes based on their degrees > increased expressive power**
* Can use continuous features*

Gated GNNs
	![[Pasted image 20231210155004.png]]
* Want to compute messages (*m*)
	Message dependent on type of edge *k*, neighbour *d* at time *t-1*
	and not dependent on *f* 
	E is a parameter of edge *k*
	Can bias *Ek*
	GRU is a recurrent NN

Introduce backward edges - Allows information to propagate back to orphan nodes
	Alternatively, create a "supernode" that is connected to all nodes, backpropagate information from this supernode
