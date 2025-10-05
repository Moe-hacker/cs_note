# proposition(命题)：
A proposition is a statement (declarative sentence(陈述句)) that is either true or false, but not both. For example, "It is raining" is a proposition because it can be either true or false.
Btw, what about "This sentence is false."? 
We assume this is not a proposition.....just assume. Anyway, computer can only handle boolean computations (布尔运算).
Godel/Turing: WTF???????
# logical connectives(逻辑连接词)：
Logical connectives are symbols (符号) or words used to connect propositions to form more complex statements (复合语句). The most common logical connectives are:
- AND (∧) (与, 合取): "p AND q" is true if both p and q are true. This is also called conjunction (合取).
- OR (∨) (或, 析取): "p OR q" is true if at least one of p or q is true. This is also called disjunction (析取).
- NOT (¬) (非, 否定): "NOT p" is true if p is false. This is also called negation (否定).
- IMPLIES (→) (蕴含, 条件): "p IMPLIES q" is true if whenever p is true, q is also true. This is also called conditional (条件).
- IF AND ONLY IF (↔) (当且仅当, 双条件): "p IF AND ONLY IF q" is true if p and q are both true or both false. This is also called biconditional (双条件).
Seems that my teacher like to use ~ for logic NOT (否定符号), I prefer !, but this might not be acceptable in exams.
# truth table(真值表)：
For implication (蕴含), "p IMPLIES q" is false only when p is true and q is false; otherwise, it is true.
| p     | q     | p → q |
|-------|-------|-------|
| True  | True  | True  |
| True  | False | False |
| False | True  | True  |
| False | False | True  |
Why?
Assume a teacher tells you "If you study hard, you will pass the exam." If you study hard and pass the exam, the teacher's statement is true. If you study hard but fail the exam, the statement is false. If you don't study hard but still pass the exam, the statement is still considered true because the condition (studying hard) was not met. Finally, if you neither study hard nor pass the exam, the statement is also true because the condition was not met.
# logical equivalence(逻辑等价)：
Two propositions are logically equivalent if they have the same truth value (真值) in every possible scenario. This is denoted as p ≡ q.
For example, the propositions "p → q" and "¬p ∨ q" are logically equivalent because they have the same truth values in all possible cases.
| p     | q     | p → q | ¬p    | ¬p ∨ q |
|-------|-------|-------|-------|-------|
| True  | True  | True  | False | True  |
| True  | False | False | False | False |
| False | True  | True  | True  | True  |
| False | False | True  | True  | True  |
# De Morgan's Laws(德摩根定律)：
De Morgan's Laws describe the relationship between conjunctions and disjunctions through negation. They state that:
- The negation of a conjunction is the disjunction of the negations: ¬(p ∧ q) ≡ ¬p ∨ ¬q
- The negation of a disjunction is the conjunction of the negations: ¬(p ∨ q) ≡ ¬p ∧ ¬q
# predicates and quantifiers(谓词和量词)：
A predicate is a function (函数) that takes one or more arguments (参数) and returns a proposition. For example, "is even(x)" is a predicate that returns true if x is an even number and false otherwise.
Quantifiers are symbols (符号) used to indicate the scope of a predicate. The two most common quantifiers are:
- Universal quantifier (∀) (全称量词): "∀x P(x)" means "for all x, P(x) is true."
- Existential quantifier (∃) (存在量词): "∃x P(x)" means "there exists an x such that P(x) is true."
For example, "∀x (is even(x) → is integer(x))" means "for all x, if x is even, then x is an integer."
# negation of quantifiers(量词的否定)：
The negation of a universally quantified statement "∀x P(x)" is "∃x ¬P(x)", which means "there exists an x such that P(x) is false."
The negation of an existentially quantified statement "∃x P(x)" is "∀x ¬P(x)", which means "for all x, P(x) is false."
For example, the negation of "∀x (is even(x) → is integer(x))" is "∃x (is even(x) ∧ ¬is integer(x))", which means "there exists an x such that x is even and x is not an integer."
# Affirming the consequent(肯定后件)：
This is a logical fallacy (逻辑谬误) that occurs when one assumes that if "p → q" is true, and q is true, then p must also be true. This is not necessarily the case.
For example, consider the statements:
- If it is raining, then the ground is wet. (p → q)
- The ground is wet. (q)
From these statements, one cannot conclude that it is raining (p) because there could be other reasons for the ground being wet, such as someone watering the garden.
# Denying the antecedent(否定前件)：
This is another logical fallacy that occurs when one assumes that if "p → q" is true, and p is false, then q must also be false. This is also not necessarily the case.
For example, consider the statements:
- If it is raining, then the ground is wet. (p → q)
- It is not raining. (¬p)
From these statements, one cannot conclude that the ground is not wet (¬q) because there could be other reasons for the ground being wet, such as someone watering the garden.
# converse(逆命题)：
The converse of a conditional statement "p → q" is "q → p". The truth of the converse is not guaranteed by the truth of the original statement.
For example, the converse of "If it is raining, then the ground is wet" is "If the ground is wet, then it is raining." The converse may be false even if the original statement is true.
# contrapositive(逆否命题)：
The contrapositive of a conditional statement "p → q" is "¬q → ¬p". The contrapositive is logically equivalent to the original statement, meaning they have the same truth value (真值).
For example, the contrapositive of "If it is raining, then the ground is wet" is "If the ground is not wet, then it is not raining." Both statements are true or false together.