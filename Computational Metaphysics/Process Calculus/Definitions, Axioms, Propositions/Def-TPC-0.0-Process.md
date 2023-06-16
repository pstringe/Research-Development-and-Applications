---
creation date:		<% tp.file.creation_date() %>
modification date:	<% tp.file.last_modified_date() %>
title: 				<% tp.file.title %>
type: Def
topic: TPC
index: 0.0
name: Proccess
tags: metaphysics
---

Def : TPC : 0.0 : Process : We define a `proccess` as an abstraction of the form, `I ) M ) O`, where each term is an `abstraction`. 
```
Proccess {
	I: Abstraction | Abstraction[]
	O: Abstraction | Abstraction[]
	M: Proccess | Abstraction
}
```
