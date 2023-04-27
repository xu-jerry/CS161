# Lecture 8

## Semantics
- $w \models \alpha$
  - sentence $\alpha$ is true at world w
  - w satisfies $\alpha$
  - w entails $\alpha$

## Models
- $M(\alpha)=\{w:w\models \alpha\}$
- counter models:
  - $M(\neg\alpha)$
- $\alpha$ and $\beta$ are equivalent if
  - $M(\alpha) = M(\beta)$
- $\alpha$ is inconsistent/unsatisfiable if 
  - $M(\alpha) = \empty$
- $\alpha$ is tautology/vacuous/valid:
  - $M(\alpha) = W$
- $\alpha$, $\beta$ are mutually exclusive (never true together)
  - $M(\alpha) \cap M(\beta) = \empty$
- $\alpha$, $\beta$ are exhaustive
  - $M(\alpha) \cup M(\beta) = W$
- $\beta$ follows from $\alpha$
  - aka $\alpha$ implies $\beta$
  - aka $\alpha$ entail $\beta$
  - $M(\alpha) \subseteq M(\beta)$
- $M(\alpha \cap \beta) = M(\alpha) \cap M(\beta)$
- $M(\alpha \cup \beta) = M(\alpha) \cup M(\beta)$
- $M(\alpha) = \overline{M(\neg \alpha)}$
- Example:
  - $(E \cup B) \implies A$
  - $(\neg E \cap \neg B) \cup A$
  - E: 1, 2, 3, 4
  - B: 1, 2, 5, 6
  - A: 1, 3, 5, 7

## Inference
- "deduction"
- given (knowledge base)
  - $\alpha_1, \alpha_2, \dots, \alpha_n$ - set
  - $\Delta = \alpha_1 \cap \alpha_2 \cap \dots \cap \alpha_n$ - single sentence
- Question: Does sentence $\alpha$ from KB $\Delta$?
- truth table, model enumeration
  - $\Delta \models \alpha$ iff $M(\Delta) \subseteq M(\alpha)$
  - inference rules
  - reduction to SAT
  - conversion to normal forms (knowledge compilation)

## Aside
- $\Delta \models \alpha$ is a relation
- $\Delta \implies \alpha$ is a sentence

## Refutation Theorem
- $\Delta \models \alpha$ iff $\Delta \wedge \neg \alpha$ is inconsistent

## Inference
- Modus Ponens
$$\frac{\alpha, \alpha \implies \beta}{\beta}$$
- or-introduction 
$$\frac{\alpha, \beta}{\alpha \vee \beta}$$
- and-introduction 
$$\frac{\alpha, \beta}{\alpha \wedge \beta}$$
- Modus Tollens 
$$\frac{\alpha \implies \beta, \neg \beta}{\neg \alpha}$$
- New notation:
$$\Delta \vdash_R \alpha$$
- means $\alpha$ can be derived from $\Delta$ using inference rules R

## Example
- Knowedlge base:
  - $\Delta = A \vee B, D \implies E$
- Query
  - $\alpha = A \vee B \vee  C$
$$\frac{\Delta \models \alpha}{R = \{r_1, r_2\}}$$

## Resolution (Inference Rule)
$$\frac{\frac{\alpha \vee \beta, \neg \beta \vee \gamma}{\alpha \vee \gamma}}{\frac{\neg \alpha \vee \beta, \beta \vee \gamma}{\neg\alpha \implies \gamma}}$$
- Resolution is "Refutation Complete" when applied to CNF (Conjunctive normal form)

## Another example
$$\frac{A \vee B, \neg B \vee C \vee D}{A \vee C \vee D}$$
- numerator are clauses, denominator is resolvent
- we resolved clause 1 + clause 2 on variable C

## Big boi example
- $\Delta$:
  - $(A \vee \neg B) \implies C$
  - $C \implies D \vee \neg E$
  - $E \vee D$
- $\alpha$:
  - $A \implies D$
- convert to CNF:
  - $\Delta$:
  - 0: $(\neg A \vee C)$
  - 1: $(B \vee C)$
  - 2: $(\neg C \vee D \vee \neg E)$
  - 3: $(E \vee D)$
  - $\neg \alpha$:
  - 4: $A$
  - 5: $\neg D$
- 6: $C$ - 0, 4 on A
- 7: $E$ - 5, 3 on D
- 8: $D \vee \neg E$ - 2, 6 on C
- 9: $D$ - 7, 8 on E 
- 10: contradiction - 5, 9