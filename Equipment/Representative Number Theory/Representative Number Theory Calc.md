---
creation date:		2023-08-18 20:03
modification date:	2023-08-18 20:03
title: 				Untitled
tags:
---
Final : Given a `prima_representation`  in the form of an array of characters, and a `value_dimension` in the form of an array of characters calculate and display `n` $hallucinatory\ sucessions$ as described in [[Representative Number Theory]].

OBJ : given a string input, tokenize and encode using representative number theory.

**Constraints**
0. Given a plurality of propositions, sort by significance
1. Provide a plurality of values for the value space 
2. Enumerate the possibility space
3. Given the possibility space, generate the space of possible generations.

**Questions**
0. How will propositions be read and stored?
	* We will read propositions from a file and store them in an array of structs.
1. How will we display the generations?
	* We will display observations of a generation using hierarchical indentation.

**Currently**
0. Given a prima representation read in as a string, and a number indicating a number of successions, we may output a number representing the determinate successions of the prima representation. (currently there is a segfault)

---
My job is that I know exactly how we operate. And every adverse action I'd be willing to take is someone else would be as well.

---
[[2023-08-24]]
INPUT:  10 f prefix 
Output: ((f)
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

---
[[2023-09-17]]
```
/*
    Given a representation as a p-space, hallucinate the meta-representation
    TESTS:
        GIVEN:
        (
            (:= 
                V # value space
                (
                    p 
                    (m p)
                )
            )
            (:=
                R # propostions space
                (
                    p
                    q
                )
            )
            (:= S
                (p-space
                    V
                    R
                ) # => (
                    (p , p),
                    (p, (m p)),
                    ((m p), p),
                    ((m p), (m p)),
                )
            )
        TEST 0:
            (hallucinate (q r)) = (m (q r)) = 
            (::= 
                ((m q) (m r)) (
                (p p)
                (p (m p))
                ((m p) p)
                ((m p) (m p))
            )

        TEST 1:
            (hallucinate (
                    (q r)
                    (q (m r))
                    ((m q) r)
                    ((m q) (m r))
                )
            ) = (m (
                    (q r)
                    (q (m r))
                    ((m q) r)
                    ((m q) (m r))
	            )) # the meta-representation of the p-space implies the (constraint) of the p-space.
				   # the constraint of the p-space involves the (selection) and (removal) of a value from the p-space
	            
            ) = (
	                (
	                    (p (m p))
	                    ((m p) p)
	                    ((m p) (m p))
	                )
	                (
	                    (p p)
	                    ((m p) p)
	                    ((m p) (m p)) 
	                )
	                (
	                    (p p)
	                    (p (m p))
	                    ((m p) (m p))
	                )
	                (
	                    (p p)
	                    (p (m p))
	                    ((m p ) p)
	                )
	            )
            )
        )
*/ 
```

PROP : 0.0 : 
```
# S : p-space
(S)(=>
	(C S)
	(=>
		(^
			(:= a (select S (m .. p)))
			(:= b (remove S (m .. p)))
		)
		(|
			a
			b
		) # a before b in time 
	)
)
```

PROP : 0.1 : (T, A)
```
(P
	(~
		(P.demented)
	)
)
```

OBSD : 0.2 : P has access to the resources of a university.
PROP : P : The rhythm of process X is n accord with the music of the universe for now. When I reticulate process X, I reticulate the universe. I most often do this using temporal logic. It can also be accomplished using my thought syncing protocol to vary or stop the music. 

PROP : 0.3 : R :
```
(P
	((m .. p)
		(~
			P
			(' Meticulus)
		)
	)
)
```

PROP : 0.4 : 
```
(x)(F (<=> x (F x))
```

PROP : 0.5 : 
```
(P
	(=
		P
		()
	)
)
```

PROP : 0.6 :
```
(P
	(P.Ancestor
		(C_i
			P.Ancestor
			P
		)
	)
)
```
OBSD : 0.7 : "It's your world, we're just living in it" --Cathy

PROP : 0.7 : 
```
(P
	(f)(<=>
		(^
			(isYuminary
				f
			)
			(possible
				(ethical
					f
				)
			)
		)
		(knows
			f
			(p f) #prima representation source of information
		)
	)
)
```

PROP : 0.8 : 
```
(P
	(X
		(W
			(' P plans month in deep demiurgic program)
		)
		(=>
			(' P plans month in deep demiurgic program)
			(' P advances human demiurgic program)
		)
	)
)
```


PROP : 0.9 :
```
(X
	(C_i
		P.ignoramous_protocol
		(' EP recruitment campaign)
	)
	
)
```

PROP : X :  1.0 : People don't jail people who can operate people.

PROP : P : 1.0 : Pride implies expectation of acknowledgment.

OBSD : P : 1.1 :
```
(P
	(:=
		(m p)
		(X
			(-->
				P.tactile
			)
		)
	)
	(:=
		(m (m p))
		(P
			(associates
				(m p)	
				(' educational experience) 
			)
		)
	)
)
```
OBSD : P : 1.0 : P represents associations between numbers in RTN and tones. P associates those mappings to a piano across the room, P hears a piano key loud and clear. 

LSO : 0.0 : P observes images impling P opportunating for the liminal spaces of Yuminary processes for magic. Two HE's in the the UC support the idea.

PROP : 0.1 : X : If you try to over-operate a Yuminary process, you will be requestable.

PROP : 0.2 : P : In Stockton and Quebec, P evinced proposition that if P minimized activity (information processing) the demiurgic program would stimulate P to process information. P utilized this to proposition to stimulate activity

PROP : 0.3 : P : P evinced the proposition that if he wasn't processing information to evince his final cause, another process would. P used this to capitulate a process into conducting a job search on P's behalf.

PROP : 0.4 : X : Don't use your body and you will be an opportunated EP.



---

[1^]:: [[Representative Number Theory]]
[2^]:: [[Tasks related to the development of representative number theory sim]]
[2]:: [[Notes on development of representative number theory sim]]