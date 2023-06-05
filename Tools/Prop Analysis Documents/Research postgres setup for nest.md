---
creation date:		2023-05-27 20:59
modification date:	2023-05-27 20:59
title: 				Research postgres setup for nest
source: https://blog.devgenius.io/setting-up-nestjs-with-postgresql-ac2cce9045fe
tags:
---
## Tasks
- [x] open pgAdmin ✅ 2023-05-28
- [x] create a new database in running server ✅ 2023-05-28
- [x] install config `npm install @nestjs/config` ✅ 2023-05-28
- [x] set up env ✅ 2023-05-28
```
DB_HOST='localhost'
DB_PORT=5432
DB_USERNAME='postgres'
DB_PASSWORD='workdb123'
DB_NAME='work_db'
```
- [x] add config module ✅ 2023-05-28
- [x] install typeorm ✅ 2023-05-28
```
npm install @nestjs/typeorm typeormnpm install pg
```
- [x] set up connection configuration in `app.module.ts` ✅ 2023-05-28
- [x] Create an entity for dialectic ✅ 2023-05-28
- [x] Export Dialectic Entity
- [x] Add dialectic entity module to dialectic module imports ✅ 2023-05-28
- [x] test ✅ 2023-05-28
- [x] Debug database error ✅ 2023-05-28
	- [x] Compare the values in the env to the values in pgadmin

## Notes
* We have the following db error:
```
[Nest] 27544  - 05/28/2023, 7:54:49 AM   ERROR [TypeOrmModule] Unable to connect to the database. Retrying (1)...
error: database "prop_analysis" does not exist
    at Parser.parseErrorMessage (/Users/poitier/Documents/prop_ananlysis_back/node_modules/pg-protocol/src/parser.ts:369:69)
    at Parser.handlePacket (/Users/poitier/Documents/prop_ananlysis_back/node_modules/pg-protocol/src/parser.ts:188:21)
    at Parser.parse (/Users/poitier/Documents/prop_ananlysis_back/node_modules/pg-protocol/src/parser.ts:103:30)
    at Socket.<anonymous> (/Users/poitier/Documents/prop_ananlysis_back/node_modules/pg-protocol/src/index.ts:7:48)
    at Socket.emit (node:events:511:28)
    at addChunk (node:internal/streams/readable:332:12)
    at readableAddChunk (node:internal/streams/readable:305:9)
    at Socket.Readable.push (node:internal/streams/readable:242:10)
    at TCP.onStreamRead (node:internal/stream_base_commons:190:23)
```