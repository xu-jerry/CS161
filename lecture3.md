# Lecture 3

## Problem
- searching problem: IS, FS, actions (successor function)
- search engine
  - uninformed, informed
- solution

## The Search Process
- !! on the midterm !!
- terminology:
  - fringe/frontier
  - expand
  - generate
- search tree
- expand - check if node is good, generate its children
- nodes on the fringe are waiting to be expanded
- a search strategy is a criterion for deciding which node on the fringe to expand next

## Evaluating Search Strategies
- completeness: does it find a solution if one evals?
- optimal: does it always find the least-cost solution?
- time complexity: number of nodes generated/expanded
- space complexity: maximum number of nodes in memory
- Parameters:
  - b, branching factor
  - d, depth of optimal solution
  - m, maximum depth of search tree

## In a tree
- depth, root is d = 0
- how many nodes for each depth? 2^d
- if branch factor is b, then b^d nodes for each depth
- $N(b, d) = 1+b+b^2+ ... +b^d = \frac{b^{d+1}-1}{b-1} \approx \frac{b^{d+1}}{b-1}=(\frac{b}{b-1})b^d=O(b^d)$
- the last level dominates, always greater than the rest of tree

## BFS - Breadth-First Search
- expand the the shallowest node first
- optimal? yes
- complete? yes
- time? $O(b^d)$
- space? $O(b^d)$

## DFS - Depth-First Search
- expand the deepest node first
- optimal? no
- complete? no
- time? $O(b^m)$
- space? $O(b*m)$

## Merging BFS and DFS
- keep on increasing the size of the tree you DFS over
- when hit l = d, you are done
- optimal? yes
- complete? yes
- time? $O(b^d * \frac{b}{b+1})$
  - since last level dominates
  - as the branching factor increases, the overhead diminishes
- space? $O(b*d)$