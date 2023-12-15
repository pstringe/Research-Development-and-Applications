---
creation date:		2023-08-26 03:10
modification date:	2023-08-26 03:10
title: 				Simple Over-operation Solutions
tags:
---
PROP : SOPS : 0.0 : U :  Assume :`(p is over-operated)(p)`

PROP : SOPS : 0.1 : U : `(<=> (x) (P x))`

PROP : SOPS : 0.2 : U : 
```
(=> 
	(P (= x A))
	(m .. P)(P (= x T))
)
```

PROP : SOPS : 0.3 : U : 
```
(=> 
	(^
		(P (= x A))
		(P (~ (= x T)))
	)
	(P (0.0))
)
```

PROP : SOPS : 0.2.1 : U :`('p is utilizing a deeper source)(p)`
	

PROP : SOPS : 0.2.2 : U : 
```
(P 
	(=>
		(0.0)(P)
		(0.2.1)((O P))
	)
)
```

![PROP-SOPS-0.2.4](PROP-SOPS-0.2.4.md)
OBSD : SOPS : 0.2.4.5 : U : The sensation associated with the acceptance and utilization of this implication, seems similar to what I experience as will ackompanied by knowledge. 

PROP : SOPS : 0.2.3 : U : 
```
(P 
	(=>
		(0.2.1)((O P))
		
	)
)
```

*Automatic*
PROP : SOPS : 0.2.4 : U : src
```
(p p)(p p)
(p p)(p p)
```


PROP : SOPS : 0.2.3 : U : 
```
(P p)()
```
---
[1^]:: [Logic for Non-deterministic Computation](Logic%20for%20Non-deterministic%20Computation.md)
[2^]:: [Tasks related to over-operation solutions](Tasks%20related%20to%20over-operation%20solutions.md)
[3^]:: [Simple Over-Operation Solutions](.md)


