## Inicia o projeto
```sh
    npm init -y
```
Usa como dependência de desenvolvimento o typescript
```sh
    npm i -D typescript
``` 
Mudar as configurações do typescript de es2016 para es2020 (não necessário)

```sh
    npx tsc --init
``` 

Para usar o node com typescript é necessário uma dependência

```sh
    npm install -D @types/node
```



### Para gerar o arquivo js a partir de um type...
```sh
     npx tsc src/server.ts
     node src/server.js
``` 
Mass isso não será preciso com os dois passos seguintes, em produção...
```sh
     npm install tsx -D
     npx tsx src/server.ts
``` 
Para automatizar ainda mais mude o package.json
```json
"scripts": {
    "dev": "tsx watch src/server.ts"
}
```
```sh
    npm run dev
``` 

## Eslint
```sh
    npm i eslint @rocketseat/eslint-config -D
```

## Fastify

```sh
    npm i fastify
``` 

## Query Builder

Colocando o query builder knex

```sh
    npm install knex sqlite3
```

## Migrations
 mude o package.json
```json
"scripts": {
    "knex": "node --loader tsx ./node_modules/knex/bin/cli.js --knexfile ./knexfile.ts"
}
```

Para criar novas migrations
```sh
    npm run knex -- migrate:make nome-da-migration
```
Para executar a última migration
```sh
     npm run knex -- migrate:latest
```
Para voltar a ultima migration

```sh
     npm run knex -- migrate:rollback
```
## testes

```sh
     npm i vitest -D
```
```sh
      npm i supertest -D   
```
```sh
      npm i -D @types/supertest
```