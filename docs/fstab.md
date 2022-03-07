# fstab

Em seguida, abra o arquivo `/etc/fstab` da máquina e certifique-se de que seu sistema de arquivos de partições tenha *ACLs* habilitadas conforme ilustrado na captura de tela abaixo.

Normalmente, os sistemas de arquivos Linux modernos comuns, como *ext3*, *ext4*, *xfs* ou *btrfs* suportam e têm ACLs habilitadas por padrão. Se esse não for o caso do seu sistema de arquivos, basta abrir o arquivo `/etc/fstab` para edição e adicionar a string `acl` no final da terceira coluna e reinicializar a máquina para aplicar as alterações.

O arquivo deve estar assim:

```
/dev/mapper/dybian--vg-root /               ext4    errors=remount-ro 0       1
UUID=0abf402b-b636-4d70-a3ed-766e0b401f2f /boot           ext2    defaults        0       2
/dev/mapper/dybian--vg-home /home           ext4    defaults        0       2
/dev/mapper/dybian--vg-tmp /tmp            ext4    defaults        0       2
/dev/mapper/dybian--vg-var /var            ext4    defaults        0       2
/dev/mapper/dybian--vg-swap_1 none            swap    sw              0       0
/dev/sr0        /media/cdrom0   udf,iso9660 user,noauto     0       0
```

Por ser uma tabela, você deverá enxergá-lo assim:

| <file system>                                   | <mount point> | <type>      | <options>         | <dump> | <pass> |
| ----------------------------------------------- | ------------- | ----------- | ----------------- | ------ | ------ |
| /dev/mapper/dybian--vg-root                     | /             | ext4        | errors=remount-ro | 0      | 1      |
| UUID=0abf402b-b636-4d70-a3ed-766e0b401f2f /boot | ext2          | defaults    | 0                 | 2      |
| /dev/mapper/dybian--vg-home                     | /home         | ext4        | defaults          | 0      | 2      |
| /dev/mapper/dybian--vg-tmp                      | /tmp          | ext4        | defaults          | 0      | 2      |
| /dev/mapper/dybian--vg-var                      | /var          | ext4        | defaults          | 0      | 2      |
| /dev/mapper/dybian--vg-swap_1                   | none          | swap        | sw                | 0      | 0      |
| /dev/sr0                                        | /media/cdrom0 | udf,iso9660 | user,noauto       | 0      | 0      |
