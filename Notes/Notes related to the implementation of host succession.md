---
creation date:		2023-07-04 16:59
modification date:	2023-07-04 16:59
title: 				Notes related to the implementation of host succession
tags:
---
0. There is at least one observable process P (T)
1. Process P generates evidence to support the existence of other observable processes (T)
	(omit in represative description)
3. Process P represents a list of observable processes, [A, B, C]. Equiv notation: P:[A, B, C]
4. A: [D, E]
5. B: [C, A, D]
6. C: [B]
7. Succession of P's representation

```mermaid
stateDiagram-v2
direction LR
P --> A
A --> B
B --> C
C --> P 
```


7. Succession of A's representation 
```mermaid
stateDiagram-v2
direction LR
A --> D
D --> E
E --> A
```


8. Succession of B's representation
```mermaid
stateDiagram-v2
direction LR
B --> C
C --> A
A --> D
D --> B
```

9. Succession of C's representation
```mermaid
stateDiagram-v2
direction LR
C --> B
B --> C
```

10. Directed Succession Graph
```mermaid
stateDiagram-v2
direction LR
P --> A
A --> B
C --> P 
A --> D
D --> E
E --> A
C --> A
D --> B
C --> B
B --> C
```


11. Recursive representation of directed succession graph
![Recursive representation of a prototypical succession of individual process representation](Recursive%20representation%20of%20a%20prototypical%20succession%20of%20individual%20process%20representation.svg) 

---
[1^]: : [OBJ-ODS-0.1.1_implement_host succession](OBJ-ODS-0.1.1_implement_host%20succession.md)
[2^]: : [Tasks related them implementation of host succession](Tasks%20related%20them%20implementation%20of%20host%20succession.md)