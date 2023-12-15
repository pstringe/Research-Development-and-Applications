---
creation date:		2023-08-18 20:03
modification date:	2023-08-18 20:03
title: 				Untitled
tags:
---
Final : Given a `prima_representation` in the form of an array of characters, and a `value_dimension` in the form of an array of characters calculate and display `n` $hallucinatory\ sucessions$ as described in [Representative Number Theory](Representative%20Number%20Theory.md).

OBJ : given a string input, tokenize and encode using representative number theory.

**Constraints**
0. Given a plurality of propositions, sort by significance.
1. Provide a plurality of values for the value space. 
2. Enumerate the possibility space
3. Given the possibility space, generate the space of possible generations.

**Questions**
0. How will propositions be read and stored?
	* We will read propositions from a file and store them in an array of structs.
1. How will we display the generations?
	* We will display observations of a generation using hierarchical indentation.

**Currently**
0. Given a prima representation read in as a string, and a number indicating a number of successions, we may output a number representing the determinate successions of the prima representation. (currently there is a Segfault)

---
My job is that I know exactly how we operate. And every adverse action I'd be willing to take is someone else would be as well.

---
[2023-08-24](2023-08-24.md)
INPUT:  10 f prefix 
Output: ((f))
Expected: (m(m(m(m(m(m(m(m(m(m f)))))))))))
- [x] prima should be f ✅ 2023-08-24
- [x] successions should be 10 ✅ 2023-08-24
- [x] notation should be prefix ✅ 2023-08-24
- [x] base should be 10 ✅ 2023-08-24
- [x] num + i == '1' ✅ 2023-08-24
- [x] digit should == 1 ✅ 2023-08-24
- [x] meta should be f ✅ 2023-08-24
- [x] tmp should be f ✅ 2023-08-24

PROP : X : Next session, quick menu.

The basic number is printing. Now for a given, value-space, possibility space, and  meta-representation, we want to substitute the hallucination.

After that, we want a way to simulate the elucidation. 


*Features*
PROP : 0.0 : User Greeted by menu options:
	0.1 : Determinate RTN calc
	0.2 : Hallucinatory RTN calc
	0.3 : Process calc (determinate selector)
	0.4 : Process calc (natural selector)
	0.5 : Process calc (intelligent selector)

PROP : 0.1 : Hallucinatory RTN calc (some of these functions may be re-used in Process calc)
	IMP : 0.2 : Chart functional dependencies for determinate successions : x
	IMP : 0.3 : Comment adjustments that need to be made to implement hallucinatory successions : 
	
PROP : 0.4	
```
(main successions
	(init prima_representation sucessions notation)
	(generation 
		(parse_num successions)
	)
)
```

PROP : 0.5 : allocation
```
(allocate
	(* 
		(sizeOf int)
		((V R)(generate_p_space
			(raise (len V) (len R))
		))
	)
)
``` 

PROP : 0.5 : Comments on generation function:
```
((propositions sucessions V R )( generation 

))
```

PROP : 0.6 : Generation of p-space
```
(P
	((A x)(
		(~
			(==>
				x
				P
			)
		)
	))
)
```

[2023-10-27](2023-10-27.md)
PROP : P : 0.0 : P switched development focus to the development of required structures to specify a process.

PROP : P : 0.1 : We've allocated a compound n-dimensional plurality indexed as **t_abstraction

