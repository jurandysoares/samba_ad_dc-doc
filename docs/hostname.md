# Hostname

Por fim, configure o nome do host da sua máquina com um nome descritivo, como o nome de um *personagem*, editando os arquivos `/etc/hostname` e `/etc/hosts` ou executando:

- `PERSONAGEM=pernalonga.seu-nome.lab`
- `sed -i s/${HOSTNAME}/${PERSONAGEM}/g  /etc/hostname /etc/hosts`
- `hostnamectl set-hostname ${PERSONAGEM}`

Troque `pernalonga` pelo nome do personagem escolhido, e `seu-nome` por seu primeiro nome ou um apelido, ambos com letras minúsculas e sem acento.
