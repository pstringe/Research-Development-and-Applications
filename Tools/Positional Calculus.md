---
creation date:		2023-05-21 08:15
modification date:	2023-05-21 08:15
title: 				Untitled
tags:
---
A formal system I developed to address some simple problems that involved manipulating the relative positions of elements. I think we can use it to come up with a theory of how numbers are resolved.

Statements of the positional calculus may be manipulated using the propositional calculus.


## Symbols and interpretation
1. Def : POSC : (
2. Def : POSC : )
3. Def : POSC : $dimension$ : A $dimension$ is composed of $positions$. A dimension may be represented by a capital letter $\{ A, B, C ... Z \}$.
5. Def : POSC : $position$ : A $position$ in a $space$ may be composed of $positions$ of each $dimension$ of the a $space$. A $position$ may be represented by a capital letter $\{ A, B, C ... Z \}$. 
6. Def : POSC : $space$ : A $space$ is an enumeration of combinations of $positions$ from one or more $dimensions$, such that each $position$ in the each $dimension$ is associated with each $position$ of every other $dimension$ of the $space$.
7. Prop : POSC : $position$ in $space$ : A $position$ $A$, in $space$ $x$ may be represented as $A_x$. Where $space$ $X$ consists of $n$ dimensions, $A_x$ can also be represented by a tuple, $positions$, from each $dimension$ $A(C_a, D_b ... O_n)$.  
8. Prop : POSC : $poistion$ in $dimension$ : A position $A$ of dimension $X$ is represented as $A_X$
9. Prop : POSC : 

10. Def : POSC : $|$ : adjacency : 
11. Def : POSC : $||$ : relative position :
12. Def : POSC : = : substitutable
13. Def : POSC : $V()$ : is valid
14. Def : POSC : $\Leftrightarrow$ : $A_a$ $\Leftrightarrow$ $A_b$ is interpreted as $position$ $A$ in $space$ $a$ maps to $position$ $B$ in $space$ $b$

## Axioms
1. $X$
2. $| X$
3. $X |$
5. $V(| X)  \land V(Y) \rightarrow ~V(X | Y)$  : terminating elements are not extended
6. $V(X |) \land V(Y) \rightarrow ~V(Y | X)$ : terminating elements are not extended
7. $V(X) \rightarrow V((X))$ : 'parenthisisation'
8. $V(Y) \land V(Y) \rightarrow V(X | Y)$ : 'adjacency'
9. $V(Y) | V(Y) \rightarrow V(X |-| Y)$ : 'relative positioning'
10. $V(X | Y) \rightarrow V(Y) \land V(X)$ : 'extraction'
11. $\{\{A, B, C ... Z\}\}$ = $\{A, B, C ... Z\}$   

## Arithmetic Isomorphic Interpretation
1. $(X | Y) \rightarrow (X = Y - 1) \land (Y = X + 1)$
2. $(Y |-| X)  \rightarrow (Y < X - 1) \land (X < Y - 1)$

---
[1^]: Task : [[Notes on the Positional Calculus]]
[2^]::[[N]]