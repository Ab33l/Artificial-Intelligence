Consider a square grid having many obstacles and we are given a starting cell and a target cell. We want to reach the target cell (if possible) from the starting cell as quickly as possible. Here A* Search Algorithm comes to the rescue.

It combines the advantages of both Uniform Cost Search (UCS) and heuristic information to find the optimal path in a weighted graph efficiently. It uses an evaluation function that considers both the cost of the path from the start node and an estimated cost to reach the goal node.

It is suitable for problems that require finding the optimal path in a weighted graph while considering both the cost of the path and additional heuristic information. 

In addition, It is often applied in shortest path problems, navigation or route planning, pathfinding in games and resource allocation.

Pseudo code

1.  Initialize the open list
2.  Initialize the closed list put the starting node on the open list (you can leave its f at zero)

3.  While the open list is not empty:
    a) find the node with the least f on the open list, call it "q"

    b) pop q off the open list
  
    c) generate q's 8 successors and set their parents to q
   
    d) for each successor:
        i) if successor is the goal, stop search
        
        ii) else, compute both g and h for successor
          successor.g = q.g + distance between 
                              successor and q
          successor.h = distance from goal to 
          successor (It can be done using many ways, but the area of scope in this project will be on: three heuristics-Manhattan, Diagonal and Euclidean Heuristics)
          successor.f = successor.g + successor.h

        iii) if a node with the same position as successor is in the OPEN list which has a lower f than successor, skip this successor

        iv) if a node with the same position as successor  is in the CLOSED list which has a lower f than successor, skip this successor otherwise,add the node to the open list end (for loop)
  
    e) push q on the closed list end (while loop)