# SSH: chave para o GitHub

## Gerar uma chave nova (se não tiver)
```bash
ssh-keygen -t ed25519 -C "seu-email"
```
Cria a chave privada (`id_ed25519`) e a pública (`id_ed25519.pub`) em `~/.ssh`.

## Mostrar a chave pública para cadastrar
```bash
cat ~/.ssh/id_ed25519.pub
```
Copiar a linha inteira (começa com `ssh-ed25519`) e colar em github.com/settings/keys > New SSH key > Authentication Key.
Nunca copiar ou enviar a chave privada (o arquivo sem `.pub`).

## Testar a conexão
```bash
ssh -T git@github.com
```
Esperado: "Hi usuario! You've successfully authenticated".
"Permission denied (publickey)" = chave não cadastrada no GitHub.

## Primeira conexão
O SSH pede para confirmar o fingerprint do servidor. Conferir com o publicado pelo GitHub antes de digitar `yes`.
O servidor fica salvo em `~/.ssh/known_hosts`.

## Boa prática
Uma chave para o trabalho e outra para projetos pessoais.
