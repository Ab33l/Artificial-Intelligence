Depth First Search Implementations

Steps Involved:
Step 1: Create a set or array to keep track of visited nodes.
Step 2: Choose a starting node.
Step 3: Create an empty stack and push the starting node onto the stack.
Step 4: Mark the starting node as visited.
Step 5: While the stack is not empty, do the following:
a) Pop a node from the stack.
b) Process or perform any necessary operations on the popped node.
c) Get all the adjacent neighbors of the popped node.
d) For each adjacent neighbor, if it has not been visited, do the following:
e) Mark the neighbor as visited.
f) Push the neighbor onto the stack.
Step 6: Repeat step 5 until the stack is empty.

Pseudo-code:

procedure DFS(node):
    mark node as visited
    process(node)
    
    for each neighbor in node.neighbors:
        if neighbor is not visited:
            DFS(neighbor)


Steps Involved if a Disconnected Graph:
Step 1: Create a recursive function that takes the index of the node and a visited array.
Step 2: Mark the current node as visited and print the node.
Step 3: Traverse all the adjacent and unmarked nodes and call the recursive function with the index of the adjacent node.
Step 4: Run a loop from 0 to the number of vertices and check if the node is unvisited in the previous DFS, then call the recursive function with the current node.