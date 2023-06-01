# Lecture 16

## Learning
- Learning parameters under complete data
- incomplete data
  - Em algorithm
- learning structure

## Learning models
- learn a model (generative learning, unsupervised)
  - unlabeled data
- learning a query (discriminative learning, supervised)
  - labeled data
  - learn a classifier
  - examples:
    - decision trees
    - random forests

## Entropy
- higher is more even
- lowest is spike
- formula is 
$$ENT(X) = \sum_x Pr(x)*log_ePr(x)$$
$$ENT(X|y) = -\sum_xPr(x|y)log_ePr(x|y)$$ 
- ^ this one might increase!
$$ENT(X|Y) = -\sum_yPr(y)ENT(X|y)$$
$$ENT(X|Y) \leq ENT(X)$$
- Example
$$ENT(B) = 0.788$$
$$ENT(B|A) = ENT(B|a)Pr(a) + ENT(B|\bar{a})Pr(\bar{a}) = 0.329 < 0.788$$

## How entropy helps
- conditional entropy can affect order of nodes in trees
- entropy 0 if 100% for one choice
- entropy 1 if equal for each
- maximize information gain / minimum entropy at the end

## Ensemble learning
- start with dataset, 