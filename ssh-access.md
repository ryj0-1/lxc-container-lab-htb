# SSH Remote Access Configuration

## Install SSH server

apt install openssh-server -y

---

## Enable root login (lab environment only)

PermitRootLogin yes

Restart service:

systemctl restart ssh

---

## Remote connection

ssh root@1x.xx.xx.xx

---
