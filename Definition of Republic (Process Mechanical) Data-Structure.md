---
creation date:		2023-09-12 11:37
modification date:	2023-09-12 11:37
title: 				Definition of Republic Data-Structure
tags:
---

The data structure we define here may be utilized to simulate a process mechanical system to simulate government structures and intelligence mechanics. The first draft of the definition is not an exhaustive proof. The definition is reliant on isomorphisms between three formal systems [Representative Logic](Representative%20Logic.md), [Abstract Representative Calculus](Abstract%20Representative%20Calculus.md), [Process Calculus](Process%20Calculus.md), [Representative Calculus](Representative%20Calculus.md).

![Representative Logic](Representative%20Logic.md)
TYPE : INDEX : ORIGIN : REP : M-REP

**PT 1: Demonstration of the observer's paradox in representative and process calculus**
PROP : 0.0 : P : $f(x)$ : $f$ represents $x$
```
(f x)
```

PROP : 0.1 : P : $(f(x) \leftarrowtail O(f(x)))$ : $f$'s representation of x is dependent on the observer of $f$'s representation of x.
```
(dep
	(f x)
	(O (f(x)))
)
```

ISO : 0.0 : P : $((\leftarrowtail)\ ::=\ ('(is\ affected\ by)\ '(depends\ on)))$
```
(::=
	(' dep)
	(
		(' isaffectedby)
		(' dependson)
	)
)
```

PROP : 0.3 : P : $((f_{0}(f_{0}) \Rightarrow f_{1}) \supset (f_{0} \neq f_{1}))$ : :  [Axiom-TC-0.1-GD](Axiom-TC-0.1-GD.md) [Axiom-TC-0.2-EP](Axiom-TC-0.2-EP.md) RESOLUTION
```
(=>
	(evaluates
		(f_0
			(f_0)
		)
		f_1
	)
	(!=
		f_0
		f_1
	)
)
```

NOTE : 0.3.1 : P : This is reflective of a temporal solution to the EP, but does not demonstrate the expression of the prima equality relation, of which evaluation is the temporal expression.

PROP : 0.2 : P : $f := f(f)$ : : [Axiom-TC-0.1-GD](Axiom-TC-0.1-GD.md) [Axiom-TC-0.2-EP](Axiom-TC-0.2-EP.md) resolution.
```
(:=
	f
	(f f)
)
```

PROP : 0.4 : P : $(f_{0}(f_{0}) \Rightarrow f_{1}(f_{1}))$ : : [Axiom-TC-0.1-GD](Axiom-TC-0.1-GD.md) [Axiom-TC-0.2-EP](Axiom-TC-0.2-EP.md) 
```
(evaluates
	(f_0
		(f_0)
	)
	(f_1
		(f_1)
	)
)
```

PROP : 0.5 : P : $(O(f) = f)$ : $f$ is the observer of $f$
```
(=
	(O f)
	f
)
```

PROP : 0.6 : P : $(f \cong F)$ : $f$ is isomorphic to $F$ 
```
(<-=
	f
	F
)
```

PROP : 0.7 : P : $(f(f)) \supset (O(F) = F))$ : $f$'s representation of $f$ implies the observer of $F$ is $F$ : [0.3, 0.6]
```
(=>
	(f f)
	(
		(O F)
		F
	)
)
```

PROP : 0.8 : P : $(\ O(F)\  :=\  (F_{n}\ )\ O(F_{n}\ )\ F_{n+1}\ )\ )\ )$
```
(:= 
	(O F)
	(F_n ) (O F_n) ) F_{n+1})
)
```

PROP : 0.9 : P : $((f(x)\ \leftarrowtail\ f(f(x))))\ \supset ((x_{n}\ )\ F_{m})\ x_{n+1}\ )\ O(F)\ )\ (\ x_{n+1}\ )\ F_{m + 1}\  )\ x_{n+2}\ )\ )$ : $f$'s representation of $x$ depends on the observer of $f$'s representation of $f$'s representation of $x$ : $f$'s representation of $x$ is affected by the observer of $f$'s observation of $f$'s observation of $x$.
```
(=>
	(dep
		(f x)
		(f (f x))
	)
	(proc
		(x_n ) F_m ) x_{n+1})
			) (O F) )
		(x_{n+1} ) F_m+1 ) x_{n+2})
	)
)
```

PROP : 1.0 : $((f = (O\ f))\ \supset (F = (O\ F)))$ : [6, 7]
```
(=>
	(=
		f 
		(O f)
	)
	(=
		F
		(OF)
	)
)
```

PROP : 1.1 : $((O(F)\ =\ F)\ \supset (C(F)\ =\ C(O(F)))$
```
(=>
	(=
		(O F)
		F
	)
	(=
		(C F)
		(C 
			(O 
				F
			)
		)
	)
)
```

PROP : 1.2 : $((f(x_0)\ =>\ x_1)\ \land (x_0\ \neq x_1 ))$
```
(^
	(f
		x_0
		x_1
	)
	(!=
		x_0
		x_1
	)
)
```

PROP : 1.3 : $((1.2)\ \land (x_0 = f))$
```
(&&
	(1.2)
	(=
		x_0
		f
	)
)
```

PROP : 1.4 : $(f_n(f_n) \Rightarrow f_{n+1})$
```
(evaluates
	(f_n f_n)
	f_n+1
)
```

PROP : 1.5 : $(f_n(f_n) = f_n^0(f_n^{-1}(...f_n^{-inf}...)))$
```
(=
	(f_n
		f_n
	)
	(f_n^0
		(f_n^1
			(...f_n^-inf...)
		)
	)
)
```

PROP : 1.6 : $((f_n^{-inf}(f_n^{inf - 1}) = f_n^{-inf})$
```
(=
	(f_n^{-inf}
		(f_n^{inf-1})
	)
	(f_n^{-inf})
)
```

PROP : 1.7 : $(f_x^i \leftarrowtail F_x^i)$ 
```
(dep
	f_x_i
	F_x^i
)
```

**PT 2: Expression of Simple Process Mechanical System in the OP**
PROP : 2.0 : $((f = O(f)) \supset (F_n )\ O(F)\ ) F_{n+1}))$ : [1.0, 0.6]
```
(=>
	(=
		f
		(O f)
	)
	(F_n ) (O F) ) F_{n+1})
)
```

PROP : 2.1 : $( f(x) \leftarrowtail f(f(x)) ) \supset ( (x_n )F_m) x_{n+1})) O(F) ) (x_{n+1} ) F_{m+1} ) x_{n+2}) )$ : [0.1, 0.6]

PROP : 2.1.0 :
```
(dep
	(f x)
	(f 
		(f 
			x
		)
	)
)
```

PROP : 2.2.0 : 
```
(=>
	(
		(x_n ) F_m ) x_{n+1})
			) (O F) )
		(x_n+1 ) F_{m+1} ) x_n+2)
	)
)
```

PROP : 2.2 : `(:= F (G H))`

---
[1^] :: [Tasks related to processing republic data-structure](Tasks%20related%20to%20processing%20republic%20data-structure.md)







