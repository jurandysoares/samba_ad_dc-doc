# smb.conf

Em seguida, renomeie ou remova a configuração original do samba. Esta etapa é absolutamente necessária antes de provisionar o Samba AD porque, no momento do provisionamento, o Samba criará um novo arquivo de configuração do zero e apresentará alguns erros caso encontre um arquivo `smb.conf` antigo.

Comando:

- `rm /etc/samba/smb.conf`

