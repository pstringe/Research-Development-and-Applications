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
Lisp for writing operatic programs

I started writing a DSL for the purpose of transcribing some formal propositions in my hand-written notes into my computer. I started with a traditional functional syntax, and while contemplating parsing and relating it to another project I was building to calculate using my [[Representative Number Theory]], I realized it would be more efficient to switch to prefix notation.
I have an abstraction I use, a $plurality$, which is really similar to a list and identical syntactically so the DSL pretty much turned into a lisp. At least syntactically.

COND
```
(cond 
	((condition_0) (implication_0))
	((condition_1) (implication_1))
	.
	.
	((condition_n) (implication_n))
)
```

AND
```
(&& 
	( cond
		((= a b) (t))
		((~ (= a b)) (t))
))(a b)
```

OR
```
(|| 
	( cond
		((~ (= b ()) (t))
		((~ (= a ()) (t))
)))(a b)
```

NOT
```
(~ a b)(a b)
```

---
[1^]:: [[Notes on representative lisp]]
[2^]:: [[Tasks related to representative lisp]]