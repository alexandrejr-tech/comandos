# Linux: arquivos e pastas

## Criar pasta
```bash
mkdir -p ~/projetos
```
`-p` cria as pastas do caminho que não existirem e não dá erro se já existir.

## Copiar arquivos
```bash
cp origem destino
cp /mnt/c/Users/SEU-USUARIO-WINDOWS/.ssh/id_ed25519 ~/.ssh/
```
Copia um ou mais arquivos. O último caminho é sempre o destino.

## Remover pasta vazia
```bash
rmdir ~/cp
```
Só apaga pastas vazias. Seguro: não apaga conteúdo por engano.

## Atenção: um comando por linha
Dois comandos na mesma linha viram um comando só.
Exemplo do erro: `mkdir -p ~/.ssh cp arquivo` criou uma pasta chamada "cp".
Para encadear de propósito, use `&&` entre eles.
