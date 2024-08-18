# Truth-Eliminability-Sorting-Algorithm

*WIP*

For: ***Classical Extensions of Kripke-Feferman: Constraint Satisfaction and Alethic Paradox***

> https://www.thoughtscript.io/papers/000000000013

> Mirrored: https://thoughtscript-io.onrender.com/papers/000000000013.html

There's widespread consensus that no offered solution to the **Liar Paradox** gets all of the following:
1. All the other **Alethic Paradoxes**: *Yablo-Visser*, *Liar Cycles*, *Revenge Sentences*, *Boolean Compounds*, *Curry Compounds*, *McGee Sentences*, etc.
2. No ***touted*** "philosophical (non-formal/mathematical) solution" can prove its formal correctness (**Soundness**, **Completeness**, **Consistency**, Metalogical Theorems, address **Tarski's Undefiniability Theorem**, etc.). (These are mostly what you'd find on the SEP article about the **Liar Paradox**.)
3. No formal solution can explain the big "philosophical why" (it must explain the problem) while addressing issues of formal correctness. It mustn't just be an ad-hoc trick of mathematical machinery.
4. No solution offers both a "philosophical explanation" and formal proof of its correctness.
5. Additionally, no formal solution is known to overcome all of the existing concerns: **Bacon 2015**, **Revenge Paradox**, etc.

(Optionally) Adding to the above: 

6. Is **Classical** (preserves **Bivalence** and the other **Classical** validities).

## Definitions

Formal definitions.

> Consult **Section 3.2** for an overview of **Truth as a Metalinguistic Predicate**.

### Sentences Names, Name-Forming Operators, and Diagonalization

Here and below I’ll use the convention `⟨`,`⟩` to denote the familiar **Gödel Numbering** technique:

1. **Sentence Name** - the **Name** of a **Sentence** (e.g. - a **Variable Name** in Computer Science) `P` for a **Sentence** `S` shall be written: `P := S`.
2. **Name-Forming Operator** - `⟨S⟩` represents the mapping of some **Sentence**, **Proposition**, or **Expression** `S` to its **Name**. `⟨S⟩ ≡ P := S` returning `P`.
3. **Diagonalization** - a **Technique** that associates the **Fixed Point** of a **Sentence** containing `S` as a sub-expression so that `S` is its own name.

> This should come as no surprise since it forms the historical and mathematical basis for Variable Naming, Memory Addressing, and Value Assignment within programming languages.

### T-Scheme

1. *Tarski’s 1933 **Definition of Truth***  - `For all x, True(x) if and only if ϕ(x)`.
2. **Modern Formulation** - (For all `S`) `T(⟨S⟩) ↔ S`:
   * **Capture** (or **T-Intro**) - conditional subrule of the **T-Scheme** biconditional. The rule going from `S` to `T(⟨S⟩)`.
   * **Release** - conditional subrule of the **T-Scheme** biconditional. The rule going from `T(⟨S⟩)` to `S`.

### Truth Tellers

```
S := T(⟨S⟩)
```

1. **Truth Teller** - like the **Liar Sentence** but expressing **Truth** of itself. Constructed via **Fixed-Point Diagonalization** like the **Liar Sentence**.

### Alethic Paradox

