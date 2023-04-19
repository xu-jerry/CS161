# Lecture 6

## CSPs
- formulation as search
- backtracking search strategy (dfs)
- improvements

## Variable and Value Ordering
- Variables X, Y, Z
- value 0, 1
- constraints X = Y, Y = Z
- two solutions
  - X = Y = Z = 0
  - X = Y = Z = 1
- heuristic: rule of thumb, intuition

## Variable Ordering
- X, Z, Y
- much less branches

## Example
- back to australia map
- choose most constrained variable, variable with the fewest legal values
- value ordering heuristic: choose least constraining value
- choose value that rules out the fewest values of remaining variables
- tree structure is 6th one

## Two player games
- terminal state
- score for x, utility
- game tree
- max triangle: maximize
- min upside down triangle: minimize
- minimax algorithm

## Chess
- B = 35
- million nodes
- depth of 4
- pruning: don't have to look at every node