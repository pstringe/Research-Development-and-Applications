---
creation date:		2023-05-31 11:38
modification date:	2023-05-31 11:38
title: 				Implement Post method for propositions
tags:
---
## Tasks
## Notes
### Fixing Dialectic
* We have the following error:
```
[Nest] 21020  - 05/31/2023, 11:32:14 AM   ERROR [ExceptionsHandler] date/time field value out of range: "1685547133969"
QueryFailedError: date/time field value out of range: "1685547133969"
    at PostgresQueryRunner.query (/Users/poitier/Documents/prop_ananlysis_back/src/driver/postgres/PostgresQueryRunner.ts:299:19)
    at processTicksAndRejections (node:internal/process/task_queues:95:5)
    at InsertQueryBuilder.execute (/Users/poitier/Documents/prop_ananlysis_back/src/query-builder/InsertQueryBuilder.ts:163:33)
    at SubjectExecutor.executeInsertOperations (/Users/poitier/Documents/prop_ananlysis_back/src/persistence/SubjectExecutor.ts:434:42)
    at SubjectExecutor.execute (/Users/poitier/Documents/prop_ananlysis_back/src/persistence/SubjectExecutor.ts:137:9)
    at EntityPersistExecutor.execute (/Users/poitier/Documents/prop_ananlysis_back/src/persistence/EntityPersistExecutor.ts:182:21)
    at DialecticService.create (/Users/poitier/Documents/prop_ananlysis_back/src/dialectic/dialectic.service.ts:22:5)
    at DialecticController.create (/Users/poitier/Documents/prop_ananlysis_back/src/dialectic/dialectic.controller.ts:20:12)
    at /Users/poitier/Documents/prop_ananlysis_back/node_modules/@nestjs/core/router/router-execution-context.js:46:28
    at /Users/poitier/Documents/prop_ananlysis_back/node_modules/@nestjs/core/router/router-proxy.js:9:17
```

* Postgres types related to time:
```
`timetz`, 
`timestamptz`, 
`timestamp`, 
`timestamp without time zone`, 
`timestamp with time zone`, 
`date`, 
`time`, 
`time without time zone`, 
`time with time zone`
```

* Our date fields are of type, timestamp.
* We need to review the format of JS dates and check for more compatible alternatives.
* We've changed the column annotations in our entity definition to timestamp. It seems to have had no effect on the error.
* Typeorm has issues with postgres timestamps the solution was to use their custom decorators:
```
@CreateDateColumn()
@UpdateDateColumn()  
```
* Regarding the data updates, we can store propositions on the responses of dialectic requests. And pass them as a prop to the proposition component. This will work initially, but we will want to consider more efficient state management in a sooner rather than later iteration.

- [x] Add 1:M constraints and M:1 ✅ 2023-05-31
- [x] Add relations property in find method ✅ 2023-05-31
- [ ] Implement post on frontend for propositions
- [ ] Write a function to parameterize a route.
- [ ] Implement refresh 

