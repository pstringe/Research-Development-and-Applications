---
creation date:		2023-06-06 18:47
modification date:	2023-06-06 18:47
title: 				Migrate to typescript
tags:
---
## Tasks
- [x] Install ✅ 2023-06-06
- [x] Convert files ✅ 2023-06-06
- [x] Implement types and interfaces from data model ✅ 2023-06-06
- [ ] ERROR in [eslint] src/Propositions.tsx
  Line 26:36:  Parsing error: An element access expression should take an argument
- [ ] Study an existing tsconfig.json file to see if we can identify this flag. Record observations.
- [x] Re initialize the typescript file with `tsc --init` ✅ 2023-06-09
-

# Notes


## [2023-06-09](2023-06-09.md)
### Tasks 
* [ ] Look up an example of using a synthetic event with textfield, record findings
- [x] Restrict the type of refresh method ✅ 2023-06-09
- [ ] TS2686: 'React' refers to a UMD global, but the current file is a module. Consider adding an import instead.
- [ ] 

### Notes
1. We have an issue with imports:
2. Our imported Proportions module is resolved. But our --jsx flag is not set. 
3. I'm using typescript
4. [Hyp Disc] The configuration file being referred to is tsconfig.json
5. When we check the tsconfig we see the flag menthioned in [2.] was added
6. We have 3 files that indicate errors:
	1. useFetch.tsx
	2. App.tsx
	3. Propositions.tsx
	
7. Error in Propositions.tsx:
```
No overload matches this call.  
Overload 1 of 2, '(props: { component: ElementType<any>; } & SystemProps<Theme> & { children?: ReactNode; component?: ElementType<any> | undefined; ref?: Ref<...> | undefined; sx?: SxProps<...> | undefined; } & Omit<...>): Element | null', gave the following error.  
Type 'void[]' is not assignable to type 'ReactNode'.  
Type 'void[]' is not assignable to type 'ReactFragment'.  
The types returned by '[Symbol.iterator]().next(...)' are incompatible between these types.  
Type 'IteratorResult<void, any>' is not assignable to type 'IteratorResult<ReactNode, any>'.  
Type 'IteratorYieldResult<void>' is not assignable to type 'IteratorResult<ReactNode, any>'.
```

8. The error was caused by forgetting the return keyword in a map
9. We have the following error in our handle submit method:
```
Type 'Proposition | Partial<Proposition> | undefined' is not assignable to type 'Proposition | undefined'.  
Type 'Partial<Proposition>' is not assignable to type 'Proposition'.  
Types of property 'id' are incompatible.  
Type 'number | undefined' is not assignable to type 'number'.  
Type 'undefined' is not assignable to type 'number'.ts(2322)
```

10. We type our propositions state variable as a partial of Propositions type
11. Property 'value' does not exist on type 'EventTarget & Element'.ts(2339)
12. I thought we remedied this problem already. I remember that synthetic events work differently than standard events. We have the following code.
```ts
const handleChange = (event: SyntheticEvent) => {
	setInput(event.currentTarget.value);
}
```

13. We have an error where the type of our refresh function is not compatible with the type that is passed on the dialectic method.
14. We have an issue:
15. 