# Pokemon Game.

* Created by Shlomi Lantser

## About the assignment:
The given task was to build a runnable Pokemon game with a given sever that contians all the game data:
* Agents as players.
* Pokemons as Pokemons.

My task was to assign each agent to the given pokemons and to catch 'em all while using graph implementation project.

## The Algorithm:
I assigned pokemons to each agent depending on the distance between them and by using TSP and Djikstra Shortest Path algorithms.
this was used with threads- each thread to each agentץ

# Directed weighted graph implemantation python.
 
 ## The Directed Weighted Graph class
The main purpose of this class is to demonstarte how a graph is really look like.
I desided not to implement a class of nodes and edges like in the last assigment, in the Graph constructor I created two
dicts(but in aim to initialize the graph I give it two lists in the json files) , one for nodes and one for edges, and with them I implemented all the other functions.

The main veriables which I use in this class are:
  - nodes (dict type)
    - here I held all our nodes using the uniqe ids and position
  - edges (dict type)
    - here I held all our edges using three variables:
      - src : what is the node id i came from
      - dest : what is the node id i go to
      - w: what is the "weight" of this edge

|Main Functions|Explenation|RunTime|
|---|---|---|
|DiGraph constructor | The main constuctor of new Graph, here I initialize the nodes dict and the edges dict |O(1)
|get_all_v| return as a dict all the node in the graph |O(1)
|all_out_edges_of_node| return a dict of all the edges which go out from a given node |O(1)
|all_in_edges_of_node| return a dict of all the edges which in to a given node |O(1)
|add_node| adding a new node to our data structure(if his id exsist)|O(1)
|add_edge| create new edge in the graph|O(1)
|remove_node| in this function I removing a node from our graph, I need to find the givven id delete the edge go from it and into it|O(E)
|remove_edge| here I remove an edge from our graph|O(1)
|v_size| gives us the amount of nodes in our graph|O(1)
|e_size| gives us the number of edges in the graph|O(1)


# The Graph Algorithms and explanation.
The main purpose of this class is to implement known graph algorythms on the graph I was created.
I liked this part because I did the same thing in java but in more complicated and long way,
and now I really apply the approch of KIS- Keep It Simple

The main veriables which I use in this class are:
  * graph (which is a DiGraph type)
    * here I have all of the graph information I built earlier.
   
|Main Functions|Explenation|RunTime|
|---|---|---|
|GraphAlgo constructor | The main constuctor of the Graph's algorythms, using the DiGraph class|O(1)|
|get_graph| getting the graph information|O(1)|
|isConnected| this function check if a graph is strongly connected using the DFS method and the Kosaraju algorythm, this function is Boolean and I implement it in aim to solve the center algo |O(V +V*(V+E))|
|shortestpath| in this function i have used in the Dijkstra algorythm, at first I update al the nodes "weight" to inf execept the src node which I update to 0, I ran on all the nodes and update their weight to the min, and also saved the prev node of each node in the shortest path in aim to return the list of nodes I walk in |O(V^2 +E)|
|center| in the center function I find the center of a graph (if it connected) using the shortestPathDist, for each node I check the max path to other node and take the maximum one, than I returned the shortest path between all of the nodes maximum path and take his node | O(V^4)
|TSP| in a given list of cities I need to find the shortest path which contain all of them and the weight of it|O(n^4)
|load_from_json| this function loads the json file to my project|O(V+E)|
|

## How to run:
* open cmd in the main file(Ex4-OPP) and run this command: `java -jar Ex4_Server_v0.0.jar 11` (or any case between 0-15)
* open cmd in the src file inside the main file(Ex4-OPP\src) and run this command: `python student_code.py`

# Running video :

https://user-images.githubusercontent.com/92504985/164766696-39abfc19-04ea-43d3-8fc4-d6e7f9a56274.mp4

