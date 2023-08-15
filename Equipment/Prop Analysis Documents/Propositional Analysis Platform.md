---
creation date:		2023-05-18 11:58
modification date:	2023-05-18 11:58
title: 				Propositional Analysis
tags:
---

![[Prop Analysis Introduction]]
![[SPEC-PA-General_Requirements]]
![[SPEC-PA-Data_Collection_Requirements]]
![[PA-DSN_Analysis_Requirements]]
![[PA-Logical_Analysis_Requirements]]
![[PA-Temporal_Analysis_Requirements]]
![[PA-User_Stories]]
![[SPEC-PA-Data_Model|SPEC-PA-Data_Model]]

### Interfaces
![[SPEC-PA-API]]

![[SPEC-PA-UI_Features]]
![[V2 Prop Analysis Spec for C implementation]]
![[Propositional Analysis ERD]]

**API Module**
```C
/*
** mapping between string 
*/

typedef struct s_map {
	char *type;
	int length;
	int bytes;
} t_map;

typedef struct s_mapper {
	t_map types[NO_OF_TYPES];
	map
}

t_map type_mapping[NO_OF_TYPES] =  {
	{"int", 1, 4},
	{"char", 1, 1},
	{"string", 0, 1},
}

typedef struct s_request {
	void *data;
} t_request;

typedef struct s_response {
	void *data;
} t_response;

typedef struct s_resource  {
	char  *name;
	char ;
	t_response (*create)(struct s_resource*, t_request*);
	t_response (*read)(struct s_resource*, t_request*);
	t_response (*update)(struct s_resource*, t_request*);
	t_response (*delete)(struct s_resource*, t_request*);
}   t_resource;


```

---
[1^]:: [[Notes related to propositional analysis specificaton]]
[2^]:: [[Tasks related to propositional analysis specification]]
[3^]:: [[V2 Prop Analysis Spec for C implementation]]
