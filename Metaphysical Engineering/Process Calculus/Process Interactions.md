---
creation date:		2023-05-25 16:36
modification date:	2023-05-25 16:36
title: 				Process Interactions
tags:
---

0. [Prop] We represent 2 processes `P0` and `P1` on a graph and connect them via a `temporal edge`.
1. [Def]  *Interface* : We refer to `I` and `O` as interfaces
2. [Def] *Binding* : Given two interfaces, `I` of `PO` and `O` of `P1`, a binding is an abstraction mapping the `abstractions` of interface `I` to the `abstractions` of interface `O` such that the `abstractions` of `I` update with the values of `O` upon `observation`.
3. [Def] *Temporal Edge*: An compound abstraction consisting of `bindings`, the index of which updates upon `observation`
