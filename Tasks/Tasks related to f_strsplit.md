---
creation date:		2023-07-06 15:25
modification date:	2023-07-06 15:25
title: 				Tasks related to ft_strsplit
tags:
---
- [x] study and deconstruct previous solution ✅ 2023-07-06
- [x] write tests for f_strsplit ✅ 2023-07-03
	- [x] write cmp_array function ✅ 2023-07-03
- [x] define prototype for $fstrplit(x, d)$ in terms of g(x, d , r, i) ✅ 2023-07-03
- [x] write pseudocode for each funciton ✅ 2023-07-03
- [x] translate pseudocode into formal syntax ✅ 2023-07-06
- [x] write a function to append an pointer to memory onto an array ✅ 2023-07-06
- [x] write [[f_bzero]] ✅ 2023-07-03
- [x] write [[f_memalloc]] ✅ 2023-07-03
- [x] write f_free_array() ✅ 2023-07-05
- [x] write f_array_resize() ✅ 2023-07-05
- [x] write f_array_append() ✅ 2023-07-05
- [x] fill cases ✅ 2023-07-05
- [x] copy string in f_array_append ✅ 2023-07-05
	- [x] write f_memccpy ✅ 2023-07-05
- [x] test and record observations ✅ 2023-07-06
- [x] modify array functions to use char* instead of void. (generalize at a later time if useful) ✅ 2023-07-13- 
- [ ] debug f_strsplit, record observations.
* error: error: incomplete type 'char []' where a complete type is required
* We will go back and check on this value if it becomes an issue
* error: Couldn't materialize: couldn't get the value of variable str: read memory from 0x7ff7bf6ffff8 failed (0 of 8 bytes read)
* error: errored out in DoExecute, couldn't PrepareToExecuteJITExpression
- [x] try adding a pointer ✅ 2023-07-13
- [x] allocate memory instead ✅ 2023-07-14
	- [x] Identify existing function ✅ 2023-07-14

* We're debugging this function 
* We've concatenated the first token onto current
* We're about to recur
* i should equal 5
* i = 4
* we did not skip the delimiter
* In the conditional we should be checking the str instead of cur
- [x] Implement change ✅ 2023-07-14
[[2023-07-14]]
* We made some changes, no longer passing an index, just manipulating the pointer.
* Observed a seg-fault when running the changes

Debugging Observations
*  l == 3
* tmp = ""
* we save the first word in tmp

[[2023-08-12]

---
[1^]:: [[Notes related to f_strsplit]]
[2^]:: [[Tasks related to f_strsplit]]
