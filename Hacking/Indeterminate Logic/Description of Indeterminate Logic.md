---
creation date:		2023-06-10 14:25
modification date:	2023-06-10 14:27
title: 				Proposition
type:     
topic:
index:
name:
tags: 
---

## Values
0. [Def] For any given proposition `P`, may be represented by a tuple `(c, f)` where `c` is a value representing `P`'s relationship to the current state, and `f` is a value representing `P`'s relationship to a future state.
1. [Def] `c` may be any of the following values: `T F U C`
2. [Def] `f` may be any of the following values: `A R U C`
3. [Def] `c==T` if `P` is an isomorphic representation of the current state
4. [Def] `c==F` if `~(c==T)`
5. [Def] `c==U` if `~(c==T) ^ ~(c==F)`
6. [Def] `c==C` if the value of c depends on an indeterminate value
8. [Def] `f==A` if `P` is an isomorphic representation of a future state. (evidation of `P`)
9. [Def] `f==R` if `~(f==A)`
10. [Def] `f==U` if `~(f==A) ^ ~(f==R)`
11. [Def] `f==C` if the future state of `P` depends on an indeterminate value
12. [Def] `f==S` if the subject evidates `P` is isomorphic a past state 
13. [Def] `f==E` if the subject evidates `P` is not isomorphic to a past state

## Operators
### Equality Operators
0. [Def] `C(x, y)`:  `[x, y] ) C ) {} ` : `x === y` ,x is isomorphic to y in form.
2. [Def]` E(x, y)`:  `x ) E ) y` : `x == y`, the evaluation of x is isomorphic to the evaluation of y in form and content
3. [Def] `S(x, y)`:  `x ) S ) y`: `x := y`, x is an abstraction of y. (y may replace x)
4. [Def] `O(x, y)`:  `x ) O ) ` : `x::=Y`, x may be any one of the values in the set y
5. [Prop] for a given `x` and `y` more than one of these operators may apply

### Abstract Operators
0. [Def] `mE(x, A)`:  `[x] ) mE ) y`: `x::=A`  Where `A:={a, b, c ... n}`, assign to x, one of the values of `A`, to produce `y` 
1. [Def] `eX(x)`: `x ) eX ) A`: Expression of `x` where `x` represents an abstraction and `A := {a, b, c ... n}` represents a resulting set of abstractions.`

### Relationships
0. *indeterminate*: `uR()`
1. *determinate*: `dR()`
2. *contingent*: `cR()`

### Logic Definition
Def : NLA : 0.0 : Indeterminate Logic Values
```
type Value = T | A | R | F | C | S | E
```

![[Def-NLA-1.0-Abstraction]]


### Logical Operators
0. `tG((T | F) | (A | R))`: toggle a measured state
1. `m?(A)`: measure an indeterminate state
2. `t(x) => g()`
3. `d(x)`