---
creation date:		2023-07-28 11:27
modification date:	2023-07-28 11:27
title: 				Notes on process composition and self-reference to demonstrate stimulus-response
tags:
---
DEF : PCSR : 0.0.1 : $Stimulus$ : Given two representative abstractions, $f$ and $g$ where $((O\ f)=g)$, a change in $f$ is the stimulation of $g$.

DEF : PCSR : 0.0.2 : $Response$ : Given two representative abstractions, $f$ and $g$ where $((O\ f)=g)$ and $(f ((m\ g) \neq g))$,$((f\ ((m\ g) \neq g))\ is\ the\ response\ of\ g)$ $\iff$ $(f\ ((m\ g)\ =\ g)\ =\ (C_f\ ((m\ f)\ \neq f)))$.

DEF : PCSR : 0.0.3 : $Reticulation$ : Given two representative abstractions, $f$ and $g$ where $((O\ f)=g)$, $(f\ ((m\ f)\ \neq\ f))$, $(f\ ((m\ f)\ \neq\ f)) \Rightarrow (f\ ((m\ g)\ \neq\ g)) = A)$, $(f\ ((m\ g) \neq g))$ is the reticulation of $g$.

DEF : PCSR : 0.0.4 : $Ingratiation$ : Given two representative abstractions, $f$ and $g$ where
$((O\ f) = g)$ and $(f\ ((m\ g) \neq g))$ as the reticulation of $g$, $(f\ ( (m\ g) \neq g))$ where, $(f\ ((m\ f)\ \neq\ f)) \Rightarrow (f\ ((m\ g)\ \neq\ g)) = A)$, is the ingratiation of f's reticulation, $(f\ ((m\ g) \neq g))$, of g. 

PROP : PCSR : 0.0.5 : $Observer\ dependency$ : $((f x) \leftarrow ((O f)\ (f x)))$
INTERP: PCSR-0.0 : f's representation of x is dependent on the observer of f's representation of f representing x.

*Self Evaluation In Process Calculus*
PROP : PCSR : 0.1 : $((f_0 f_0) \Rightarrow f_1)$
PROP : PCSR : 0.1 : $(f := (f\ f)) \cong (F:= (F\ )(O\ F))\ F))$  
PROP : PCSR : 0.2 : $((f_0\ f_0) \Rightarrow f_1) \cong (F_0\ ) F_0\ ) F_1))$

NOTE :  As the complexity of our systems increases, instead of attempting to emulate our formal syntax for the process calculus, we introduce a technical syntax.

PROP : PCSR : 0.3 : 
```
(
	(F_0 ) F_0 ) F_1)
		) F_1 )
	(F_2 ) F_2 ) F_3)
)
```

NOTE : In the following following propositions, we introduce a technical syntax for the representative calculus. It is lisp-like to minimize excessive parsing upon implementation. We should be able to read an expression in the representative calculus and generate an environment to simulate an isomorphic process-mechanical system.

PROP : PCSR : 0.4 :
```
(->
	(^
		(
			(<-| 
				(f f) ((O f) f)
			)
		)
		(f = O(f))	
	)
	(
		(F_n ) O(F) ) F_{n+1}) 
	)
)
```

INTERP : PCSR : 0.5 : $f's$  representation of $f$ is dependent on the observer of $f's$ representation of $f's$.

PROP : PCSR : 0.6 : Generalization of PCSR-0.3 : 
```
(
	(F_n ) F_n ) F_{n+1})
		) F_{n+1} )
	(F_{n+2} ) F_{n+2} ) F_{n+3})
) 
```
NOTE : PCSR : 0.5 : Subscript indicates, step.
PROP : PCSR : 0.6 : 


*Composition of Mutually Dependent Processes*
PROP : PCSR : 0.4 : Where `(F = O(F))`
```
(
	(F_n ) F_n ) F_{n+1})
		) O(F_n) )
	(F_{n+1} ) F_{n+1} ) F_{n+2})
) == (
	(F_n ) F_n ) F_{n+1})
		) F )
	(F_{n+1} ) F_{n+1} ) F_{n+2})
)
```

PROP :  

---
[1^]:: [[Tasks related to processing notes on process composition, self-ref and stimulus-response]]