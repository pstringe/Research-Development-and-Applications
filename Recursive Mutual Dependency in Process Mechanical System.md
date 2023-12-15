---
creation date:		2023-09-06 16:15
modification date:	2023-09-06 16:15
title: 				Mutual Dependency (Entanglement) in Process Mechanical System
tags:
---
PROP : 0.0 : 
```
(:= V (p, (m p)))
```

PROP : 0.1 : 
```
(:= R (q, r, F))
```

PROP : 0.2 : 
```
(:= S (
	(q, r, F)
	(q, r, (m F))
	(q, (m r), F)
	(q, (m r), (m F))
	((m q), r, F)
	((m q), r, (m F))
	((m q), (m r), F)
	((m q), (m r), (m F))
))
```

PROP : 0.3 : 
```
(:= 
	F
	(
		(:= F (proc 
			F | F | (m F)
		))
	)
)
```

PROP : 0.1 : 
```
F | F | (m F)
```

PROP : 0.2 : 
```

```