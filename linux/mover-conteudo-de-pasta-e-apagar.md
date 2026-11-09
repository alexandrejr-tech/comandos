# Linux: mover conteúdo de pasta e apagar

Exemplo: tirar tudo de dentro da pasta `proposta/`, colocar na pasta atual e apagar a pasta vazia.

## Fazer o * pegar arquivos ocultos
```bash
shopt -s dotglob
```
Liga uma opção do Bash pra que o `*` também pegue arquivos ocultos (`.git`, `.gitignore`, `.env.example`). Sem isso, você perderia o histórico do git e as configs.

## Mover tudo pra pasta atual
```bash
mv proposta/* .
```
`proposta/*` é a origem, o `.` é o destino (aqui).

## Voltar o * ao normal
```bash
shopt -u dotglob
```
Desliga a opção de novo, pra não te surpreender em comandos futuros.

## Apagar a pasta que ficou vazia
```bash
rm -rf proposta
```
`-r` = recursivo (pasta e conteúdo), `-f` = força (sem perguntar).

## Conferir
```bash
ls -la
```
Lista tudo, incluindo ocultos, pra conferir que os arquivos subiram certo.
