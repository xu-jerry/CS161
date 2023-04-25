# Lecture 7

## Knowledge Representation & Reasoning (Logic)
- knowledge
- statement
- logic (KB)
- -> Logic deduction
- -> conclusion
- Expert Systems
- Commonsense reasoning

## Types of Logic
- symbolic: logic
- numeric: probability
- learn data
- neuro symbolic approach

## Example
- Pits: cells that are adjacent to a pit are breezy
- Wumpus: cells that are adjacent to wumpus are smelly
- can sometimes conclude where pits and wumpuses are

## Propositional Logic (Boolean)
- Syntax
- Semantic

## Syntax
- basic syntax
- normal forms

## Vocabulary
- variables: X1, ..., Xn
  - value: true/false, 1/0
- logical connectives
  - and, or, not, imply, equivalent
- rules
  - a variable is a sentence
  - if S is a sentence, then not S is a sentence
  - if S1, S2, are sentences, then all of the following are sentences:
    - S1 and S2
    - S1 or S2
    - S1 implies S2
    - S1 equivalent to S2
- S1 $\land$ S2 - conjunction
  - S1 is a conjunct
- S1 $\lor$ S2 - disjunction
  - S1 is a disjunct
- S1 $\implies$ S2 - implication
  - S1 is a premise antecedent
  - S2 is a 

## Rules
- De Morgan's
  - $\neg(\alpha \land \beta)=\neg\alpha \lor \neg\beta$
  - $\neg(\alpha \lor \beta)=\neg\alpha \land \neg\beta$
- Contraposition Laws
  - $\alpha \implies \beta = \neg \beta \implies \neg \alpha$

## Normal Forms
- Conjunctive normal form (CNF)
  - disjunction of literals is a clause
  - CNF is a conjunction of clauses
- disjunctive normal form (DNF)
  - conjunction of literals is a term
  - disjunction of terms
  - DNF
- Horn clause
  - has at most one positive literal
- Negation normal form (NNF)
  - literal is NNG
  - if S1, S2 are NNFs then
    - $S_1 \land S_2$
    - $S_1 \lor S_2$
    - are NNFs
- CNF and DNF are subsets of NNF
- CNF is universal

## Example
- $(B \land E) \implies A$
- $M(\alpha)$ = meaning, model of $\alpha$
- tautology