# Infraestrutura do Active Directory com o Samba4

O Samba é um software de código aberto gratuito que fornece uma interoperabilidade padrão entre o sistema operacional Windows e os sistemas operacionais Linux/Unix.

O Samba pode operar como um servidor de arquivos autônomo e servidor de impressão para clientes Windows e Linux por meio do conjunto de protocolos SMB/CIFS ou pode atuar como um Controlador de Domínio Active Directory ou associado a um reino (REALM em inglês) como membro de um domínio . O nível de floresta e domínio do AD DC mais alto que o Samba4 pode emular atualmente é o Windows 2008 R2.

Este tutorial começará explicando todas as etapas que você precisa seguir para instalar e configurar o Samba4 como um controlador de domínio no Debian 11.

Essa configuração fornecerá um ponto de gerenciamento central para usuários, máquinas, compartilhamentos de volume, permissões e outros recursos em uma infraestrutura mista Windows-Linux.

Pré-requisito:

- Instalação de um servidor Debian
- Endereço IP fixo nas interfaces do servidor