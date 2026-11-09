# Git: configuração inicial

## Instalar
```bash
sudo apt install -y git
```
`sudo` roda como administrador, `apt` é o instalador do Ubuntu, `-y` aceita sem perguntar.

## Definir nome e e-mail dos commits
```bash
git config --global user.name "seu-nome"
git config --global user.email "seu-email@exemplo.com"
```
`--global` vale para todos os repositórios desse usuário.

## Trocar de conta (ex.: pessoal ↔ trabalho)
```bash
git config --global user.name "usuario-da-outra-conta"
git config --global user.email "email-da-outra-conta@exemplo.com"
```
Roda de novo os dois comandos com os dados da conta que você quer usar.

## Conferir a configuração
```bash
git config --global --list
```

## Remover uma configuração errada
```bash
git config --global --unset user.emial
```
Apaga a chave informada (ex.: uma criada com erro de digitação).

## Clonar por SSH
```bash
git clone git@github.com:usuario/repositorio.git
```
O endereço SSH fica no botão Code do repositório, aba SSH.
