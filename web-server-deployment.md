# Web Server Deployment

## Apache

apt install apache2 -y

Test:

http://10.0.3.50

---

## Nginx container

lxc-create -n web-srv-nginx -t download -- -d ubuntu -r focal -a amd64

Check:

systemctl status nginx
nginx -v

---
