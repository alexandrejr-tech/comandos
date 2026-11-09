# Linux: navegação

## Ir para a pasta pessoal
```bash
cd ~
```
O `~` é um atalho para `/home/<usuario>`.

## Entrar numa pasta
```bash
cd ~/projetos
```

## Mostrar onde estou
```bash
pwd
```
Print working directory: mostra o caminho completo da pasta atual.

## Listar arquivos
```bash
ls
```
Lista o conteúdo da pasta atual.

```bash
ls -la
```
`-l` mostra detalhes (permissões, dono, tamanho, data), `-a` inclui arquivos ocultos (os que começam com ponto).

## Mostrar o conteúdo de um arquivo
```bash
cat ~/.ssh/id_ed25519.pub
```
Imprime o arquivo inteiro na tela.
