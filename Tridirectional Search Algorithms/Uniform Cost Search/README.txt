
From the starting state, we will visit the adjacent states and will choose the least costly state then we will choose the next least costly state from the all un-visited and adjacent states of the visited states, in this way we will try to reach the goal state.
We won't continue the path through a goal state, even if we reach the goal state we will continue searching for other possible paths (if there are multiple goals).
We will keep a priority queue that will give the least costly next state from all the adjacent states of visited states.

Pseudocode:
UniformCostSearch(start, goal):
    Create an empty priority queue called frontier
    Create an empty set called explored
    
    Create a node with start as the initial state and cost 0
    Add the initial node to the frontier
    
    while frontier is not empty:
        Remove the node with the lowest cost from the frontier (priority queue)
        Set the node as current
        
        if current state is equal to the goal state:
            return the path from the initial state to the current state
        
        Add the current state to the explored set
        
        for each neighbor of current state:
            if neighbor is not in the explored set:
                Create a new node with neighbor as the state and cost (current cost + cost from current state to neighbor)
                Add the new node to the frontier
    
    // If the goal state is not found and the frontier becomes empty, it means there is no path from start to goal
    return "Goal state not reachable"

It particularly useful when you need to find the optimal path in a weighted graph, considering the costs associated with each edge. It is well-suited for scenarios involving shortest paths, resource allocation, traffic routing, and other situations where the cost of traversal is a critical factor.