---
creation date:		2023-05-28 13:21
modification date:	2023-05-28 13:21
title: 				API
tags:
---
|      |             |                       |                                                           |                            |
| ---- | ----------- | --------------------- | --------------------------------------------------------- | -------------------------- |
| Verb | Resource    | Route                 | Description                                               | Related to Frontend Routes |
| GET  | Proposition | /propositions         | returns array of propositions                             | /propositions/:id          |
| GET  | Proposition | /propositions/:id     | return                                                    | /propositions/:id          |
| POST | Proposition | /proposition          | `{ proposition, tokenization, value }`                    |                            |
| GET  | Token       | /tokens/:match        | return an array of tokens that match the substring :match |                            |
| GET  | Token       | /tokens/?prop_n=val_n | returns an array of tokens where specified                |                            |
| GET  | Dialectic   | /dialectic            | returns array of dialectic entities                       | /dialectic                 |
| GET  | Dialectic   | dialectic/:id         | returns a single dialectic entity                         | /dialectic                 |
| POST | Dialectic   | /dialectic            | {proposition, tokenization, value}                        | /dialectic                 |