# LXC Bridge Network Configuration

## Container creation

lxc-create -n linuxcontainer -t download

Selected:
- ubuntu
- jammy
- amd64

---

## Enable LXC bridge

Edit config:

sudo nano /etc/default/lxc-net

Set:

USE_LXC_BRIDGE="true"

Restart service:

sudo systemctl restart lxc-net

---

## Attach container to bridge

Config file:

/var/lib/lxc/linuxcontainer/config

Network config:

lxc.net.0.type = veth
lxc.net.0.link = lxcbr0
lxc.net.0.flags = up

---

## Static IP assignment

lxc.net.0.ipv4.address = 10.xx.xx.xx/2xx
lxc.net.0.ipv4.gateway = 10.xx.xx.xx

---

## Connectivity test

lxc-start -n linuxcontainer -d
lxc-attach -n linuxcontainer -- ping -c 3 8.8.8.8
