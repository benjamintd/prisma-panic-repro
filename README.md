# Prisma Panic Reproduction

A Prisma Query Engine panic bug when using createManyAndReturn on a model with `@ignore`d columns. 

## Installation 

Initialize a postgres database and copy its connection string in `.env` 

```.env
DATABASE_URL="postgresql://test:test@localhost:5432/prisma-panic-repro"
```

```bash
$ npm install
$ npx prisma migrate dev
```

## Triggering the bug

```bash
$ bun ./script.ts
```
