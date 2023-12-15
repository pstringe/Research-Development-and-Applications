---
creation date:		2023-08-17 17:16
modification date:	2023-08-17 17:16
title: 				Hallucinatory(Indeterminate) Successions
tags:
---
*Dependencies*
[Possibility Spaces and Constraints](Possibility%20Spaces%20and%20Constraints.md)

![RTN-0.1](RTN-0.1.md)
![PROP-RTN_1.1](PROP-RTN_1.1.md)

PROP : RTN : 1.2 : We may construct the the following possibility space, using a plurality representing the possible values for $q$.
$$
	S = (p,\ m(p))
$$

PROP : RTN : 1.4 : Given, $(S = (p,m(p)))$  

PROP : RTN : 1.3 : Using this $possibility \ space$, we may construct a hallucinatory number:
$$
	((q) ::= ((q,\ m(q)))
$$
![PROP-RTN-1.4](PROP-RTN-1.4.md)

PROP : RTN : 1.5 : [PROP-RTN-1.4](PROP-RTN-1.4.md) is constructed using via [Axiom-RTN-0.6](Axiom-RTN-0.6.md) and [Axiom-RTN-0.5](Axiom-RTN-0.5.md)
![PROP-RTN-1.3](PROP-RTN-1.3.md)

ISO : RTN : 1.5 : Hallucinatory numbers may be utilized as exact representations of the space of possible $successions$ given a meta-representation, encoded as a plurality of propositions. These successions are isomorphic to $successions$ in the [Process Calculus](Process%20Calculus.md).

PROP : RTN : 1.4 : $$
	((q,r) ::= (q, m(r)))
$$
PROP : RTN : 1.5 : $$
	(m((q, r))) = (m(q), m(r))
$$
PROP : RTN : 1.6 : $$
	(m((q,r))) = (m(q), m(r)))
$$
PROP : RTN : 1.7 : 
```
(m((q,r)):::= (
	(
		(q, m(q)),  
		(m(q), q),  
		(m(q), m(q))
	),  
	(
		(q, q), 
		(m(q), q), 
		(m(q), m(q))
	), 
	(
		(q, q), 
		(m(q), q), 
		(m(q), m(q))
	)
	(
		()
	)
))
```

PROP : RTN : 1.8 : 
```
(
	m(
		m(
			(q, r)
		)
	)
) ::::= (
	(
		(m(p), p), 
		(m(p), m(p))
	), 
	(
		(p, m(p)), 
		(m(p), m(p))
	), 
	(
		(m(p), p),  
		(p, p),
		(m(p), p)
	)
)
```

PROP : RTN : 1.9 : Given a representation such as 1.8 we may abstract away the top-level pluralities, and resolve uncertainty as required. For example:
```
(m
	(m
		(m
			(q, r)
		)
	)
) ::::= (
	(
		(m(p), p), 
		(m(p), m(p))		
	),
	(
		(p, m(p)), 
		(m(p), m(p))
	),
	(
		(m(p), p),  
		(p, p),
	)
)
```

PROP : RTN : P represents a meta representation and interprets it as isomporphic to two overlapping spaces. First time experiences isomorphic visual representation in menial space with delay (no post evidence). The second time. Experienced visual reticulation and tactile reticulation (vibration) in the table in real time. Though the representation was not isomorphic. There was resistance.

[Reductive demonstration of indeterminacy of abstract propositions](Reductive%20demonstration%20of%20indeterminacy%20of%20abstract%20propositions.md)
