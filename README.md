# Interesting Data Structures Algorithms Uses Cases

## Difference between Linear and Non-linear Data Structures

#### Linear Data Structure:
Data structure where data elements are arranged sequentially or linearly where the elements are attached to its previous and next adjacent in what is called a linear data structure. In linear data structure, single level is involved. Therefore, we can traverse all the elements in single run only. Linear data structures are easy to implement because computer memory is arranged in a linear way. Its examples are array, stack, queue, linked list, etc.

#### Non-linear Data Structure:
Data structures where data elements are not arranged sequentially or linearly are called non-linear data structures. In a non-linear data structure, single level is not involved. Therefore, we can’t traverse all the elements in single run only. Non-linear data structures are not easy to implement in comparison to linear data structure. It utilizes computer memory efficiently in comparison to a linear data structure. Its examples are trees and graphs.



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

## We use two data structures to implement an LRU Cache.

Queue which is implemented using a doubly linked list. The maximum size of the queue will be equal to the total number of frames available (cache size). The most recently used pages will be near front end and least recently pages will be near the rear end.
A Hash with page number as key and address of the corresponding queue node as value.We use two data structures to implement an LRU Cache.

Queue which is implemented using a doubly linked list. The maximum size of the queue will be equal to the total number of frames available (cache size). The most recently used pages will be near front end and least recently pages will be near the rear end.
A Hash with page number as key and address of the corresponding queue node as value.

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

--- 
## Tree vs graph 
A graph is a related data structure that is also quite popular (think complex networks of any kind), unlike a tree, the main difference is that there are bi-directional connections and no root 

## Applications of Queue
 - Copy and Paste
 ---
 GINI index of income equality used in Decision Trees
![alt text](https://github.com/LewisRa/DataStructures-AlgorithmS/blob/master/gini_formula.jpg)
---

Klondike/Spider Solitaire/ advanced AI methods such as constraint propagation and make use of data structures such as BST
There are hundreds of different varieties of Solitaire ranging like Golf, Tripeaks, Bakers Game, Thirteen and so on but probably the most difficult ones are Klondike and Spider solitaire! Klondike solitaire (which many people simply call solitaire) can make use of data structures ranging from stacks to splay trees! Also solitaire games can use Fisher-Yates Shuffle algorithm!

Related Articles:

Shuffle a given array using Fisher-Yates Shuffle algorithm
Shuffle a deck of cards

https://www.geeksforgeeks.org/10-projects-that-every-developer-should-lay-their-hands-on/
---
