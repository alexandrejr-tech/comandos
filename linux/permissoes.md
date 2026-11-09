# Linux: permissões

## Ler as permissões no ls -la
```
drwx------   d = pasta, depois três grupos: dono, grupo, outros
-rw-r--r--   r = ler, w = escrever, x = executar, - = sem permissão
```

## Mudar permissões com números
```bash
chmod 700 ~/.ssh                 # só o dono lê, escreve e entra (drwx------)
chmod 600 ~/.ssh/id_ed25519      # só o dono lê e escreve (-rw-------)
chmod 644 ~/.ssh/id_ed25519.pub  # dono lê e escreve, todos leem (-rw-r--r--)
```

## Como somar os números
r = 4, w = 2, x = 1
7 = 4+2+1 (rwx), 6 = 4+2 (rw-), 4 = r--, 0 = ---
Os três dígitos são: dono, grupo, outros.

## Por que a chave SSH precisa de 600
O SSH recusa uma chave privada que outros usuários consigam ler.
