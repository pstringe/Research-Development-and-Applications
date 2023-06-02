---
creation date:		2023-05-29 12:34
modification date:	2023-05-29 12:34
title: 				Propositional Analysis Monday, May 29 2023
tags:
---
## Tasks
- [ ] Implement Propositions resource
	- [x] Implement useFetch method on the frontend ✅ 2023-05-28
	- [x] Turn into a hook ✅ 2023-05-28
	- [x] Implement Post Method for dialectic interface ✅ 2023-05-28
	- [x] Set up controller ✅ 2023-05-28
	- [x] Set up service ✅ 2023-05-28
	- [x] Set up Postgres DB ✅ 2023-05-28
	- [ ] Set up repository resource for Dialectic
		- [ ] research
		- [x] Make sure dialectic entity is imported in app module ✅ 2023-05-29
		- [x] Make sure we are referencing typeOrm in Dialectic module imports ✅ 2023-05-29
		- [x] Inject the repository into the dialectic service ✅ 2023-05-29
		- [x] Remove the Provider service ✅ 2023-05-29
		- [x] Implement service methods ✅ 2023-05-29
		- [x] call service method from controller ✅ 2023-05-29
		- [x] Test ✅ 2023-05-29
	- [x] Implement dialecticService methods ✅ 2023-05-29
		- [x] implement post ✅ 2023-05-29
		- [x] implement findAll ✅ 2023-05-29
	- [x] Implement form to collect data for new dialectic ✅ 2023-05-29
		- [x] Import Dialog ✅ 2023-05-29
		- [x] implement open/close state ✅ 2023-05-29
		- [x] implement state for dialectic title ✅ 2023-05-29
		- [x] Implement Dialogue component ✅ 2023-05-29
		- [x] Add Textfield for title ✅ 2023-05-29
		- [x] Connect Textfield to internal state ✅ 2023-05-29
	
	- [ ] Implement propositions repository
	- [ ] Implement propositions service methods 
		- [ ] implement post
		- [ ] implement findById

## Objective
When a dialectic post request is submitted, a corresponding record is added to the database.

## Notes
* Testing the dialectic resource, currently there are no tables. When we submit a dialectic. We are expecting one table to be created.
* We have the following error:
```
[Nest] 45759  - 05/29/2023, 1:24:14 PM   ERROR [ExceptionsHandler] No metadata for "Dialectic" was found.
EntityMetadataNotFoundError: No metadata for "Dialectic" was found.
    at DataSource.getMetadata (/Users/poitier/Documents/prop_ananlysis_back/src/data-source/DataSource.ts:444:30)
    at Repository.get metadata [as metadata] (/Users/poitier/Documents/prop_ananlysis_back/src/repository/Repository.ts:53:40)
    at Repository.create (/Users/poitier/Documents/prop_ananlysis_back/src/repository/Repository.ts:130:18)
    at DialecticService.create (/Users/poitier/Documents/prop_ananlysis_back/src/dialectic/dialectic.service.ts:17:37)
    at DialecticController.create (/Users/poitier/Documents/prop_ananlysis_back/src/dialectic/dialectic.controller.ts:20:34)
    at /Users/poitier/Documents/prop_ananlysis_back/node_modules/@nestjs/core/router/router-execution-context.js:38:29
    at processTicksAndRejections (node:internal/process/task_queues:95:5)
    at /Users/poitier/Documents/prop_ananlysis_back/node_modules/@nestjs/core/router/router-execution-context.js:46:28
    at /Users/poitier/Documents/prop_ananlysis_back/node_modules/@nestjs/core/router/router-proxy.js:9:17
```
* The dialectic payload is empty. We will add a form to collect data
