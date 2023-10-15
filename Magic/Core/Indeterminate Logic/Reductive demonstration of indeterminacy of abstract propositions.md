---
creation date:		2023-07-20 22:26
modification date:	2023-07-20 22:26
title: 				reductive demonstration of indeterminacy of abstract propositions
tags:
---
PROP-RDIAP-18.0
PROP : RDIAP : 18.0 : Given a set of propositions, $R = (q\ r\ s)$

PROP-RDIAP-19.0
PROP : RDIAP : 19.0 : Given a value set,  $V = (p\ (m\ p))$

PROP-RDIAP-20.0
PROP : RDIAP : 20.0 : Given the possibility space, $S$, is:

$$
\begin{matrix}  
q & r & s\\  
q & r & (m\ s)\\
q & (m\ r) & s\\
q & (m\ r) & (m\ s)\\
(m\ q) & r & s\\
(m\ q) & r & (m\ s)\\
(m\ q) & (m\ r) & s\\
(m\ q) & (m\ r) & (m\ s)\\
\end{matrix}
$$
PROP-RDIAP-21.0
PROP-RDIAP-21.0 : We introduce the concept of significance, as determined by the order of the propositions, 
	EX: $(q\ |\ r)$ : q is more significant than r

PROP-RDIAP-22.0
PROP: RDIAP: 22.0 : In the above possibility space, the value of the proposition p is more significant than the value of proposition q 

PROP-RDIAP-23
PROP : RDIAP : 23: The plurality of propositions, $(q\ r\ s)$, may be abstracted as a single proposition, $a$.

$$
\begin{matrix}  
a & - & -\\
q & r & s\\  
q & r & (m\ s)\\
q & (m\ r) & s\\
q & (m\ r) & (m\ s)\\
(m\ q) & r & s\\
(m\ q) & r & (m\ s)\\
(m\ q) & (m\ r) & s\\
(m\ q) & (m\ r) & (m\ s)\\
\end{matrix}
$$
Such that $(a\ :=\ (q\ r\ s))$.

PROP-RDIAP-24 :
PROP : RDIAP : 24 : The observation of $(p\ p\ p)$ is evinced by $(p\ p\ p)$

PROP-RDIAP-24 :
PROP : RDIAP : 25 : The observation of $(a = (mp))$ may be evinced by any of :
$$
\begin{matrix}  
(m\ p) & (m\ p) & (m\ p)\\
(m\ p) & (m\ p) & p\\
(m\ p) & p & p\\
(m\ p) & p & (m\ p)\\
\end{matrix}
$$

PROP : RDIAP : 26 : When abstracting the propositions, we concern ourselves, with only the most significant propositions in the original space of possibilities.

PROP : RDIAP : 27 : Any of the possibilities of PROP-25, may be considered the [final cause](obsidian://open?vault=Master&file=Research%20and%20Development%2FFundamental%20Metaphysics%2FProcess%20Mechanics%2FDef-EM-0.2-Final_Cause) of a [generation](obsidian://open?vault=Master&file=Research%20and%20Development%2FFundamental%20Metaphysics%2FProcess%20Mechanics%2FDef-EM-0.3-Generation%20(reductive)) where $a$ is the [initial cause](Def-EM-0.1-Initial_Cause)

COMMENT : This PROP-RDIAP-27 is related to strength of evidence.

PROP : RDIAP : 28 : The computation required to elucidate the final cause, is non-deterministic.

*Justification for non-determinism*
JUST : RDIAP-28.1 : Given a [possibility space](DEF-NDC-0.0_possibility-space), representing itself as an [observable process](Def-4.0-Observable_Process). [[Axiom-PC-0.1-Observation]] implies $selection$. 

JUST : RDIAP-28.2 : $Selection$ implies $constraint$ of the [possibility space](DEF-NDC-0.0_possibility-space).

JUST : RDIAP-28.3 : C : That which selects is different from that which is selected. (Contingent upon representation of the selector)

JUST : RDIAP-28.4 : T : That which selects either represents information, or is represented, or both.

JUST : RDIAP-28.5 : C : The selector is represents information

JUST : RDIAP-28.6 : C : The is represented

JUST : RDIAP-28.7 : C : (^ RDIAP-28.6 RDIAP-28.5)

JUST : RDIAP-28.5.1 : (P (=> RDIAP-28.5 (' The selector is a [representative abstraction](Def-TC-0.0-representative_abstraction))))

JUST : RDIAP-28.5.2 : (P (=> RDIAP-28.5.1 (' The selector is an [observable process][Def-4.0-Observable_Process])))

JUST : RDIAP-28.5.3 : (P (=> (^ RDIAP-28.1 RDIAP-28.5.2) (' the $selection$ operation is non-deterministic)))

JUST : RDIAP-28.5.4 : (P (=> (^ (dep [observation] [Axiom-PC-0.1-Observation] $selection$))))

JUST : RDIAP-28.5.5 : (P (=> (^ RDIAP-28.5.3 RDIAP-28.5.4) [observation] [Axiom-PC-0.1-Observation]is non-deterministic)) 

[[Constraint of the possibility space by observation]]



---
[1^]:: [[Tasks related to reductive demonstration of the indeterminacy of abstract propositions]]
[2^]:: [[Probabilistic Logic]]