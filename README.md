# Salgo Visualizer

Salgo Visualizer is a Java application that visualizes maze generation and pathfinding algorithms. Mazes are generated pseudorandomly and with a depth-first traversal. Multiple pathfinding algorithms are supported, including A*, Breadth-First Search (BFS), Depth-First Search (DFS), Dijkstra, and Greedy Best-First.

## Features and Quirks

- The visualization happens on a two-dimensional, square grid, with movement restricted to either up, down, left, or right. 
- Users are able to adjust grid size, visualization speed, and the weight associated with certain node types (custom and finish). 
- There are four different node types: start, finish, custom, and wall. 
- One start node and one finish node are necessary to search, and multiple custom nodes and wall nodes are allowed. 
- All the edges to a particular grid node are uniform in cost, the cost being defined by that node's weight. 
- By default, all grid nodes have a weight of one, but nodes set to custom, and the node set to finish, can be assigned an integer weight ranging from zero to 100. 
- Nodes set to wall, and the node set to start, always have a weight of zero. 
- Because of how I implemented the edge weights, the "better path" check step from A* and Dijkstra has been excluded, since the first time a node is discovered, so is the best path to it. 
- After a search is completed, the number of discovered nodes, visited nodes, and path length from start to finish is displayed. 
- Hovering over a node will give the user some information too ("W" stands for weight, "TC" stands for total cost from the start to this node, and "H" stands for heuristic). 
- The heuristic used in A* and Greedy Best First is Manhattan Distance.

## Installation and Usage

- To try out the application, follow these steps:

  1. In the repository, open the dist directory and download the executable JAR file.
  2. In your terminal, navigate to the directory where SalgoVisualizer.jar is located and do:

      ```
      java -jar SalgoVisualizer.jar
      ```