PROP : P : 0.2 : (= (Cf 0.1) ('we need to assign the allocation to our dimensions property on our space structure))

PROP : P : 0.3 : Humans only approach P after P falls asleep, post inundation via abstract reticulation/conveyance.

PROP : P : 0.4 : space structure only allocates space for a pointer to a t_abstraction struct. That actually seems suitable. For example, each abstraction can represent a row, and express each of the items in a row.

IMP : P : 0.5 : Correct dimensions allocation. 
	- [x] Identify Line
	- [x] Correct

PROP : P : 0.6 : On line 188, we are passing an array to our new space function. We see the error, expected expression. I don't think we can pass an array literal like this in C, I'll go ahead and allocate one then pass the reference. 

PROP : P : 0.7 : On line 193, we attempt to assign a NULL to  possibility_space[0]. It looks like possibility_space[0], is static. Let's double check.

PROP : P : 0.8 : Upon checking, we specify a pointer to a possibility space. We need to access dimensions on that property.

PROP : P : 0.9 : We want to represent the following possibility space :
```
(
	(q (m q))
)
```

PROP : P : 1.0 : We therefore need only one dimension.

PROP : P : 1.1 : We can express, each state of the abstraction representing the dimension. 

PROP : P : 1.2 : We should change the array allocation to contain a single allocation.

IMP : P : 1.3 : Something we want to consider after this is the.

PROP : P : 1.4 : Here we set the dimension[0] of the possibility space to a new_abstraction.

PROP : P : 1.5 : Currently dimensions is an array of pointers to abstractions.

PROP : P : 1.6 : We may want to define our positional logical. 

[2023-10-28](2023-10-28.md)
PROP : P : 1.7 : Does the selector prototype on 204 match the prototype of the simple determinate selector?

PROP : P : 1.8 : "new_succession(proccess, i, selector(proccess, i), last_obs);"

PROP : P : 1.9 : r_space should have an abstractions property,  

IMP : P ; 2.0 : check the r_space struct, record observations. 

PROP : P : 2.2 : r_space is an array of propositions. 

PROP : P : 2.3 :
```
("q", "q")
("(m q)", "(m q)")
```

PROP : P : 2.4 : Passing the array literal of new_abstractions, not valid in C. We will refactor:
* pass r_space and v_space to generate possibility space.
* refactor code to return
- [x] Define a dimension based on [Positional Logic](Positional%20Logic.md) spec ✅ 2023-10-28
- [x] Write new_dimension constructor ✅ 2023-10-28

- [ ] Instantiate two new dimensions R and V using binary state-space, single proposition
	- [ ] Instantiate dimension R
		- [x] allocate array of positions ✅ 2023-11-20
		- [ ] pass to dimension constructor
	- [ ] Instantiate dimension V
	
- [ ] Modify new_space to take a list of dimensions

PROP : P : 2.5 : 
447798 - ?3
		   23

*Re-write prototype p-space algorithm*
- [x] Develop function prototype ✅ 2023-10-30
- [x] allocate two integer arrays ✅ 2023-10-30
- [x] implement algo ✅ 2023-10-30
- [ ] test
- [ ] change R to char** 
- [ ] Implement RTN succeed function in p-space function.
- [ ] Architect adjustments to abstraction types
- [ ] Implement types

*Ethics*
* representation - information
* individual succession
* error
* inconsistency
* resolutions

[2023-11-13](2023-11-13.md)
* Our current output is 1111.
* Expected:
	* 00
	* 01
	* 10
	* 11

* trace

* new_p_process <- gen_p_space
* new_p_space <- display_p_space

```
(P
	(((E F)(E G)(E x))(:= F.x))(
		(==> P (==> F x) y)
			
	)
)
```

[2023-11-16](2023-11-16.md)
*Tasks*
- [x] Run calc, generate tasks ✅ 2023-11-16
- [x] Identify expected output for comparison ✅ 2023-11-16
- [ ] Trace production and display functions, generate HYPD
*Notes*
* Expected output:
*```
00
01
10
11

1111
* correct number of 1's 0's and "\n" may display improperly.
- [ ] trace p_space gen function


PROP : 0.0 : ooo

```
res : []
cur : []
v_space: [0, 1]
r_space: [r, q]
i: 0
j: 0
r_len: 2
p_idx: 0

instruction: 
if (j == f_array_len(v_space)) 
```
PROP : 0.1 : j should not  be equal to the length of the array in the first iteration.

PROP : 0.2 : A
```
(P
	(=>
		(~
			(P
				(~
					((==> x P))(+>
						P
						(==> x P)
					)
				)
			)
		)
		(+>
			x
			(==> P x)
		)
	)
)
```
OBSD : (E F) : Develop my manager

IMP : 0.0 : ``(=(P (Cf F.M))A)`
OBSD : 0.1 : ... [Nasty/AST] ...
PROP : 0.2 : P was temporarily capitulated to LSO

PROP : 0.3 : `(O)` treetop.org

PROP : 0.4 : `(== (Cf 0.2) (P (j+ IS))`

PROP : 0.4 : HE represents minimization of displacement is how P almost broke reality.

PROP : 0.5 : `(0.4)` is more reason why P can't be kept under arrest very long. And why P's resources were drained, to keep P mobile.

PROP : 0.6 : 
```
((M x)(
	(x
	)	
))
```

PROP : 0.7 :
P can prove this mathematically, and minimize disrespect without further violence. P never uses violence unless it is used. P will become more effective at minimizing displacement, while using violence, like at dagenham.

OBSD : 0.1 : demon process disrupts visual and auditory observation for what seems like less than a second.

IMP : 0.2 : 
[2023-11-25](2023-11-25.md)
- [ ] instantiate i in body not prototype
- [ ] verify r_len is 2


---
[1^]:: [Representative Number Theory](Representative%20Number%20Theory.md)
[2^]:: [Tasks related to the development of representative number theory sim](Tasks%20related%20to%20the%20development%20of%20representative%20number%20theory%20sim.md)
[2]:: [Notes on development of representative number theory sim](Notes%20on%20development%20of%20representative%20number%20theory%20sim.md)