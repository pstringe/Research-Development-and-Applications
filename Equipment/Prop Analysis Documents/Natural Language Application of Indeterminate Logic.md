---
creation date:		2023-06-03 20:59
modification date:	2023-06-03 20:59
title: 				Natural Language Application of Indeterminate Logic
tags:
---

![[Logic for Nondeterministic Computation]]


## Definitions
0. [Prop] Each proposition is composed of `expressions`
1. [Prop] Each `expression` is composed of `abstractions`
3. [Prop] A `proposition` may be grouped to form compound `propositions` (We will temporarily ignore propositions until we understand abstraction and expression)
4. [Prop] By default, each `abstraction` in an `expression` has a value of `T`, indicating it is isomorphic in form and content to the `state`
5. [Def] If the subject hasn't resolved whether or not the `abstraction` is isomorphic to the current state, they may change the value to `U`
6. [Axiom] The subject may  `express` any `abstraction`
7. [Def] An `expression` maps one `abstraction` to many abstractions
8. [Def] A `symbol` maps one `abstraction` to another abstraction. 
9. [Def] To `express` an `abstraction` is to associate it with an `expression`  such that the expressed `abstraction` becomes an `abstraction` of the expression. (The expression can be substituted for the abstraction and the parent would maintain it's isomorphisms)

## Rules for evaluation
0. Given the expression `D`
1. If for every `abstraction`  `t` in `D`, `t.value == T`  then  `D.value == T` 
2. If for every `abstraction` `t` in `D` , `t.value == T || t.value == A`  then `D.value == A`
3. If there exists a token `t` in `D` such that `t.value == R` then `D.value == R`  
4. If there exists a token `t` in `D` such that `t.value == F` then `D.value == F`
