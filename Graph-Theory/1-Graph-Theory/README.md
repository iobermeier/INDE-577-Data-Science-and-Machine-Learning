# Graph Theory

Graph Theory is a non-tabular method in which networks can be depicted through points/nodes and lines/edges. A network graph contains a set of vertices connected to one another with various types depending on the number of edges connecting different nodes:
- simple graph - at most 1 edge between 2 vertices with no loops
- multigraph - any 2 vertices are joined by more than 1 edge
- complete graph - each vertex is connected by an edge to every other vertex
- directed graph - a graph in which a direction is specified to each edge

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/205550903-5c74f495-3794-44b4-9b5d-8b951a5420cb.png" alt="graph theory" style="width:600px;"/>
</p>

Used in operations research, social sciences, and molecular chemistry, graph theory uses features from connections to describe relationships and connectivity of groups. Degree can describe the number of edges that are connected to a node, or for example, the number of friends a person may have. Similarly, the path, or route along multiple edges can describe the connectivity of a graph. Depending on its use, network graphs have robust capabilities to not only process and calculate info, but also present them in a user-friendly method.


## Machine Learning Implementation

Artificial neural networks are essentially similar to network graphs since they share the same structure, terminology, and concepts. As seen in the image below, the perceptron model for neural networks resembles the layout of any network graph.

<p align="center">
<img src="https://user-images.githubusercontent.com/97500105/205550818-16887826-015f-495a-ad5a-2e23078de53c.png" alt="graph theory" style="width:500px;"/>
</p>

## Modeling

Network graphs typically create nodes and edges from data that is read in from CSV or text files that specify the any node attributes as well as source and destination locations for the edges. To build the graph model, details need to be given by the creator such as what type of graph to generate, specific attributes, and how to stylistically plot the data.

## Understanding the Data
The given dataset is the National Cancer Institute's Nature Pathway Interaction Database published in 2006 that shows flights taken across the world. The dataset was created to track the spreading of disease in an epidemic and how to best vaccinate people in order for the disease to cease spreading. 

The dataset has 2905 rows for each airport location and 12 columns with information such as city name, latitude, longitude, and airport codes. After building the initial nodes, we can see that the network resembles the countries of the world. By adding the edges of the graph, we can see the paths of the network across various cities. By pinpointing the countries and cities with the highest degree, vaccinations could be deployed to those first to decrease the likelihood of spreading over time.

## References & Further Reading:
- [Medium](https://medium.com/basecs/a-gentle-introduction-to-graph-theory-77969829ead8)
- [Britannica](https://www.britannica.com/topic/graph-theory)
- [Wikipedia](https://en.wikipedia.org/wiki/Graph_theory)
