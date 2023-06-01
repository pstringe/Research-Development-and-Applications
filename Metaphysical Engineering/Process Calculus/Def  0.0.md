---
creation date:		<% tp.file.creation_date() %>
modification date:	<% tp.file.last_modified_date() %>
title: 				<% tp.file.title %>
tags: #metaphysics
---
Def :: 0.0: *Process*: We define a `proccess` as an abstraction of the form, `I ) M ) O`, where each term is an `abstraction`. 
```
Proccess {
	I: Interface
	O: Interface
	M: Proccess | Proccess[]
}
```