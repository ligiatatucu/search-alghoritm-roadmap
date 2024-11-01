# search-alghoritm-roadmap
In the following alghoritm, it is calculated the distance between Porto Unico and Curitiba based on heuristic approach,a problem solving strategy that uses practical methods to produce solution that may not be perfect but are good enough given the time constraints. 
In this case, the heuristic approach is Greedy Algorithm. This method implies two parts:
 1. First part - creating vertex, adjacent and graph classes
 2. Second part - creating orderred array classes

Explanation of the code :
a) Class Vertex 
   The constructor initializes a new instance of Vertex with the following attributes:
   -label: This represents the unique identifier for the vertex, such as a name or number. It helps distinguish this vertex from others in the graph.
   -visited: A Boolean attribute, initially set to False. It tracks whether this vertex has been visited
   -distance_objective: This attribute might represent a heuristic or cost estimate to reach a target vertex.
   -adjacent:This is a list that will hold other vertices (specifically, Edge objects or similar structures) that are adjacent, or directly connected, to this vertex
   #Method: add_adjacent(self, adjacent)#-this method adds an adjacent vertex to the adjacent list
   #Method: print_method(self)#-this method iterates over the adjacent list and prints the label and cost of each adjacent vertex.
b) Class Adjacent - to represent the path between vertex and adjacent
    
   
