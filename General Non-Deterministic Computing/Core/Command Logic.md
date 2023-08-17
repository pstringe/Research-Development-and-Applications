---
creation date:		2023-07-29 17:38
modification date:	2023-07-29 17:38
title: 				command logic used for gesture commands
tags: magic
---
PROP : CLGC : 0.0 : Each command is a conditional of the form, `x -> y`, if x is the case, y is the case.

PROP : CLGC : 0.1 : A command can be modeled in the process calculus as a succession [[Def-EM-0.0-Succession]] or a generation [[Def-EM-0.3-Generation (reductive)]].

PROP : CLGC : 0.2 : We refer to `x` as the `action` isomorphic to the [[Def-EM-0.1-Initial_Cause]], and `y` as the `expectation`, isomorphic to the [[Def-EM-0.2-Final_Cause]], when modeled as a generation. 

PROP : CLGC : 0.3 : When modeled as a succession, the `action` is isomorphic to the input [[Axiom-PC-0.1-Observation]] while the `expectation` is isomorphic to the [[Def-PC-0.4-Evaluation]].

PROP : CLGC : 0.4 : There are two types of commands:
	1. Event-based
	2. Imperative

PROP : CLGC : 0.5 : An imperative takes the form of `do x` and can be formulated as a proposition of the form,  `x is the case at a future point in time`, or using our temporal logic $(x = A)$. The `future point in time` may be either, the next observation or the generation that is the expression of the succession. 

![[PROP-CLGC-0.6]]

PROP : CLGC : 0.7 : A command executed in a single succession is instantaneous.

PROP : CLGC : 0.8 : The result of a command can be justified via the $reticulation$ of liminal space(s) modeled by [[Axiom-PC-0.3-GD_Substitution]] and elucidated in [[Process Representation]].

PROP : CLGC : 0.9 : A command executed over a generation, takes time to execute. 

PROP : CLGC : 1.0 : Currently we utilize three event  based commands, where the action is a `hand gesture`.

PROP : CLGC : 1.1 : We represent a hand gesture using the following forms:
	POC : 
```
	(
		finger: (
			p, 
			(
				m(
					p
				)
			), 
			(
				m(
					m(
						p
					)
				)
			) 
			.
			.
			. 
			(
				m(
					m(
						m(
							m(
								m(
									m(
										m(
											m(
												p
											)
										)
									)
								)
							)
						)
					)
				)
			)
		), 
		region: ( 
			(
				p 
				.
				.
				.
				m(
					m(
						m(
							p
						)
					)
				)
			)
		)
	),
	contact : (
		p1 : POC, 
		p2: POC
	)

PROP : CLGC : 2.0 : We can represent a command using the process calculus where the user is represented as the process, `F`:

Given:
```

prop: string = 'F has a headache'
p1: POC = (1, 0)
p2: POC = (0, 1)
g: Contact = (p1 : POC, p2: POC)
final_cause = (~prop)
```

The execution of the command is the observation:
```

prop ) g ) F ) prop
```

We may abstract away the information of this observation using the form:
```

(initial_cause, final_cause, source_of_information)
```

In the case of our example:
```

(g, ~prop, SBE+)
```

This command may be interpreted as:

The user touches the tip of their index finger to the tip of their thumb to alleviate a headache.
```

