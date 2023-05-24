# Lecture 15

## Class variables
- C
- have children $A_1, A_2, \cdots, A_n$
  - "attributes"

## Naive Bayes Structure
- Naive Bayes Classifier
- $Pr(C|A_1, A_2, \cdots, A_n)$
- "Instance"
  - $a_1, a_2, \cdots, a_n$
- $Pr(C=yes|a_1, \cdots, a_n) \ge 0.5$ -> true, else false
- $$Pr(c|a_i, a_j) = \frac{Pr(a_i, a_j|c)Pr(c)}{Pr(a_i, a_j)} = \frac{Pr(a_i|c)Pr(a_j|c)Pr(c)}{Pr(a_i, a_j)}$$
$$= \frac{Pr(a_i|c)Pr(a_j|c)Pr(c)}{\sum_{c'} Pr(a_i, a_j|c')Pr(c')} = \frac{Pr(a_i|c)Pr(a_j|c)Pr(c)}{\sum_{c'} Pr(a_i|c')Pr(a_j|c')Pr(c')}$$

## Example
- given title, probability if you'll like the movies

## Sickness example
- 4 parameters
- 2 independent parameters
- CPTs1->BN1->Pr1

## Learning
- parameters
  - complete data
  - incomplete data
- structure

## Initially
- CPT1 -> Pr1 arbitrary