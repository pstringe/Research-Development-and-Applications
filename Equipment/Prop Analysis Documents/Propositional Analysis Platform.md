---
creation date:		2023-05-18 11:58
modification date:	2023-05-18 11:58
title: 				Propositional Analysis
tags:
---
[V2 Prop Analysis Spec for C implementation](V2%20Prop%20Analysis%20Spec%20for%20C%20implementation.md)
[V3 Prop Analysis](V3%20Prop%20Analysis.md)

---
![Prop Analysis Introduction](Prop%20Analysis%20Introduction.md)
![SPEC-PA-General_Requirements](SPEC-PA-General_Requirements.md)
![SPEC-PA-Data_Collection_Requirements](SPEC-PA-Data_Collection_Requirements.md)
![PA-DSN_Analysis_Requirements](PA-DSN_Analysis_Requirements.md)
![PA-Logical_Analysis_Requirements](PA-Logical_Analysis_Requirements.md)
![PA-Temporal_Analysis_Requirements](PA-Temporal_Analysis_Requirements.md)
![PA-User_Stories](PA-User_Stories.md)
![SPEC-PA-Data_Model](SPEC-PA-Data_Model.md)

### Interfaces
![SPEC-PA-API](SPEC-PA-API.md)

![SPEC-PA-UI_Features](SPEC-PA-UI_Features.md)
![V2 Prop Analysis Spec for C implementation](V2%20Prop%20Analysis%20Spec%20for%20C%20implementation.md)
![Propositional Analysis ERD](Propositional%20Analysis%20ERD.md)

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
[1^]:: [Notes related to propositional analysis specificaton](Notes%20related%20to%20propositional%20analysis%20specificaton.md)
[2^]:: [Tasks related to Propositional Analysis Specification](Tasks%20related%20to%20propositional%20analysis%20specification.md)
[3^]:: [V2 Prop Analysis Spec for C implementation](V2%20Prop%20Analysis%20Spec%20for%20C%20implementation.md)
