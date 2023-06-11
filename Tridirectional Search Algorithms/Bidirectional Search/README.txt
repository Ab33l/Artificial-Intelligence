It runs two simultaneous searches, one form initial state called as forward-search and other from goal node called as backward-search, to find the goal node. Bidirectional search replaces one single search graph with two small subgraphs in which one starts the search from an initial vertex and other starts from goal vertex. 
The search stops when these two graphs intersect each other.

It is particularly useful when dealing with large graphs, high branching factors, and situations where an optimal path is required. 
It can be beneficial in memory-constrained environments and scenarios where the start and goal states are known.

We can consider bidirectional approach when:
1) Both initial and goal states are unique and completely defined.
2) The branching factor is exactly the same in both directions.