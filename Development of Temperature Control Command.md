---
creation date:		2023-08-31 03:57
modification date:	2023-08-31 04:04
title: 				Development of temperature control
tags:
---
PROP : P : 0.9 : A 
```
(P
	(:= 0.9.1
		(X
			(<
				cur_temp
				ideal	
			)
		)
	)
)
```

PROP : P : 1.0 : (F, A)
```
(P
	(X
		(=
			cur_temp
			ideal
		)
	)
)
```

OBSG : P : 1.1 : Back and triceps warm. Hands and lower extremities cold, temp dropping

PROP : P : 1.1 : 
```
(P
	(=>
		(X
			(=
				cur_temp
				ideal
			)
		)
		(P
			(=
				cur_temp
				ideal
			)
		)
	)
)
```

PROP : P : 1.2 : A
```
(P
	(X
		(=
			cur_temp
			ideal
		)
	)
)
```

OBSG : P : 1.3 : Immediate rise in temperature around the same regions as before accompanied by audible feedback

NOTE : P : 1.4 : We desire a syntax to efficiently represent properties of an abstraction.

*Syntax for declaring expressed abstractions as properties of the parent abstraction*
```
(x := ( (m x) (m (m x)) (m (m (m x))) )) <-= (x := (x.m x.mm x.mmm))

(x := (a b c)) <-= (x := (a(x) b(x) c(x))) <-= (x := ((a x) (b x) (c x))) <-= (x := (x.a x.b x.c))
```

PROP : P : 1.5 : T
```
(P
	(=> 
		(X
			(=
				P.hands.cur_temp
				ideal
			)
		)
		(P
			(=
				P.hands.cur_temp
				ideal
			)
		)
	)
)
```

PROP : P : 1.6 : A
```
(P
	(X
		(=
			P.hands.cur_temp
			ideal
		)
	)
)
```

OBSG : P : 1.7 : A  Slight rise in temperature, but also need to account for hand movement. temperature was not ideal.

PROP : P : 1.8 : 
```
(P
	(X
		(P
			(||
				(=>
					(P (' practices process mechanics))
					(= 
						P1_6
						T
					)
				)
				(=> 
					(P (' over-operates X))
					(=
						P1_6
						T
					)
				)
			)
		)
	)
)
```

PROP : P : 1.9 : A : over-operation of X to fulfill P1_6
```
(P 
	((m X)
		(X
			(=
				P1_6
				T
			)
		)
	)
)
```

OBSG : P : 2.0 : Temperature stays the same, then drops and oscillates. 
```
(P
	(=
		(C_i temp)
		B
	)
)
```

PROP : P : 2.1 :
```
(P
	((m .. B_0)(
		(~ 
			(==> 
				B_0 
				P
			)
		)
	))	
)
```

PROP : P : 2.2 
```
(P 
	(=> 
		2_1 
		(P
			(=
				P.temp
				ideal
			)
		)
	)
)
```

PROP : 2.3 :  P : T : `(= 2_1 T)`
OBSG : 2.4 : Slight rise in temperature, short and insignificant. In-ideal.

---
PROP : P : 2.3 : T
```
(P
	(::=
		P.temp
		(
			(p .. P.temp)
			P.temp
			(m .. P.temp)
		)
	)
)
```

OBSD : 2.4 : analog counting operation is marginally effective. Temp drops after switching focus
PROP : P : T : 2.4 : `(= P.temp (m P.temp))`
OBSG: 2.5 : Immediate rise in temp in back and neck. 
PROP : P : T : 2.5 : `(= P.temp (m (m P.temp)))`
OBSG : 2.5 : Immediate rise in temp around back, more significant than before, temperature drop not as immediate or sharp. We require a method to sustain the temperature change.
PROP : P : T : 2.6 : `(= P.temp (m (m (m P.temp))))`

---
[1^]:: [Core commands](Core%20commands.md)
