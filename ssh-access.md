# SSH Remote Access Configuration

## Install SSH server

apt install openssh-server -y

---

## Enable root login (lab environment only)

PermitRootLogin yes
⚠ Security note:

PermitRootLogin was enabled only for lab testing and learning purposes.
In production environments this setting should remain disabled and key-based authentication should be used instead.

Recommended production setting:

PermitRootLogin no
PasswordAuthentication no
PubkeyAuthentication yes


Restart service:

systemctl restart ssh

---

## Remote connection

ssh root@1x.xx.xx.xx

---
