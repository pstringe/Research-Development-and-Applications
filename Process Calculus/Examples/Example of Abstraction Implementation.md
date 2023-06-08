## Example of Abstraction Implementation
```ts
type Value = 'T' | 'F' | 'U' | 'A' | 'R' | 'C'

class Abstraction {
	constrcuctor(symbol: string) {
		this.symbol = symbol
		this.val: Value = T
		this.expression: Abstraction[] = []
	}
	/*
		The value of any thing represented by an abstraction is beyond evaluation, 
		for practical purposes, we will need to apply a pseudo-base-case.
		
		By default, our array of abstractions will be empty to avoid traversal in which, 
		case we can return the value of the abstraction.
	*/
	
	this.value = (): Value => {
		const expression = this.expression;
		if (!this.expression.length){
			return this.val
		}
		let aflag = false;
		for (let abstraction of expression){
			let val = abstraction.value()
			//if we encounter a U or a C, the expression evaluates as C
			if (val == 'U' || val == 'C'){
				this.val = 'C';
				return this.val;
			}
			//if we encounter an F, the expression evaluates as F
			if (val == 'F') {
				this.val = 'F';
				return this.val;
			}
			//if we encounter an A, we set the accepted flag to true
			if (val == 'A'){
				aFlag = true;
			}
		}
		
		//if the loop terminates, the abstractions of the expression only contain true and accepted values
		if (aFlag){
			this.val = 'A'
			return this.val;
		}
		
		//if all abstractions of the expression evaluate to true, we evaluate the expression as true
		this.val = 'T'
		return this.val;
	}
}
```
