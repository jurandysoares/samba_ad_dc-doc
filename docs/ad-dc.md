# AD DC

Disponibilizar o Samba como Controlador de Domínio (DC em inglês) do Active Directory (AD).

Antes de começar a configurar o Samba para o seu domínio, primeiro desabilite todos os *[daemons](https://pt.wikipedia.org/wiki/Daemon_(computa%C3%A7%C3%A3o)* do samba:

- `samba-ad-dc.service`
- `smbd.service`
- `nmbd.service`
- `winbind.service`

Comando:

- `systemctl disable --now {samba-ad-dc,smbd,nmbd,winbind}.service`

