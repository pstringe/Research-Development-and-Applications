---
creation date:		2023-06-03 20:59
modification date:	2023-06-03 20:59
title: 				Natural Language Application of Indeterminate Logic
tags:
---

![[Description of Indeterminate Logic]]

## Interface Requirements
0. Each proposition is composed of `expressions`
1. Each expression is composed of `tokens`
3. Proposition may be grouped to form a compound propositions
4. By default, each token in an `expression` has a value of `T`, indicating it is isomorphic in form and content to the state described
5. If the user doesn't know whether the token is isomorphic to the current state, they may change the value to `U`
6. The user may choose to `express` any token
7. To `express` a token is to associate it with an `expression`  such that the expressed token becomes an `abstraction` of the expression. (The expression can be substituted for the token and the proposition would still make sense to the user)

## Rules for evaluation
0. Given the expression `D`
1. If for every token  `t` in `D`, `t.value == T`  then  `D.value == T` 
2. If for every token `t` in `D` , `t.value == T || t.value == A`  then `D.value == A`
3. If there exists a token `t` in `D` such that `t.value == R` then `D.value == R`  
4. If there exists a token `t` in `D` such that `t.value == F` then `D.value == F`

