---
creation date:		2023-08-20 11:57
modification date:	2023-08-20 11:57
title: 				Untitled
tags:
---
[[Notes on process composition and self-reference to demonstrate stimulus-response]]

AXIOM : OL : 0.0 : REQM : $(StimM((f, o, g)) := ((Stim(f,\ g,\ o)))$
AXIOM : OL : 0.1 : RESM : $(RespM((f,o,g)) := ((Resp(f,\ g,\ o)))$
AXIOM : OL : 0.2 : REQM : $(StimL((f, o, g)) := ((Stim(f,\ Ma(g),\ o)))$
AXIOM : OL : 0.3 : RESM : $(RespL(f,g,o)) := ((Resp(f,\ Ma(g),\ o)))$  

The following logic encodes the axioms of of CNB:11.0.3-11.0.5 using [[Representative Number Theory]].

**Bound Abstractions of the Prima-Representation**
CODE : OL : 0.4 : $f$ : variable to be encoded
CODE : OL : 0.5 : $o$ : variable to be encoded
CODE : OL : 0.6 : $g$ : variable to be encoded

**Operators**
CODE : OL : 0.07 : 10 : $Ma(x)$ : $m(m(m(m(m(m(m(m(m(m(p))))))))))((x))$
CODE : OL : 0.08 : 08 : $Stim(f, g, x)$ : $m(m(m(m(m(m(m(m(p))))))))((f, x, g))$
CODE : OL : 0.09 : 09 : $Resp(f,g,x)$ : $m(m(m(m(m(m(m(m(m(p)))))))))((f, x, g))$

**Modular Propositions**
CODE : OL : 0.10 : 04 : $ReqM((f, g, c))$ : $m(m(m(m(p))))((f, g, c))$
CODE : OL : 0.11 : 05 : $ResM((f,g, c))$ : $m(m(m(m(m(p))))((f, g, c))$
CODE : OL : 0.12 : 06 : $ResL((f,g,c))$ : $m(m(m(m(m(m(p)))))((f, g, c))$
CODE : OL : 0.13 : 07 : $ReqL((f,g,c))$ : $m(m(m(m(m(m(m(p))))))((f, g, c))$

![[Technical Isomorphisms of Operatic Logic]]

**High Level spatial dependency between government abstractions**
PROP : 0.0 : $(:=\ f\ (f\ g\ ...))$
PROP : 0.1 : $(:=\ g\ (g\ f\ ...))$
PROP : 0.2 : $(:=\ (p\ f)\ ((p\ f)\ (p\ g))\ ...))$
PROP : 0.3 : $(:=\ (p\ g)\ ((p\ f)\ (p\ g) \ ...))$
PROP : 0.4 : $(dep\ f\  (p\ f))$
PROP : 0.5 : $(dep\ g\ (p\ g))$
PROP : 0.6 : $(trvrsbl\ f\ (p\ f))$
PROP : 0.7 : $(trvrsbl\ g\ (p\ g))$

*Operators*
DEF : OL : 0.8 : $=$ : $(m (m (m p)))$ 
DEF : 0L : 0.9 : $:=$ : $(m(m(m(mp))))$
DEF : OL : 1.0 : $\Rightarrow$ : $(m(m(m(mp))))$
 

---
[1^]:: [[Tasks related to the development of operatic logic]]
[2^]:: [[Notes related to the development of operatic calculus]]
