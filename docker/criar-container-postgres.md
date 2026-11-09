# Docker: criar container do Postgres

## Criar e rodar o container
```bash
docker run --name nome-do-container -e POSTGRES_USER=seu-usuario -e POSTGRES_PASSWORD=sua-senha -e POSTGRES_DB=nome-do-banco -p 5432:5432 postgres
```
- `--name`: nome do container.
- `-e POSTGRES_USER` / `POSTGRES_PASSWORD`: usuário e senha do banco.
- `-e POSTGRES_DB`: nome do banco criado.
- `-p 5432:5432`: liga a porta 5432 da máquina à do container.
- `postgres`: a imagem usada.

## Ligar de novo depois
```bash
docker start nome-do-container
```
