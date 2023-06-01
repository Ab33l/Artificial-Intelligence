Breadth First Search Implementations

Steps involved:

Step 1: Consider the graph you want to navigate.
Step 2: Select any vertex in your graph (say v1), from which you want to traverse the graph.
Step 3: Utilize the following two data structures for traversing the graph.
Visited array(size of the graph)
Queue data structure
Step 4: Add the starting vertex to the visited array, and afterward, you add v1’s adjacent vertices to the queue data structure.
Step 5: Now using the FIFO concept, remove the first element from the queue, put it into the visited array, and then add the adjacent vertices of the removed element to the queue.
Step 6: Repeat step 5 until the queue is not empty and no vertex is left to be visited.

Pseudo-code:

// Here, Graph is the graph that we already have and X is the source node
Breadth_First_Search( Graph, X ):
    Let Q be the queue
    Q.enqueue( X )     // Inserting source node X into the queue
    Mark X node as visited.

    While ( Q is not empty )
        Y = Q.dequeue( )     // Removing the front node from the queue

    Process all the neighbors of Y, For all the neighbors Z of Y
    If Z is not visited:
        Q. enqueue( Z )     // Stores Z in Q
        Mark Z as visited
