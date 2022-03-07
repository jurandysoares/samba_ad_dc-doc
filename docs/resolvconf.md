# Resolvconf.md

O cliente DNS do servidor deve ser configurado para máquina local. A maneira mais prática de fazer isso é instalar o pacote `resolvconf` e editar o arquivo `/etc/resolvconf/resolv.conf.d/head`, inserindo nele o conteúdo:

```
nameserver 127.0.0.1
```

Comandos:

- `apt install resolvconf`
- `nano /etc/resolvconf/resolv.conf.d/head`
- `systemctl restart resolvconf`

