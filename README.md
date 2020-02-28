# Interesting Data Structures Algorithms Uses Cases

GINI index of income equality used in Decision Trees
![alt text](https://github.com/LewisRa/DataStructures-AlgorithmS/blob/master/gini_formula.jpg)

 ## Hashing - Search Engine

## What data structure is used in SQL database?
-Pretty much every data structure you've ever heard about - and many you probably haven't encountered - will be used somewhere in a database engine
- For more information, get SQLite or PostgreSQL and have a look at their source.
- The vast majority of data structures in a database don't actually have anything to do with storage.  They're for parsing, query optimization, query execution, concurrency, query scheduling, managing application connections, etc.
1. lists and queues for parsing.
2. trees for parse trees and execution plans.  The nodes in these trees are typically not of the same type, particularly for execution plans, which can make for adventures in debugging when things go wrong.
3. A manner of data structures (including stored ones such as B-Trees) in index structures.
4. Hash tables, tries, and other in-memory "speed" structures for metadata (ie, table definitions and such things).
5. And more hash tables for lots of other things, such as lock managers, hash join structures, etc.  
6. Some more specific to db engines are Pages and Rows, which are dynamic in their definitions and can't be completely stated as static structures in any programming language.  In this sense, they're more like networking packets than more traditional data structures.  Pages and Rows will be used in index structures and base table storage.

## Applications of Breadth First Travesal

1. Shortest Path and Minimum Spanning Tree
2. Peer to Peer Networks (Bittorrent) (Breadth First Search)
3. Crawelers in Search Engines
4. Social Networks Websites (Find people within the distance "k" using Breadth first search)
- You’re interested in company X. You want to find someone who works at company X in your network. You’d prefer to find someone who is ‘closer’ to you; a first-degree connection is much more preferable than a fourth-degree connection. This is perfect for a BFS. You first search your first-degree connections (added first) before you search your second-degree connections (their friends) and so on.
5. GPS Navigation Search systems
6. Broadcasting in Networks
7. Important for self-driving cars

https://www.geeksforgeeks.org/applications-of-breadth-first-traversal/

## Applications of Depth First Search
1. For a weighted graph, DFS traversal of the graph produces the minimum spanning tree and all pair shortest path tree.

https://www.geeksforgeeks.org/applications-of-depth-first-search/

## Applications of Queue
 - Copy and Paste
 

