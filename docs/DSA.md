# **DSA**

## **Array**

### Quick reference

|        | Worst Case   |
| ------ | ------------ |
| space  | O(n)O(n)O(n) |
| lookup | O(1)O(1)O(1) |
| append | O(1)O(1)O(1) |
| insert | O(n)O(n)O(n) |
| delete | O(n)O(n)O(n) |

An array organizes items sequentially, one after another in memory.

Each position in the array has an **index**, starting
 at 0.

#### Strengths:

- **Fast lookups**. Retrieving the element at a
   given index takes O(1)O(1)O(1) time,
   regardless of the length of the array.

- **Fast appends**. Adding a new element at the
   end of the array takes O(1)O(1)O(1) time.

#### Weaknesses:

- **Fixed size**. You need to specify how many
   elements you're going to store in your array ahead of time.
   (Unless you're using a fancy dynamic array.)

- **Costly inserts and deletes.** You have to ["scoot over" the other elements to fill in or close gaps](https://www.interviewcake.com/concept/python/array?#inserting), which takes worst-case O(n)O(n)O(n) time.

## **Queue**

### Quick reference

|         | Worst Case   |
| ------- | ------------ |
| space   | O(n)O(n)O(n) |
| enqueue | O(1)O(1)O(1) |
| dequeue | O(1)O(1)O(1) |
| peek    | O(1)O(1)O(1) |

A **queue** stores items in a first-in, first-out
 (FIFO) order.

Picture a queue like the line outside a busy restaurant. First come, first served.

#### Strengths:

- **Fast operations**. All queue operations take
   O(1)O(1)O(1) time.

#### Uses

- **[Breadth-first search](https://www.interviewcake.com/concept/bfs)** uses a queue to keep track of the nodes to visit next.

- **Printers** use queues to manage jobs—jobs get printed in
   the order they're submitted.

- **Web servers** use queues to manage requests—page requests get fulfilled in the order they're received.

- **Processes** wait in the CPU scheduler's queue for their turn to run.

## **Linked List**

### Quick reference

|         | Worst Case   |
| ------- | ------------ |
| space   | O(n)O(n)O(n) |
| prepend | O(1)O(1)O(1) |
| append  | O(1)O(1)O(1) |
| lookup  | O(n)O(n)O(n) |
| insert  | O(n)O(n)O(n) |
| delete  | O(n)O(n)O(n) |

A **linked list** organizes items sequentially, with each item
 storing a pointer to the next one.

Picture a linked list like a chain of paperclips linked together. It's 
quick to add another paperclip to the top or bottom. It's even quick to 
insert one in the middle—just disconnect the chain at the middle link, 
add the new paperclip, then reconnect the other half.

An item in a linked list is called a **node**. The first node is called the **head**. The last node is called the **tail**.

#### Strengths:

- **Fast operations on the ends**. Adding elements
   at either end of a linked list is O(1)O(1)O(1).
   Removing the first element is also O(1)O(1)O(1).

- **Flexible size**. There's no need to specify
   how many elements you're going to store ahead of time. You
   can keep adding elements as long as there's enough space
   on the machine.

#### Weaknesses:

- **Costly lookups**. To access or edit an item
   in a linked list, you have
   to take O(i)O(i)O(i) time to walk
   from the head of the list to the iiith
   item.

## **Hash Maps**

### Quick reference

|        | Average      | Worst Case   |
| ------ | ------------ | ------------ |
| space  | O(n)O(n)O(n) | O(n)O(n)O(n) |
| insert | O(1)O(1)O(1) | O(n)O(n)O(n) |
| lookup | O(1)O(1)O(1) | O(n)O(n)O(n) |
| delete | O(1)O(1)O(1) | O(n)O(n)O(n) |

A **hash table** organizes data so you can quickly
 look up values for a given
 key.

#### Strengths:

- **Fast lookups**. Lookups
   take O(1)O(1)O(1) time *on
   average*.

- **Flexible keys**. Most data types can be
   used for keys, as long as
   they're [hashable](https://www.interviewcake.com/concept/hashing).

#### Weaknesses:

- **Slow worst-case lookups**. Lookups
   take O(n)O(n)O(n) time *[in the worst
   case](https://www.interviewcake.com/concept/python/hash-map?#when-lookups-cost-o-n)*.

- **Unordered**. Keys aren't stored in a
   special order. If you're looking for the smallest key, the
   largest key, or all the keys in a range, you'll need to
   look through every key to find it.

- **Single-directional lookups**. While you can
   look up the *value* for a given key
   in O(1)O(1)O(1) time, looking up
   the *keys* for a given *value* requires looping
   through the whole dataset—O(n)O(n)O(n) time.

- **Not cache-friendly**. Many hash table implementations
   use [linked lists](https://www.interviewcake.com/concept/linked-list),
   which don't put data next to each other in memory.

## **Trees**

### Quick reference

A **tree** organizes values hierarchically.

![A tree of animals and their classes. The root node is the Animal kingdom, and its children are the classes Reptile and Mammal. These classes are further split up into specific types such as Lizards, Snakes, Birds, etc.](https://www.interviewcake.com/images/svgs/trees__animal_classes.svg?bust=209) 

Each entry in the tree is called a **node**, and every node links
 to zero or more child nodes.

If you flip the picture upside down, it kind of looks like a tree.
 That's where the name comes from!

#### Example uses:

- **Filesystems**—files inside folders inside folders

- **Comments**—comments, replies to comments, replies to replies

- **Family trees**—parents, grandparents, children, and grandchildren

### Leaves, Depth, and Height

**Leaf nodes** are nodes that're on the bottom of the tree (more formally: nodes that have no children).

Each node in a tree has a **depth**: the number of links
 from the root to the node.

A tree's **height** is the number of links from
 its root to the furthest leaf. (That's the same as the
 maximum node depth.)

![A tree with a height of 4. Each depth is labeled, starting with the root at depth 0, then the next level at depth 1, and so on until the last level at depth 4.](https://www.interviewcake.com/images/svgs/trees__depth_height.svg?bust=209) 

### Tree Traversals

#### Breadth First Search (BFS)

In a [BFS](https://www.interviewcake.com/concept/bfs), you first explore all the nodes one step away, then all
 the nodes two steps away, etc..

Breadth-first search is like throwing a stone in the center of a 
pond. The nodes you explore "ripple out" from the starting point.

Here's a sample tree, with the nodes labeled in the order they'd be
 visited in a BFS.

![A tree with a root node labeled 1. The root's left child is labeled 2 and its right is labeled 3. The left child of 2 is labeled 4 and the right is labeled 5. The left child of 3 is labeled 6 and the right 7. The left child of 5 is labeled 8 and the right is labeled 9.](https://www.interviewcake.com/images/svgs/trees__bfs.svg?bust=209) 

#### Depth First Search (DFS)

In a [DFS](https://www.interviewcake.com/concept/dfs), you go as deep as possible down one path before backing
 up and trying a different one.

Depth-first search is like walking through a corn maze. You explore
 one path, hit a dead end, and go back and try a different one.

Here's a how a DFS would traverse the same example tree:

![A tree with a root node labeled 1. The root's left child is labeled 2 and its right is labeled 7. The left child of 2 is labeled 3 and the right is labeled 4. The left child of 4 is labeled 5 and the right is labeled 6. The left child of 7 is labeled 8 and the right is labeled 9.](https://www.interviewcake.com/images/svgs/trees__dfs.svg?bust=209) 

**Comparing BFS and DFS**

- A BFS will find the **shortest path** between the
   starting point and any other reachable node. A depth-first
   search will not necessarily find the shortest path.

- Depth-first search on a binary tree *generally* requires less memory than breadth-first.

- Depth-first search can be easily implemented with recursion.

You can also use BFS and DFS on [graphs](https://www.interviewcake.com/concept/graph).

#### Pre Order Traversal

Visit the current
 node, then walk the left subtree, and finally walk the right
 subtree.

A pre-order traversal usually visits nodes in the same order as a
 DFS.

![A tree with the same nodes as the depth first search tree. The root node is labeled 1, its left child labeled 2 and its right labeled 7. The left child of 2 is labeled 3 and the right is labeled 4. The left child of 4 is labeled 5 and the right is labeled 6. The left child of 7 is labeled 8 and the right is labeled 9.](https://www.interviewcake.com/images/svgs/trees__pre_order_traversal.svg?bust=209) 

#### In Order Traversal

Walk the left subtree
 first, then visit the current node, and finally walk the
 right subtree.

Of all three traversal methods, this one is probably the
 most common. When walking a binary search tree, an in
 order traversal visits the nodes in sorted, ascending
 order.

![A tree with a root node labeled 6. The root's left child is labeled 2 and its right is labeled 8. The left child of 2 is labeled 1 and the right is labeled 4. The left child of 4 is labeled 3 and the right is labeled 5. The left child of 8 is labeled 7 and the right is labeled 9.](https://www.interviewcake.com/images/svgs/trees__in_order_traversal.svg?bust=209) 

#### Post Order Traversal

Walk the left subtree,
 then the right subtree, and finally visit the current node.

This one's kind of rare ... but it shows up in some parsing
 algorithms,
 like [Reverse
 Polish Notation](https://en.wikipedia.org/wiki/Reverse_Polish_notation).

![A tree with a root node labeled 9. The root's left child is labeled 5 and its right is labeled 8. The left child of 5 is labeled 1 and the right is labeled 4. The left of 4 is labeled 2 and the right is labeled 3. The left child of 8 is labeled 6 and the right is labeled 7.](https://www.interviewcake.com/images/svgs/trees__post_order_traversal.svg?bust=209) 

### Binary Trees

A **binary tree** is a tree where every node has at most two children.

![The letters of the alphabet (up to Q) represented in a non-binary tree on the left and a binary tree on the right. The binary tree has at most two children per node whereas the non-binary tree has up to 8.](https://www.interviewcake.com/images/svgs/trees__binary_non_binary.svg?bust=209) 

### Full binary trees

A **full binary tree** is a binary tree where
 every node has exactly 0 or 2 children.

![A binary tree with 6 nodes, each with either 0 or 2 children.](https://www.interviewcake.com/images/svgs/trees__full_binary.svg?bust=209) 

#### Perfect binary trees

A **perfect binary tree** doesn't have room for
 any more nodes—unless we increase the tree's
 height.

![A binary tree where every node except the leaves has two children, and all the leaf nodes are at the same depth.](https://www.interviewcake.com/images/svgs/trees__perfect_binary.svg?bust=209) 

#### Complete binary trees

A **complete binary tree** is like a perfect binary tree
 missing a few nodes in the last level. Nodes are
 filled in from left to right.

Complete trees are the basis for heaps and priority queues.

![A binary tree where every level except the last is completely filled and each node has either 0 or 2 children.](https://www.interviewcake.com/images/svgs/trees__complete_binary.svg?bust=209) 

#### Balanced binary trees

A **balanced binary tree** is a tree whose
 height is small relative to the number of nodes it has. By
 small, we usually mean the height
 is O(lg(n))O(lg(n))O(lg(n)),
 where nnn is the number of nodes.

Conceptually, a *balanced* tree "looks full,"
 without any missing chunks or branches that end much
 earlier than other branches.

There are few different definitions of balanced depending
 on the context. One of the most common definition is that
 a tree is balanced if: (a) the heights of its left and
 right subtrees differ by at most 1, and (b) both subtrees
 are also balanced.

![A balanced binary tree on the left, and an unbalanced binary tree on the right. The balanced tree looks full, with the subtrees to the left and right of the root node both ending at the same depth. The unbalanced tree has only one node to the left of the root and 3 to the right, ending at depth 3.](https://www.interviewcake.com/images/svgs/trees__balanced_unbalanced_binary.svg?bust=209) 

Similar definitions can be used for trees that have more than two
 children. For instance, a full *ternary* tree (with up to
 three children per node) is a tree where every node has zero or 
three children.

### Relationship between height and number of nodes

In perfect binary trees there's a cool mathematical relationship between the number of nodes and the height of the tree.

First, there's a pattern to how many nodes are on each level:

1. Level 000: 20=12^0=120=1 nodes,

2. Level 111: 21=22^1=221=2 nodes,

3. Level 222: 22=42^2=422=4 nodes,

4. Level 333: 23=82^3=823=8 nodes,

5. *etc
   *

Let's call the total number of nodes in the tree nnn, and the
 height of the tree hhh.

We could solve for nnn by adding up the number of nodes on each level in the tree:

n=20+21+22+23+...+2h−1=2h−1n = 2^0 + 2^1 + 2^2 + 2^3 + ... + 2^{h-1} = 2^{h} - 1n=20+21+22+23+...+2h−1=2h−1

Solving for hhh in terms of nnn,
 we get:

n=2h−1n = 2^{h} - 1n=2h−1 n+1=2hn + 1 = 2^{h}n+1=2h log⁡2((n+1))=log⁡2(2h)\log_{2}{((n+1))} = \log_{2}{(2^{h})}log2​((n+1))=log2​(2h) log⁡2(n+1)=h\log_{2}{(n+1)} = hlog2​(n+1)=h

That's the relationship between a perfect binary tree's height and
 the number of nodes it has.

This is the intuition behind our definition of balanced that
 we used above. A perfect tree is balanced, and in a perfect
 tree the height grows logarithmically with the number of
 nodes.