```
[Nest] 27038  - 05/31/2023, 2:29:16 PM   ERROR [ExceptionHandler] Nest can't resolve dependencies of the DialecticService (?). Please make sure that the argument DialecticRepository at index [0] is available in the PropositionModule context.

Potential solutions:
- Is PropositionModule a valid NestJS module?
- If DialecticRepository is a provider, is it part of the current PropositionModule?
- If DialecticRepository is exported from a separate @Module, is that module imported within PropositionModule?
  @Module({
    imports: [ /* the Module containing DialecticRepository */ ]
  })

Error: Nest can't resolve dependencies of the DialecticService (?). Please make sure that the argument DialecticRepository at index [0] is available in the PropositionModule context.

Potential solutions:
- Is PropositionModule a valid NestJS module?
- If DialecticRepository is a provider, is it part of the current PropositionModule?
- If DialecticRepository is exported from a separate @Module, is that module imported within PropositionModule?
  @Module({
    imports: [ /* the Module containing DialecticRepository */ ]
  })

    at Injector.lookupComponentInParentModules (/Users/poitier/Documents/prop_ananlysis_back/node_modules/@nestjs/core/injector/injector.js:247:19)
    at Injector.resolveComponentInstance (/Users/poitier/Documents/prop_ananlysis_back/node_modules/@nestjs/core/injector/injector.js:200:33)
    at resolveParam (/Users/poitier/Documents/prop_ananlysis_back/node_modules/@nestjs/core/injector/injector.js:120:38)
    at async Promise.all (index 0)
    at Injector.resolveConstructorParams (/Users/poitier/Documents/prop_ananlysis_back/node_modules/@nestjs/core/injector/injector.js:135:27)
    at Injector.loadInstance (/Users/poitier/Documents/prop_ananlysis_back/node_modules/@nestjs/core/injector/injector.js:61:13)
    at Injector.loadProvider (/Users/poitier/Documents/prop_ananlysis_back/node_modules/@nestjs/core/injector/injector.js:88:9)
    at /Users/poitier/Documents/prop_ananlysis_back/node_modules/@nestjs/core/injector/instance-loader.js:56:13
    at async Promise.all (index 4)
    at InstanceLoader.createInstancesOfProviders (/Users/poitier/Documents/prop_ananlysis_back/node_modules/@nestjs/core/injector/instance-loader.js:55:9)
```

* This error showed up when I imported the dialectic service into the repository service.
* My assumption was, since the repository is available where the service is defined. It should be available wherever it is used
* The service should only be available in one place since we are using dependency injection.

* Questions
	* Why doesn't the dialectRepository seem available in the proposition's module?
* We needed to remove the dialectic service from the providers array of the propositions module, and add the DialecticModule to the imports array of the Propositions module.

### Join columns error
We have the following error:
```
[Nest] 27492  - 05/31/2023, 3:52:28 PM   ERROR [ExceptionsHandler] Cannot read properties of undefined (reading 'joinColumns')
TypeError: Cannot read properties of undefined (reading 'joinColumns')
    at /Users/poitier/Documents/prop_ananlysis_back/src/query-builder/SelectQueryBuilder.ts:2319:39
    at Array.map (<anonymous>)
    at SelectQueryBuilder.createJoinExpression (/Users/poitier/Documents/prop_ananlysis_back/src/query-builder/SelectQueryBuilder.ts:2257:57)
    at SelectQueryBuilder.getQuery (/Users/poitier/Documents/prop_ananlysis_back/src/query-builder/SelectQueryBuilder.ts:87:21)
    at SelectQueryBuilder.getQueryAndParameters (/Users/poitier/Documents/prop_ananlysis_back/src/query-builder/QueryBuilder.ts:507:28)
    at SelectQueryBuilder.loadRawResults (/Users/poitier/Documents/prop_ananlysis_back/src/query-builder/SelectQueryBuilder.ts:3745:40)
    at SelectQueryBuilder.executeEntitiesAndRawResults (/Users/poitier/Documents/prop_ananlysis_back/src/query-builder/SelectQueryBuilder.ts:3541:37)
    at SelectQueryBuilder.getRawAndEntities (/Users/poitier/Documents/prop_ananlysis_back/src/query-builder/SelectQueryBuilder.ts:1670:40)
    at SelectQueryBuilder.getMany (/Users/poitier/Documents/prop_ananlysis_back/src/query-builder/SelectQueryBuilder.ts:1760:36)
    at EntityManager.find (/Users/poitier/Documents/prop_ananlysis_back/src/entity-manager/EntityManager.ts:1083:14)
```
### Observations
* The error is not produced on startup
* The error occurs when we load the frontend route `/dialectic`, and attempt to fetch the results
* Every requested have failed in this iteration 
### Conjecture
* This error has something to do with the relation between dialectics and propositions. 
* It may be a problem with the entity definition, https://github.com/typeorm/typeorm/issues/2016

* Had to correct the entity references

- [x] wire up the post for submission of proposition ✅ 2023-05-31
- [x] test ✅ 2023-05-31
- The request goes through but need to implement tokenization service






