---
creation date:		2023-06-10 14:25
modification date:	2023-06-10 14:27
title: 				Proposition
type: Prop
topic: Op
index: 0.3
name: 
tags: metaphysics 
---
Prop : Op : 0.3 : [[Prop-Op-0.1]] and [[Prop-Op-0.2]] are not true simultaneously
```
(E F)(F (0.0.1 0.0.2))(
	(^
		(~
			(v
				(^
					((m .. F) (== 0.0.1 T))
					((m .. F) (== 0.0.2 T))
				)
				(^
					((m .. (m .. F)) (== 0.0.1 T))
					((m .. (m .. F)) (== 0.0.2 T))
				)
			)
		)
		(^
			((m .. F) (== 0.0.1 T))
			((m .. (m .. F)) (== 0.0.2 T))
		)	
	)
)
```