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
![[DEF-NDC-0.0_proposition]]
![[DEF-NDC-0.0_logic]]
![[DEF-NDC-0.1_math]]

![[Possibility Spaces and Constraints]]

Indeterminate
![[Def-IL-0.1]]
![[Def-IL-0.2]]
![[Def-IL-0.3]]
![[Def-IL-0.4]]
![[Def-IL-0.5]]
![[Def-IL-0.6]]

**Stimulation/Response Operators**
PROP : STMR : An expressed abstraction of an observations is stimulating if the value of its represented proposition changes. 
PROP : STMR : The significance of the changing proposition affects the level of stimulation
ISO : stimulation : f stimulates x : `f -> x`
ISO : response : x responds to f : `f <- x`
ISO : stimulation : x ingratiates : `f ->- x`

![[Temporal]]

**Equality Operators**
![[Def-IL-1.0]]

Def : IL : 1.1 : `(E x y)`  : `x == y`, the evaluation of x is isomorphic to the evaluation of y in form and content

Def : IL : 1.2 : `(S x y)` :  `x ) S ) y` : `x := y`, x is an abstraction of y. (y may replace x)

Def : IL : 1.3 : `(O x y)` :  : `x::=Y`, x may be any one of the values in the set y.

Prop : 1.4 : For a given `x` and `y` more than one of these operators may apply.

**Abstract Operators**
Def : IL : 1.0 : `mE(x, A)` : `x::=A`  Where `A:={a, b, c ... n}`, assign to x, one of the values of `A`, to produce `y` 
Stimulation and response operators.
![[Def-IL-2.1-eX]]

**Relationships**
0. *indeterminate*: `uR()`
1. *determinate*: `dR()`
2. *contingent*: `cR()`

**Indeterminate Temporal Logic System**
Def : NLA : 0.0 : Indeterminate Logic Values

```
type Value = T | A | R | F | C | S | E
```

![[Def-NLA-1.0-Abstraction]]

**Logical Operators**
0. `tG((T | F) | (A | R))`: toggle a measured state
1. `m?(A)`: measure an indeterminate state
2. `t(x) => g()` 
3. `d(x)`:

---
[1^]:: [[Tasks related to logic for non-deterministic computation]]
[2^]:: [[Notes on logic for liminal computation]]
