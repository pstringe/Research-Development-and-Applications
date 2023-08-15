---
creation date:		2023-06-03 21:28
modification date:	2023-06-03 21:30
title: 				Data Model
tags: #tools #engineering
---
**Propositions** contains the following properties:
* proposition: string representing the proposition in standard form
* tokenization: an integer array, of tokens representing the proposition
* created: a Timestamp representing the time the proposition was submitted
* updated: a Timestamp representing the time the proposition was submitted

**Comments** contains the following properties:
* text: string
* created: a Timestamp representing the time the comment was submitted
* updated: a Timestamp representing the time the comment was updated

**Source** contains the following properties:
* link: string
* text: string

### Value
```C
enum value{T, A, U, R, F, C}
```

### Token
```C
struct Token {
	id: int
	text: char*
	value: value	
	tokenization: int[]
}
```

### Expression
```C
struct Expression {
	id: int
	value: value
	tokens: Token[]
}
```

### Proposition
```C
struct Proposition {
	id: int
	expressions: Expression[]
	value: value
	created_at: time_t
	updated_at: time_t
}
```

### Source
```C
struct Source {
	id: int
	link: char*
}
```

### Citation
```C
struct Citation {
	id: int
	source: Source
	title: char*
	date: time_t
	pagNo: char*
	index: int
}
```

### Dialectic
```C
struct Dialectic {
	id: int
	name: char*
	created_at: time_t
	updated_at: time_t
}
```

### Comment
```C
struct Comment {
	id: int
	created_at: time_t
	updated_at: time_t
}
```


