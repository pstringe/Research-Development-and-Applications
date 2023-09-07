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
[1^]:: [[Representative Number Theory]]
[2^]:: [[Tasks related to the development of representative number theory sim]]
[2]:: [[Notes on development of representative number theory sim]]