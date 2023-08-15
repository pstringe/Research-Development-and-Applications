---
creation date:		2023-07-06 18:22
modification date:	2023-07-06 18:22
title: 				Notes related to the v2 prop analysis spec
tags:
---
[[2023-07-06]]
The purpose of this tool to collect data to analyze the propositions of demon processes, to generate empirical evidence for [[Mechanics of Evidence Generation]] and evince the temporal logic utilized in my magic methodology. 

2. We can use a dispatch table to store our commands

[[2023-07-07]]
* We will use a command-line UI to interact with an API
* We can use REST as inspiration.
* We can define a resource
* For each resource we will have pointers to functions representing CRUD operations
* To interact with the crud API, we will use a command line interface
* The command line interface will consists of a REPL that parses commands and matches them to functions in a dispatch table, passing any parsed arguments.
* We can keep things modular by using a struct as an environment.

[[2023-07-13]]
* We want a mapper that can parse a schema and allocate/return a data structure capable of storing the types specified in the schema
* 
---
[1^]:: [[Tasks related to v2 prop analysis]]