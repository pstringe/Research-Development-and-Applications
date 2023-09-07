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

```
# stimulation
( --> (m p) (m (m p)) (m (m (m p))))) (
	(m p)         # src
	(m(m p))      # dst
	(m(m(m p)))   # observation - prop - imp
)

# response
( <-- (m p) (m (m p)) (m (m (m p)))) (
	m(p),         # src
	m(m(p)),      # dst
	m(m(m(p))).   # observation - prop - imp
)

# menial request
( req_m
	(--> (m p) (m (m p)) (m (m (m p))))
)(
	(m p)          # src
	(m (m p))      # dst
	(m (m (m p))). # observation - prop - imp
)

# menial response
( res_m
	(<-- (m p) (m (m p)) (m (m (m p))))
)(
	(m p)           # src
	(m (m p))       # dst
	(m (m (m p))).  # observation - prop - imp
)

# liminal request
( req_l
	(--> (m p) (m (m p)) (m [(m (m (m p)))] ))
)(
	(m p)           # src
	(m (m p))       # dst
	(m (m (m p))).  # observation - prop - imp
)

# liminal response
( res_l
	(<-- (m p) (m (m p)) (m [(m (m (m p)))] ))
)(
	(m p),          # src
	(m (m p))       # dst
	(m (m (m p)))   # observation - prop - imp
)

# liminal response
( res_l
	(<-- (m p) (m (m p)) (m [(m (m (m p)))] ))
)(
	(m p),          # src
	(m (m p))       # dst
	(m (m (m p)))   # observation - prop - imp 
)

#Examples

(res_l (m p) (m (m p)) (m (m (m p))))


```

