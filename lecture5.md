# Lecture 5

## Constraint Satisfaction Problems (CSP)
- standard formulation of CSPs as search
- standard search strategy
- improvements: six total

## CSP
- set of variables X1, ..., Xn
- value D1, ..., Dn
- constraints: allowable combination of values
- example of problem: coloring a map with some colors, no bordering regions have same color
- solution: WA = red, etc.

## types of constraints
- unary: one variable
- binary: two variables
- higher-order constraints: > 2 variables
- hard constraint
- soft constraint: satisfy as many constraints you can
- constraint graph (binary CSPs)
  - primal graph
  - tree width

## Satisfiability (SAT)
- variables X1, ... Xn
- values 0/1, T/F
- P2, reduce to P1, solve to get solution, if P1 can solve efficiently, then P2 can solve efficiently
- NP complete means being able to solve them means u can solve all NP problems
- SAT is prototypical problem

## CSP on Search
- Search Problem
  - IS
  - FS (test)
  - actions (successor fn)
- State
  - partial variable assignment
  - {X = T, Z = F}
  - {X = F, Y = T, Z = F} - complete
  - {Z = T}
  - {} - empty
- 6 children, depending on which variable and which value
- use symmetry to choose X, Y, Z in order, to reduce number of total nodes
- DFS, since all solutions are same depth, optimal and complete
- backtracking search

## Ways to be more efficient
1. A. No constraint is violated
2. a
3. a
4. B. forward checking
5. C. arc consistency
6. a

## Forward checking
- maintain a set of positive values for each variable
- when you assign a value to a variable, update possible values for other vars
- declare "bad state" if some variable loses all its values

## Arc consistency (Binary CSPs)
- if constraint between two states, there are arcs between them
- arc X->Y is consistent means:
  - for every possible value of X, there is a compatible value for Y
  - make every arc consistent by removing possible values
- to check a particular arc: d^2
- maximum number of times you can check an arc
- can check an arc up to d times, since X->Y, Y can lose values d times
- O(n\*d^2\*d^2)