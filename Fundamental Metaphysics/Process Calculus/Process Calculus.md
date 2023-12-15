---
creation date:		2023-05-24 16:05
modification date:	2023-05-24 16:05
title: 				Process Calculus Axioms
tags: #metaphysics
---

The process calculus is a tool for representing the evolution of a self-representing [representative abstraction](Def-TC-0.0-representative_abstraction).

In time, we refer to this as a process. The process abstraction is used to demonstrate a [temporal solution to representative paradox](Temporal Solution to Representative Paradox (Observer's Paradox), an observer's paradox.

Simple examples can be found in: [[Reductive Examples]]

[[Equality Operators]]
![[Def-TC-0.1.2-abstraction]]
![[Def-PC-0.1.3-compound_abstraction]]![[Prop-PC-0.1.4]]![[Def-PC-0.0-Process]]
*Demonstrate the expression of abstractions in a simple process using [[Representative Number Theory]]*
```
# We use (proc x) to denote a theorem of process calculus
# (:= a b) : a may be expressed as b

(:=
	(proc (' 
		F
	))
	(proc (' 
		F | F | (m F)
	))
)

# Isomporphic data-structure for describing state of a simple process
(
	F     # input
	F     # p-space
	(mf)  # output
)
```

![[Def-PC-0.4-Evaluation]]

![[Axiom-PC-0.1-Observation]]

![[Axiom-PC-0.2-Substitution]]

![[Axiom-PC-0.3-GD_Substitution]]

![[ISO-PC-0.3.1]]

![[Axiom-PC-0.4]]

![[Prop-PC-0.0]]

---
[^1]:: [[Tasks Related to the development of the Process Calculus]]
[^2]:: [[Notes Related to the development of the Process Calculus]] 
[^4]: [[Tasks related to computational metaphysics]]
[^3]: [[Notes related to computational metaphysics]]
[^4]:: [[Reductive Examples]]