> From [Dictionary.com](https://www.dictionary.com/browse/alethic): **Alethic** "of or relating to such philosophical concepts as truth, necessity, possibility, contingency, etc".
1. **Alethic Paradox** - for any sentence `S`: The shortest proof resulting in **Contradiction** that requires the use of **T-Scheme** (**F-Schema**, or our other **Alethic** inferences including proven biconditionals involving the
**Truth Predicate**).

### Properties of Truth and T-Schema

1. **Truth Transparency** - the principle that `S` and `T(⟨S⟩)` are always and everywhere intersubstitutable.
2. **Truth Eliminability** - (W.R.T. to **T-Scheme**) in rewriting `T(⟨S⟩)` in the lexiographical form `S` (via **Truth Transparency**) `S` *must* contain content that *doesn’t* predicate **Truth**.
   * A stronger criterion on (or reading of) **Truth Transparency** (and **T-Scheme**).
   * **Truth Transparency** requires that `T(⟨S⟩)` can be rewritten in a form where no `T` appears (where **Truth** is not predicated).
3. **Truth Opacity** - when a **Sentence** `S` cannot be rewritten (via **Truth Transparency**) without a `T` appearing (where **Truth** is not predicated). Such a **Sentence** is **Truth Opaque**.

## Truth Eliminability Algorithm and KFG

A Finite, **Sorting**, Algorithm used to determine whether a **Sentence** is **Truth Opaque** or not.

May circumvent general concerns stemming from **Bacon 2015** (my original paper was never published):
* Appears to be a new "species" of **Restrictionist** approaches that also doesn't require every **Sentence** or **Theorem** to be "Cleaned", "Healthy", or "Debuggered".
  * E.g. - those approaches that follow the Classical Axiom, Theorem, and Tautology: **Weakening** `P → (Q → P)`.
  * The **T-Scheme** is actually a **Material Conditional** with some **Constraint**, "Checkpoint", or condition that must be met / a "Restriction" on it.
* Invalidates the move from **P1** to **P2** (by Substitution or Diagonalization).
* Sorted expressions are nevertheless given **Truth-Values** and don't entail **Untruth** (or **Falsity**).
* So, both **Truth Opaque** and non-**Truth Opaque Sentences** are allowed - they are not "banned" or "outlawed".
* Not clear that **Diagonalization** is legitimate for such **Sorted Expressions**. In the original papers by Gödel, **Diagonalization** is justified only up to and for *primitive recursive number-theoretic function*(s). As such, it's not clear a **Revenge**-type **Sentence** can be constructed at all for **KFG**.
* **Truth Opaque Expressions** aren't necessarily **Theorems** nor are the assertions of them as such.
* The conclusion of the argument is essentially that **KFG** will prove a Theorem that's **Truth Opaque**.  Consider the unproblematic Sentence: `S := T(S) → T(S)` - it's a Theorem, receives Truth Values, and is **Truth Opaque**.

Blocks **McGee's T-Intro** step.

Satisfies **Tarski's Undefinability Theorem** for **T-Scheme** since `S` and `T(⟨S⟩)` can be **Logically Consistent** yet diverge in Truth Values within **KFG**.

## Some Validations and Truth Table Proofs

Some simple **Truth Table** and basic Model checking summarized succinctly below.

> Depicts some Models of **KFG** and proves **Consistency** of **KFG** with respect to **Liar Cycles**.

> Demonstrates Classically Consistent Models (the primary goal) and ways to address the ancillary goals: **KFG** global validity and embedded **Catuṣkoṭi**.

### Truth Assignments 

The **Truth-Value** for `S ∈ C` is determined by the **Truth Opacity** of a **Sentence** and prior to **Truth-Assignments**. (It's a constraint on the **Interpretation Function** itself as specified in the Draft Paper.)

> Below, `T(S) ↔ S` refers to the specific WFF with Sentential Constant `S` substituted into **T-SCHEME**.

### Truth Eliminable Sentences

Truth Table Semantics:

| `S` | `¬S` | `C(S)` (`S ∈ C`) | `¬C(S)` | `T(S)` | `¬T(S)` | `T(S) ↔ S` | `C(S) → (T(S) ↔ S)` | 
| --- | --- | --- | --- | --- | --- | --- | --- |
| `⊥` | `⊤` | `⊤` | `⊥` | `⊤`* | `⊥`* | `⊥`* | `⊥`* |
| `⊥` | `⊤` | `⊤` | `⊥` | `⊥` | `⊤` | `⊤` | `⊤` |
| `⊤` | `⊥` | `⊤` | `⊥` | `⊤` | `⊥` | `⊤` | `⊤` |
| `⊤` | `⊥` | `⊤` | `⊥` | `⊥`* | `⊤`* | `⊥`* | `⊥`* |

There are two ways to read this:

1. *Modus Tollens* on the **Argument from Tautology**. If **T-SCHEME** is a **Tautology** then so too is `Q → T-SCHEME`. If `Q → T-SCHEME` isn't a **Tautology** then neither is **T-SCHEME** (which is precisely what `Q → T-SCHEME` is showing in the first place - e.g. **Weakened T-SCHEME**). On this view, both **T-SCHEME** and **KFG** are **Contingent**.
2. The fourth and first **Interpretation** above can be ruled out by additional (optional) extensions that modify how the **Interpretation Function** behaves (this is the route primarily endorsed by the Draft Paper but isn't the only route available. In the original Draft, `S` and `T(S)` are harmonized through additional rules added to the construction step of `C(S)` that convert `*` to the second or third interpretation.) prior to **Truth Assignment** itself (akin to the way that the Truth of **Logical Connectives** are calculated after **Atomic Proposition Truth Assignment** and **ZFC Set Theory** which has a complicated setup for the **Domain of Discourse** - both **ZFC Set Theory** and **Zero-Order Logic** are part of **KFG**).

### Truth Opaque Sentences

Truth Table Semantics:

| `S` | `¬S` | `C(S)` (`S ∈ C`) | `¬C(S)` | `T(S)` | `¬T(S)` | `T(S) ↔ S` | `C(S) → (T(S) ↔ S)` |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `⊤` | `⊥` | `⊥` | `⊤` | `⊥` | `⊤` | `⊥` | `⊤` |
| `⊤` | `⊥` | `⊥` | `⊤` | `⊤` | `⊥` | `⊤` | `⊤` |
| `⊥` | `⊤` | `⊥` | `⊤` | `⊥` | `⊤` | `⊤` | `⊤` |
| `⊥` | `⊤` | `⊥` | `⊤` | `⊤` | `⊥` | `⊥` | `⊤` |

Comments:

1. **Truth Teller** (and **Liar Cycle Negator**) expressions are given the second or third **Interpretations** above.
2. **Liar Sentences** expressions are given the first or fourth **Interpretations** above.

### Liar Cycles

> `S := T(Q)`, `Q := ¬T(S)`

Here:
1. We only need to prove that *at least one* **Consistent Interpretation** exists.
2. The following pairs must share Truth-Values:
   * `S`, `T(Q)` 
   * `¬S`, `¬T(Q)`
   * `Q`, `¬T(S)` 
   * `¬Q`, `T(S)`

| `S` | `T(Q)` | `¬S` |  `¬T(Q)` | `Q` | `¬T(S)` |  `¬Q` | `T(S)` | **Consistent** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | 
| `⊤` | `⊤` | `⊤` | `⊤` | `⊤` | `⊤` | `⊤` | `⊤` | `NO` |
| `⊥` | `⊥` | `⊥` | `⊥` | `⊥` | `⊥` | `⊥` | `⊥` | `NO` |
| `⊤` | `⊤` | `⊥` | `⊥` | `⊤` | `⊤` | `⊤` | `⊤` | `NO` |
| `⊤` | `⊤` | `⊤` | `⊤` | `⊥` | `⊥` | `⊤` | `⊤` | `NO` |
| `⊤` | `⊤` | `⊤` | `⊤` | `⊤` | `⊤` | `⊥` | `⊥` | `NO` |
| `⊥` | `⊥` | `⊤` | `⊤` | `⊤` | `⊤` | `⊤` | `⊤` | `NO` |
| `...` | `...` | `...` | `...` | `...` | `...` | `...` | `...` | `NO` |
| `⊥` | `⊥` | `⊤` | `⊤` | `⊤` | `⊤` | `⊥` | `⊥` | `YES` |
| `⊤` | `⊤` |  `⊥` | `⊥` |  `⊥` | `⊥` | `⊤` | `⊤` | `YES` |

Note:
1. One of the paired **Sentences** can behave like the **Truth Teller**. (The **Liar Cycle Negator** of the pair.)
2. We also require (through optional extensions) that **T-SCHEME** fails if a **Sentence** refers to a another **Truth Opaque** Sentence.

#### Liar Cycle Semantics and KFG

Regarding the last two **Interpretations**:

| `S` | `¬S` | `C(S)` (`S ∈ C`) | `¬C(S)` | `T(S)` | `¬T(S)` | `T(S) ↔ S` | `C(S) → (T(S) ↔ S)` |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `⊥` | `⊤` | `⊥` | `⊤` | `⊥` | `⊤` | `⊤` | `⊤` |
| `⊤` | `⊥` | `⊥` | `⊤` | `⊤` | `⊥` | `⊤` | `⊤` |

| `Q` | `¬Q` | `C(Q)` (`Q ∈ C`) | `¬C(Q)` | `T(Q)` | `¬T(Q)` | `T(Q) ↔ Q` | `C(Q) → (T(Q) ↔ Q)` |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `⊤` | `⊥` | `⊥` | `⊤` | `⊥` | `⊤` | `⊥` | `⊤` |
| `⊥` | `⊤` | `⊥` | `⊤` | `⊤` | `⊥` | `⊥` | `⊤` |

Immediately above:
1. Each **Model** pairs the respective first and second **Interpretations**.
2. We observe that `Q` (the **Liar Cycle Negator** of the pair) behaves like **Truth Tellers**.

## Resources and Links

> *Non-Exhaustive (but sufficient for what's described in the contents of this README) - please see the Paper for a complete Bibliography*.

1. Bacon, A. Can the Classical Logician Avoid the Revenge Paradoxes? Philosophical Review. 124 pp. 299-352 (2015, 7)
1. Beall, J. A Neglected Deflationist Approach to the Liar. Analysis. 61, 126-129 (2001)
1. Beall, J. Prolegomenon to Future Revenge. Revenge Of The Liar: New Essays On The Paradox. pp. 1-30 (2007)
1. Feferman, S. Axioms for Determinateness and Truth. Review Of Symbolic Logic. 1, 204-217 (2008)
1. Kripke, S. Outline of a Theory of Truth. Journal Of Philosophy. 72, 690-716 (1975)
1. Priest, G. Doubt Truth to Be a Liar. (Oxford University Press, 2006)
1. Priest, G. Logic of Paradox. Journal Of Philosophical Logic. 8, 219-241 (1979)
1. Tarski, A. The Semantic Conception of Truth and the Foundations of Semantics. Philosophy And Phenomenological Research. 4, 341-376 (1943)




