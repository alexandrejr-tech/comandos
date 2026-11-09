# Sequelize: migrations

## Criar uma migration
```bash
pnpm sequelize migration:create --name create-users-table
```
Cria o arquivo da migration. Troque o nome conforme a tabela (ex.: `create-products-table`).
Dentro do arquivo, `ctrl + espaço` mostra as operações disponíveis (ex.: `addColumn`, `removeColumn`).

## Executar as migrations
```bash
pnpm sequelize db:migrate
```
Aplica no banco todas as migrations que ainda não rodaram.

## Desfazer a última migration
```bash
pnpm sequelize db:migrate:undo
```

## Desfazer uma migration específica
```bash
pnpm sequelize db:migrate:undo --name nome-da-migration.js
```
