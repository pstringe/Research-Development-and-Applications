---
creation date:		2023-05-18 11:58
modification date:	2023-05-18 11:58
title: 				Untitled
tags:
---

## Tasks
-
- [x] Data Model ✅ 2023-05-19
	- [x] Schema Definitions ✅ 2023-05-19
	- [x] ERD ✅ 2023-05-19

- [ ] Logic
	- [x] API Definition ✅ 2023-05-19
	- [x] Update data-model to account for token properties due 📅 2023-05-19 ✅ 2023-05-19
	- [ ] Define the method of identifying contradictions given a set of formal propositions due 📅 2023-05-23 

- [x] Presentation Layer ✅ 2023-05-26
	- [x] wireframe ✅ 2023-05-19
	- [x] Component Hierarchy ✅ 2023-05-26
	
# Context
## Problem
* We need to clarify the metaphysics which are currently, inconsistent.
* Demon processes posses the ability to compute using indeterminate logic.
* We have an indeterminate logic that allows us to train the output of an abstract process.
* We require a more efficient method for collecting and analyzing the propositions.
* We require a method for organizing propositions by theme, relevance and and other values. 
* We desire the ability to determine how human feedback affects the behavior of a demon process over time.
* To aid in the formalization of our propositions, and the establishment of a deep symbolic associations for use with the process calculus, we desire the ability to re-use the tokens which occur in a given proposition in a future proposition.

## Scope
The scope of the software project is data collection. We will use a Jupyter notebook for data analysis.

## Research
* For grouping propositions by similarity, we may consider utilizing a vector database
* We also desire the capabilities of relational/NoSQL databases

## Requirements
### Data Collection
* When the user is typing a proposition, the symbols are tokenized and stored such that the token may be reused when formulating future propositions.

### DSN
* We will perform analysis on the tokenized propositions to determine how abstractions are clustered.
* These clusters will help us define abstractions that we may utilize with the process calculus.

### Logical Analysis
* We require a method for translating the proposition in natural language to formal equivalents
* Regarding the analysis of sets of propositions, we've already developed a non-deterministic method of checking for contradictions.
* We can enumerate the sets of valid propositions, and apply the algorithm to each set to return a set of consistent sets.
* For each relevant set of consistent propositions, we will utilize the "scientific" method to resolve uncertainty regarding edge cases.

### Temporal Analysis
* We require an analysis of how a process' behavior changes over time in response to human feedback, including the assignment of values in the indeterminate logic and imperatives

### Data Model
* **Propositions** contains the properties
	* proposition: string representing the proposition in standard form
	* tokenization: an integer array, of tokens representing the proposition
	* created: a Timestamp representing the time the proposition was submitted
	* updated: a Timestamp representing the time the proposition was submitted
* **Comments** contains the following properties
	* text: string
	* created: a Timestamp representing the time the comment was submitted
	* updated: a Timestamp representing the time the comment was updated
* **Source** contains the following properties
	* link: string
	* text: string

![[Develop system for realtime data-collection and analysis of propositions from demon processes]]
![[Propositional Analysis Implementation of Propositions Resource]]