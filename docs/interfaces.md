# Interfaces de rede

- `ip -br -c -4 a`
- `cat /etc/network/interfaces`

Edite o arquivo `/etc/network/interfaces` e deixe a interface de rede *enp0s9* com endereço IP fixo. É ela que está conectada à rede interna e conversará com as estações (Windows, Linux ou Mac)

```sh
# This file describes the network interfaces available on your system
# and how to activate them. For more information, see interfaces(5).

source /etc/network/interfaces.d/*

# The loopback network interface
auto lo
iface lo inet loopback

# The primary network interface
allow-hotplug enp0s3
iface enp0s3 inet dhcp

allow-hotplug enp0s8
iface enp0s8 inet static
  address 192.168.56.25
  netmask 255.255.255.0

allow-hotplug enp0s9
iface enp0s9 inet static
  address 172.16.15.2
  netmask 255.255.255.0  
```

- `ifdown enp0s9`
- `ifup enp0s9`
- `ip -br -c -4 a`