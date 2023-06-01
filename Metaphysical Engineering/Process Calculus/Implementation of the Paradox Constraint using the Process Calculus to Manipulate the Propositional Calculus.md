---
creation date:		2023-05-24 13:55
modification date:	2023-05-24 13:55
title: 				Implementation of the Paradox Constraint using the Process Calculus to Manipulate the Propositional Calculus
tags:
---
1. [Prop] `i ) m ) o`
2. [Prop] Apply evaluation for `i===x ^ m===x`
```
i ) m ) o [i:=x][m:~x][o:m]  -> x ) m  ) o [m:~x][o:m] -- substitution
							 -> x ) ~x ) o [o:m].      -- substitution
							 -> x ) ~x ) ~x  	       -- substitution
```
3. [Prop] Apply observation `x ) ~x ) ~x -> ~x ) x ) ~x ) ~x)`  [Axiom 7]
4. [Prop] Apply Evaluation `~x ) x ) ~x ) ~x )
```

```
