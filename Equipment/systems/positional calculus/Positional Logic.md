---
creation date:		2023-05-21 08:15
modification date:	2023-05-21 08:15
title: 				Untitled
tags:
---
ssss
A formal system I developed to address some simple problems that involved manipulating the relative positions of elements. I think we can use it to come up with a theory of how numbers are resolved.

theorems of the positional logic may be manipulated using the propositional calculus.
## Symbols and interpretation
Def : POSC : 0.0 : (
Def : POSC : 0.1 : )

![Def-POSC-0.2-dimension](Def-POSC-0.2-dimension.md)

![Def-POSC-0.3-position](Def-POSC-0.3-position.md) 

![DEF-POSC-0.4-space](DEF-POSC-0.4-space.md)

Prop : POSC : 0.5 : $position$ in $space$ : 0.5 : A $position$ $A$, in $space$ $x$ may be represented as $A_x$. Where $space$ $X$ consists of $n$ dimensions, $A_x$ can also be represented by a $plurality$, $positions$, from each $dimension$ such that, $ex(A_x) \Rightarrow (C_a, D_b ... O_n)$.
Prop : POSC : 0.6 : $poistion$ in $dimension$ : A position $A$ of dimension $X$ is represented as $A_X$
Def : POSC : 0.7 : $|$ : adjacency : 
Def : POSC : 0.8 : $||$ : relative position :
Def : POSC : 0.9 : = : substitutable
Def : POSC : 1.0 :  $V()$ : is valid
Def : POSC : 1.1 : $\Leftrightarrow$ : $A_a$ $\Leftrightarrow$ $A_b$ is interpreted as $position$ $A$ in $space$ $a$ maps to $position$ $B$ in $space$ $b$
## Axioms
Axiom : POSC : 0.1 : `x`
Axiom : POSC : 0.2 : `| x`
Axiom : POSC : 0.3 : `x |`
Axiom : POSC : 0.4 : $V(| X)  \land V(Y) \rightarrow ~V(X | Y)$  : terminating elements are not extended
Axiom : POSC : 0.5 : $V(X |) \land V(Y) \rightarrow ~V(Y | X)$ : terminating elements are not extended
Axiom : POSC : 0.6 : $V(X) \rightarrow V((X))$ : 'parenthesation'
Axiom : POSC : 0.7 : $V(Y) \land V(Y) \rightarrow V(X | Y)$ : 'adjacency'
Axiom : POSC : 0.8 : $V(Y) | V(Y) \rightarrow V(X |-| Y)$ : 'relative positioning'
Axiom : POSC : 0.9 : $V(X | Y) \rightarrow V(Y) \land V(X)$ : 'extraction'
Axiom : POSC : 1.0 : $\{\{A, B, C ... Z\}\}$ = $\{A, B, C ... Z\}$  
Axiom : POSC : 1.1 : $prefix(A\ B)$ : $(f(A\ B)\ \land \lnot f(A\ B))\ \Rightarrow (A || B)$
Axiom : POSC : 1.2 : $postfix(A\ B)$ : $(\lnot f(A\ B)\ \land f(A\ B))\ \Rightarrow (B || A)$
Axiom : POSC : 1.3 : $infix(D\ C)$ : $((D:=(A||B)) \land\lnot (f((A||B)\ C) \lor f(C\ (A||B)))) \Rightarrow ((A||C) \land (C||B))$

## Arithmetic Isomorphic Interpretation
1. $(X | Y) \rightarrow (X = Y - 1) \land (Y = X + 1)$
2. $(Y |-| X)  \rightarrow (Y < X - 1) \land (X < Y - 1)$

---
[1^]:: [Notes on the Positional Calculus](Notes%20on%20the%20Positional%20Calculus.md)
[2^]:: [Tasks related to the development of the positional calculus](Tasks%20related%20to%20the%20development%20of%20the%20positional%20calculus.md)
