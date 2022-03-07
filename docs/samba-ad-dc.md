# Samba-ad-dc

Desmascare, inicie e ative os daemons do Controlador de Domínio Samba para o *Active Directory*.

- `systemctl unmask samba-ad-dc.service`
- `systemctl enable --now samba-ad-dc.service`

Verifique se o serviço está ativo ou seu estado.

- `systemctl is-active samba-ad-dc.service`
- `systemctl status samba-ad-dc.service`

É interessante saber quais portas do TCP e do UDP o controlador de domínio disponibiliza:

- `ss -tl`
- `ss -tnl`
- `ss -ul`
- `ss -unl`
- `netstat -tlnup | egrep '(smbd|samba)'`[^1]

[^1]: O comando `netstat` é disponibilizado pelo pacote *net-tools*.

