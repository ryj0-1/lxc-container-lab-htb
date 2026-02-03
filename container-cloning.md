# Container Cloning and Image Export

## Create template

lxc-copy -n linuxcontainer -N custom-template -p /var/lib/lxc/

---

## Create new container from template

lxc-copy -p /var/lib/lxc/ -n custom-template -N web-server-02

---

## Filesystem export

cd /var/lib/lxc/linuxcontainer/

tar -cvzf /root/custom-image.tar.gz rootfs config

---

## Import as new container

mkdir -p /var/lib/lxc/new-hacker-box

tar -xvzf /root/custom-image.tar.gz -C /var/lib/lxc/new-hacker-box/

Edited config:
- IP address
- hostname

---
