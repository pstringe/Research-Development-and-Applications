---
creation date:		2023-07-08 15:01
modification date:	2023-07-08 15:01
title: 				simulation of indeterminacy in using the thought calculus
tags:
---

DEF : NDC : 0.0 : $possibility\ space$ : Given a set of [propositions](obsidian://open?vault=Master&file=DEF-NDC-0.0_proposition), the $possibility\ space$ is the enumeration of the combinations of possible values of the [propositions](obsidian://open?vault=Master&file=DEF-NDC-0.0_proposition). We may consider each combination, itself to be a [proposition](obsidian://open?vault=Master&file=DEF-NDC-0.0_proposition).

DEF : NDC : 0.1 : $constrain$ : $C()$: A $possibility\ space$ is constrained upon the observation of an abstraction, the meta-representation of which is a [proposition](obsidian://open?vault=Master&file=DEF-NDC-0.0_proposition) of the $possibility\ space$.

![[PROP-NDC-0.2]] 

PROP : NDC : 0.3 : $C(S)$ : $space$ $S$ is $constrained$ .

![[PROP-NDC-0.3]]

PROP : SNDC : 0.4 : Any [proposition](obsidian://open?vault=Master&file=DEF-NDC-0.0_proposition), $p$, may evaluate to any value of the $plurality$ $V$

PROP : NDC : 0.5 : Given a plurality of propositions, $( p,\  q)$, where $V = (T,\ F)$:
	0.1.1 $p$ can evaluate to any of the values of the plurality $V$
	0.2.1 $q$ can evaluate to any of the values in the set $(T,\ F)$

PROP : SNDC : 0.2 : The space of possibilities, $S$, given P can be represented as the multi-dimensional plurality :
```
(
	(T, T),
	(T, F),
	(F, T),
	(F, F)
)
``` 

FIG :

| p   | q   |
| --- | --- |
| T   | T   |
| T   | F   |
| F   | T   |
| F   | F   |

PROP : SNDC : 0.5 : Here, S is not $constrained$.

PROP : SNDC : 0.4 : $(S \land \lnot C(S)) \implies (p = U) \land (q = U)$.

![[Prop-SNDC-0.5]]

PROP : SNDC : 0.6 : $C(S,  (p=T))$, the constraint of S, where $p=T$ can be represented as: 

```
C((
	(T, T),
	(T, F),
	(F, T),
	(F, F)
))
```

which evaluates to:
```
(
	(T, T),
	(T, F),
)
```


---
[1^]:: [[Tasks related possibility spaces]]
[2^]:: [[Notes related to possibility spaces]]