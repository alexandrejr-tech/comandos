# Git: conectar a um repositório remoto

## Apontar o projeto para o repositório
```bash
git remote set-url origin https://SEU-USUARIO@github.com/organizacao/repositorio.git
```
Define a URL do `origin` usando o seu usuário pessoal do GitHub.

## Puxar o conteúdo
```bash
git pull origin master
```
Baixa o que está na branch `master`.

## Reconectar
Depois é só fazer um commit. Vai abrir a janela de login para reconectar.
