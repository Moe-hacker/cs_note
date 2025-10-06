# Proposition (命题)

A **proposition** is a declarative sentence (陈述句) that is either *true* or *false*, but not both.  
Example: “It is raining” is a proposition because it can be either true or false.

> What about “This sentence is false”?  
> We assume this is *not* a proposition (it’s a paradox). Computers only handle boolean computations (布尔运算).

# Logical Connectives (逻辑连接词)

Logical connectives are symbols (符号) or words used to connect propositions to form more complex statements (复合语句):

- **AND** (∧, 与, 合取): “p AND q” is true if both p and q are true (conjunction, 合取)
- **OR** (∨, 或, 析取): “p OR q” is true if at least one of p or q is true (disjunction, 析取)
- **NOT** (¬, 非, 否定): “NOT p” is true if p is false (negation, 否定)
- **IMPLIES** (→, 蕴含, 条件): “p IMPLIES q” is true if whenever p is true, q is also true (conditional, 条件)
- **IF AND ONLY IF** (↔, 当且仅当, 双条件): “p IF AND ONLY IF q” is true if p and q are both true or both false (biconditional, 双条件)

> Note: Some use `~` for NOT (否定符号); `!` is common in programming but may not be accepted in exams.

# Truth Table (真值表)

For implication (蕴含), “p IMPLIES q” is false only when p is true and q is false; otherwise, it is true.

| p     | q     | p → q |
|-------|-------|-------|
| True  | True  | True  |
| True  | False | False |
| False | True  | True  |
| False | False | True  |

**Why?**  
If a teacher says, “If you study hard, you will pass the exam”:
- Study hard and pass: true
- Study hard and fail: false
- Don’t study hard but pass: true (condition not met)
- Don’t study hard and don’t pass: true (condition not met)

# Logical Equivalence (逻辑等价)

Two propositions are **logically equivalent** if they have the same truth value (真值) in every possible scenario, denoted as `p ≡ q`.

Example: “p → q” and “¬p ∨ q” are logically equivalent.

| p     | q     | p → q | ¬p    | ¬p ∨ q |
|-------|-------|-------|-------|--------|
| True  | True  | True  | False | True   |
| True  | False | False | False | False  |
| False | True  | True  | True  | True   |
| False | False | True  | True  | True   |

# De Morgan’s Laws (德摩根定律)

De Morgan’s Laws relate conjunctions and disjunctions through negation:

- ¬(p ∧ q) ≡ ¬p ∨ ¬q
- ¬(p ∨ q) ≡ ¬p ∧ ¬q

# Predicates and Quantifiers (谓词和量词)

A **predicate** is a function (函数) that takes arguments (参数) and returns a proposition.  
Example: “is_even(x)” returns true if x is even.

**Quantifiers** indicate the scope of a predicate:

- **Universal quantifier** (∀, 全称量词): “∀x P(x)” means “for all x, P(x) is true.”
- **Existential quantifier** (∃, 存在量词): “∃x P(x)” means “there exists an x such that P(x) is true.”

Example:  
“∀x (is_even(x) → is_integer(x))” means “for all x, if x is even, then x is an integer.”  
“∀x(Lecture(x) → ∃y Teaches(y, x))” means “Every lecture teaches at least one subject.”


# Negation of Quantifiers (量词的否定)

- The negation of “∀x P(x)” is “∃x ¬P(x)” (“there exists an x such that P(x) is false”)
- The negation of “∃x P(x)” is “∀x ¬P(x)” (“for all x, P(x) is false”)

Example:  
Negation of “∀x (is_even(x) → is_integer(x))” is “∃x (is_even(x) ∧ ¬is_integer(x))”

# Modus Tollens (否定后件)

A valid argument form:

- If p → q
- ¬q
- Therefore, ¬p

Example:  
If it is raining, then the ground is wet.  
The ground is not wet.  
Therefore, it is not raining.

# Modus Ponens (肯定前件)

Another valid argument form:

- If p → q
- p
- Therefore, q

Example:  
If it is raining, then the ground is wet.  
It is raining.  
Therefore, the ground is wet.

# Converse (逆命题)

The **converse** of “p → q” is “q → p”.  
The truth of the converse is not guaranteed by the original statement.

Example:  
“If it is raining, then the ground is wet.”  
Converse: “If the ground is wet, then it is raining.” (May be false.)

# Contrapositive (逆否命题)

The **contrapositive** of “p → q” is “¬q → ¬p”.  
The contrapositive is logically equivalent to the original statement.

Example:  
“If it is raining, then the ground is wet.”  
Contrapositive: “If the ground is not wet, then it is not raining.”

# Affirming the Consequent (肯定后件)

A logical fallacy:

- If p → q
- q
- Therefore, p (**invalid**)

Example:  
If it is raining, then the ground is wet.  
The ground is wet.  
Cannot conclude it is raining (could be another reason).

# Denying the Antecedent (否定前件)

Another logical fallacy:

- If p → q
- ¬p
- Therefore, ¬q (**invalid**)

Example:  
If it is raining, then the ground is wet.  
It is not raining.  
Cannot conclude the ground is not wet (could be another reason).