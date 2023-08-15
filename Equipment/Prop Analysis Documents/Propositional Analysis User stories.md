---
creation date:		2023-06-12 16:42
modification date:	2023-06-12 16:42
title: 				Propositional Analysis User stories
tags:
---
# V0
### /dialectic-list
0. A user is shown the `DialecticList` component of dialectic cards when they navigate to the root route
1. A user may press a button to create a new `Dialectic` card
2. A user may click on a dialectic to be directed to `PropositionsList`

### /propositions-list
1. A user may click on a `PropositionsCard` is 

### /propositions:id
0. When navigating to the `/propositions` route, given an `id`, the user is shown a `PropositionalExpression` interface.
1. formatted like a `Feed` of cards
2. A user may click on a proposition to open it's `NLAInterface` (natural language abstraction interface)
3. When the component loads, available abstractions are fetched and loaded into a trie
4. A user may express and assign values to `abstractions` within `expressions` of the `proposition`. Using the rules defined in [[Natural Language Application of Indeterminate Logic]]
5. When a user chooses to express a value, they are presented with an interface that allows them to select from existing abstractions that match the token currently being typed as a prefix in the trie.
6. The user may press enter to select the first presented abstraction
7. If the user has finished typing their token and the corresponding abstraction does not exist, the user may press enter to add the add the abstraction to the trie.
8. Upon submission of the proposition, a check will be made for the diff between the current abstractions and queried abstractions.
9. Any non-existing abstractions will be added.