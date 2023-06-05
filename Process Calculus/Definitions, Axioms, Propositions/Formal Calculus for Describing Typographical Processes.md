0. [Axiom] Given a theorem of the form, `i ) m ) o`, we interpret  `i` as input, `o` as output, and `m`, the middle term as the model.
1. [Axiom] *Substitution*: `i ) m ) o [m := ii] === i ) ii ) o`
2. [Axiom] *Abstraction*: `i ) ii ) o <ii := m> === i ) m ) o`
3. [Axiom] *Model Term*: The middle term in the theorem, the value of which, once the value the first term has been substituted, for all of it's occurrences in the model term, becomes the last term in an evaluation.
4. [Axiom] *Model Abstraction*: Given  `o ) i ) m ) o ) 'o` ,   `o ) m ) 'o`  is a valid theorem where `t === i ) m ) o`.
5. [Axiom] *Model Substitution*: Given `o ) m ) 'o` , substitute the middle term `o ) m ) 'o [m := i ) m ) o] -> o ) i ) m ) o ) 'o` 
6. [Axiom] *Evaluation* : Given `i ) m ) o`  apply the substitution for all occurrences of the value of `i` in the model term, `m` followed by the substitution of all of the of the value of `o` in 
7. [Axiom] *Observation*: Given  `i ) m ) o`  where m is an abstraction and,  `o ) i ) m ) o`  is a valid theorem.