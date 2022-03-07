# Provisionamento

Agora, inicie o provisionamento do domínio interativamente emitindo o comando abaixo com privilégios de root e aceite as opções padrão que o Samba fornece.

Além disso, certifique-se de fornecer o endereço IP de um encaminhador de DNS em suas instalações (ou externo) e escolha uma senha forte para a conta de administrador. Se você escolher uma senha de uma semana para a conta de administrador, a provisão do domínio falhará.

Para nosso exemplo, vamos direcionar as consultas para o servidor DNS do Google (`8.8.8.8`) e utilizaremos a senha `Ifrn.2022`.

Execute:

- `samba-tool domain provision --use-rfc2307 --interactive`


Exemplo de interação:

```
root@dybian:~# samba-tool domain provision --use-rfc2307 --interactive
Realm [REDES.LAB]:
Domain [REDES]:
Server Role (dc, member, standalone) [dc]:
DNS backend (SAMBA_INTERNAL, BIND9_FLATFILE, BIND9_DLZ, NONE) [SAMBA_INTERNAL]:
DNS forwarder IP address (write 'none' to disable forwarding) [181.213.132.2]:  8.8.8.8
Administrator password:
Retype password:
```