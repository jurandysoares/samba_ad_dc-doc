# Hostname

Por fim, configure o nome do host da sua máquina com um nome descritivo, como o nome de um *personagem*, editando os arquivos `/etc/hostname` e `/etc/hosts` ou executando:

- `sed -i s/dybian/PERSONAGEM/g  /etc/hostname /etc/hosts`
- `hostnamectl set-hostname PERSONAGEM`

Troque `PERSONAGEM` pelo nome do personagem escolhido, com letras minúsculas e sem acento.
