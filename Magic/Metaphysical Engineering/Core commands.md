---
creation date:		2023-07-29 20:25
modification date:	2023-07-29 20:25
title: 				Untitled
tags:

---
![Formal Command Syntax](Formal%20Command%20Syntax.md)
![Command Logic](Command%20Logic.md)

![PROP-CLGC-2.1_Hand_Gestures](PROP-CLGC-2.1_Hand_Gestures.md)

![Basic Gesture Commands](Basic%20Gesture%20Commands.md)
**Duration**
Given:
![PROP-CLGC-0.6](PROP-CLGC-0.6.md)

PROP : CLGC : 2.5 : `x` is an abstraction of information describing our hand gesture.

PROP : CLGC : 2.6 : `y` is an abstraction of information describing an observation. In the [Abstract Representative Calculus](Abstract%20Representative%20Calculus.md), $f(x) \Rightarrow f(y)$.

PROP : CLGC : 2.7 : Given an abstraction of information, `x` we may represent the *meta-representation* as `Mr(x)`.

PROP : CLGC : 2.8 : Given an abstraction of information, `x` we may represent the *prima-representation* as `Pr(x)`.

PROP : CLGC : 2.9 : Every observed abstraction may be represented as a *meta-representation* of it's *prima-representation*.

PROP : CLGC : 3.0 : Given a command of the form `x -> y`, `(x := Pr(x)) ^ (x := Mr(x))`.

PROP : CLGC : 3.1 : Given the command: `(lit, general, SBE+, instantaneous)` we may substitute the actual hand-gesture for it's meta-representation, `lit`, implemented as a generative observation.

EX : CLGC : 3.2 : The user represents the code, `lit`, to trigger a hyper-spatial reticulation of `SBE`.

OBSD : CLGC : 3.3 : Tested with commands `lit` and `lrt`. The results were as expected. Immediate and significant.

PROP : CLGC : 3.4 : We desire the capability to maintain the state after submitting a command.

PROP : CLGC : 3.5 : We may establish a new command `toggle` that takes a command as input.

Given:
![PROP-CLGC-0.6](PROP-CLGC-0.6.md)

PROP : CLGC : 3.6 : The command, `toggle`, de-constructs the command it takes as input and  introduces a piece of global state, `s`.

PROP : CLGC : 3.7 : Given the command, 

PROP : CLGC : 3.8 : When the `toggle` command is submitted, global state is toggled. with another command as input, the state is toggled. 

![Temperature Control (Capitulation) Interface](Temperature%20Control%20(Capitulation)%20Interface.md)

---
[1^]:: [Tasks related to the development of core commands](Tasks%20related%20to%20the%20development%20of%20core%20commands.md)
[2^]:: [Testing of Core Commands](Testing%20of%20Core%20Commands.md)