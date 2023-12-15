---
creation date: 2023-09-01 03:50
modification date: 2023-09-01 03:50
title: SPATIAL_MANIPULATION_0
tags:
  - magic
  - mathematics
---
![Scanned Documents](Scanned%20Documents.pdf)

PROP : 0.0 : `(arc A B)`
PROP : 0.1 :
```
(=
	(density 
		(arc
			A
			B
		)
	)
	p
)
```

PROP : 0.2 :
```
(=
	(density
		(arc
			A
			(m B)
		)
		(/
			(m (m (m p)))
			(m (m p))
		)
	)
)
```

PROP : 0.3 : U : 
```
(P 
	(=>
		0_1
		(= 
			0_2
			A
		)
	)
)
```
