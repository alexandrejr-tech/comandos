# Git: trocar conteúdo entre branches

Exemplo: passar o que está na `staging` para a `main` (e a `main` antiga para a `staging`).

## 1. Levar a staging para a main
```bash
git checkout main && git branch main-antiga && git reset --hard staging
```
Vai pra `main` · cria um marcador `main-antiga` guardando onde ela está hoje · aponta a `main` pro conteúdo da `staging`.

## 2. Levar a main antiga para a staging
```bash
git checkout staging && git reset --hard main-antiga && git branch -d main-antiga
```
Vai pra `staging` · aponta ela pro conteúdo que a `main` tinha (salvo no marcador) · apaga o marcador.

## 3. Subir as duas
```bash
git push --force-with-lease origin main staging
```
O `--force` é necessário porque as branches não avançaram, trocaram de lugar. O `-with-lease` recusa se alguém tiver empurrado algo que você não viu.
