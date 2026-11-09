# WSL: instalação e uso

## Instalar
```powershell
wsl --install -d Ubuntu
```
Instala o WSL e a distribuição Ubuntu. Rodar no PowerShell como administrador, só na primeira vez.

## Listar distribuições
```powershell
wsl -l -v
```
Mostra as distribuições instaladas, se estão rodando e a versão do WSL. A marcada com * é a padrão.

## Definir a padrão
```powershell
wsl --set-default Ubuntu
```
Faz o comando `wsl` abrir o Ubuntu. Sem isso, pode abrir a distribuição do Docker Desktop.

## Abrir
```powershell
wsl
```
Entra na distribuição padrão. Não precisa de administrador.

## Entrar como root numa distribuição
```powershell
wsl -d Ubuntu -u root
```
`-d` escolhe a distribuição, `-u` escolhe o usuário. Útil para recuperar a senha.

## Trocar a senha de um usuário (como root)
```bash
passwd seu-usuario-linux
```
Define uma nova senha para o usuário informado.

## Sair do Linux
```bash
exit
```
Volta para o PowerShell.

## Acessar arquivos do Windows pelo Linux
```bash
cd /mnt/c/Users/SEU-USUARIO-WINDOWS/
```
O disco C: do Windows aparece em `/mnt/c`. Trabalhar nos projetos dentro do Linux (`~`), não aqui: é mais lento.
