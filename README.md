# Interesting Data Structures Algorithms Uses Cases

## Difference between Linear and Non-linear Data Structures

#### Linear Data Structure:
Data structure where data elements are arranged sequentially or linearly where the elements are attached to its previous and next adjacent in what is called a linear data structure. In linear data structure, single level is involved. Therefore, we can traverse all the elements in single run only. Linear data structures are easy to implement because computer memory is arranged in a linear way. Its examples are array, stack, queue, linked list, etc.

#### Non-linear Data Structure:
Data structures where data elements are not arranged sequentially or linearly are called non-linear data structures. In a non-linear data structure, single level is not involved. Therefore, we can’t traverse all the elements in single run only. Non-linear data structures are not easy to implement in comparison to linear data structure. It utilizes computer memory efficiently in comparison to a linear data structure. Its examples are trees and graphs.



 ## Hashing - Search Engine
 Functions: 
 - add_to_index(index, keyword, url)
 - lookup (index, keyword)
 - add_page_to_index( index, url, content)
 
 ```PY
 def lookup(index, keyword):
  for entry in index: 
   if entry[0] == keyword:
    return entry[1]
  return []
  ```
  In this function, we look through the index(list of lists) to find the entry/word that match the input keyword and return the url assocites with the keyword. This works, however, we are using a for loop to go through each entry in the index which is not scalable. One solution is to kept index in a sorted order (see Quick Sort, Merge Sort, Heap Sort, etc..). Another solution is using a hashing function to store keywords is buckets that are easier to search.
  
  We could have a bucket for each letter but this will not scle well because 't' for example would have wayy more words in the bucket tha 'z' bucket. 
  
  Suppose we have b buckets and k keywords (k>b), the properites should has function are:
  - 1. output a number between 0 and b-1. 
  - 2. map appr. k/b keywords to buckets 0 and bucket b-1
  
#### Defining a hash function
 1.Hash functions takes the keyword and # of buckets and outputs a number between 0 and b-1 buckets
 2. ord() maps single letter to number
  
ord (<one letter string> )---> number <br>
chr(<number>)---><one letter string> <br>

print ord('a')-> 97 <br>
print ord ('A')-> 65 <br>
print('B')-> 66 <br>
print chr(ord('u'))-> u <br>
 3.  number % modulus --> remainder
 
 ```PY
 def bad_hash_string(keyword, buckets):
  return ord(keyword[0] % buckets)
```
This function takes the first letter of keyword and get the number output to get a remainder. 

 
  

  

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
## Sorting 
Sorted data powers (almost) everything. Think about it: whenever you interact with a web or mobile application, you can sort a large set of data by some property. Databases also have sort and search through huge sets of data, using something called Btrees. They sort through so much data that we, as humans, can’t even wrap our heads around!
Quick Sort: traditionally built-in for many runtimes, hence used by programs that call the default. Can’t be used where worst-case behavior could be exploited or cause significant ramifications, such as services that might receive denial-of-service attacks, or real-time systems. Quick3 or Randomized variants avoid worst-case.

Merge Sort: used in database scenarios, because stable (multi-key sort) and external (results don’t all fit in memory). Useful in distributed scenarios where additional data arrive during or after sorting. Memory consumption prevents wider use on small devices, but in-place Nlog^2N version does exist. Used in C++ runtime: stable_sort.

Heap Sort: reliable in-place NlogN sort for when you can’t abide worst-case. Not commonly used as a default (previously Quick was proclaimed best; now hybrids rule). Heaps are good for keeping data “partially digested”, when you progressively receive data but don’t need to produce sorted output until it finishes arriving.To write a heap sort algorithm, it requires knowledge of arrays and trees. 

Insertion Sort: great for small or mostly-sorted arrays. A “stage 2 mop-up” for hybrids.

Some runtimes use hybrid sorts. Chrome V8 uses Quick to ‘divide and conquer’ then switches to Insertion once ranges are 10 or less. Python uses TimSort, a hybrid of Merge and Insertion. The .NET framework and some C++ STLs use Introsort, a hybrid of Quick and Heap. Not to be outdone, Java hybrid-izes TimSort and Insertion.
 
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
