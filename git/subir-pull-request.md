# Git: subir pull request (PR)

## Criar a PR
```bash
gh pr create --base main --head staging \
  --title "Título da PR" \
  --body-file "pr.md"
```

- `gh`: a CLI do GitHub. Fala com o GitHub pelo terminal, usando a sua conta logada.
- `pr create`: cria um Pull Request.
- `--base main`: branch de destino, onde as mudanças entram quando a PR for aprovada (a produção).
- `--head staging`: branch de origem, de onde saem as mudanças.
- `--title "..."`: o título da PR.
- `--body-file "..."`: a descrição da PR, lida de um arquivo `.md`.
- `\`: no fim da linha, só avisa o terminal que o comando continua na linha de baixo. Dá pra escrever tudo numa linha só sem ele.
