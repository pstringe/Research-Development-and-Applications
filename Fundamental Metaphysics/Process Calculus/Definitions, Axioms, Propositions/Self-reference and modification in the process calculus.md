---
creation date:		2023-05-24 14:32
modification date:	2023-05-24 14:32
title: 				Self-reference and modification in the process calculus
tags:
---
There is still a problem with our system. It's not self-referential which is an essential property for describing observable processes. We can make the system self-referential, by passing a reference to `m` in the input and establishing the convention that when the reference is modified, `m` will be modified. 
1. [Prop] Given `i ) m ) o`  and `i===[i m]`