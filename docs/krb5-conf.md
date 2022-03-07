# Krb5.conf

Finalmente, renomeie ou remova o arquivo de configuração principal do Kerberos do diretório `/etc` e substitua-o usando um link simbólico pelo arquivo Kerberos recém-gerado pelo Samba e que está localizado no caminho `/var/lib/samba/private`:

- `ln -sfv /var/lib/samba/private/krb5.conf /etc`

