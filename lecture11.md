# Lecture 11

## First-Order Logic [Inference]
- Reducing FOL inference to propositional
- simple/restricted methods
  - forward chaining
  - backward chaining (prolog)
- KB - definite clauses, no function symbols
- Resolution

## Universal Instantiation (UI)
- $\forall x$ king($x$) $\wedge$ Greedy($x$) $\implies$ Evil($x$)
- $$\frac{\forall x \alpha}{sub(\{x/9\}, \alpha)}$$
  - ground term, cannot be variable
- King(John) $\wedge$ Greedy(John) $\implies$ Evil(John)
- no function symbols
- unique-name assumption
- closed-world assumption

## Existential Instatiation (EI)
- $\exists$ Crown(x) $\wedge$ OnHead(x, John)

## Herbrand (1950)
- If sentence $\alpha$ is entailed by a FOL KB, then it is entailed by a finite subset of the propositional KB.

## Horn clause
- at most one positive literal

## Definite clause
- exactly one positive literal

## Forward chaining
- use tree, start from leaves
- con: creates a lot of unnecessary things

## Backward chaining
- start from top, basically depth first search

## Unification
- knows(John, x), Knows(John, Jane)
- unification $\theta=\{x/Jane\}$

## Converting to CNF
- move negations inside
- there exists x, Dog(x) is the same as Dog(D) if D doesn't exist in knowledge base
- skolem constnt
- skolem function