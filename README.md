# lxc-container-lab-htb

# LXC Container Lab — Networking, Cloning, Resource Control

## Goal

Build isolated Linux containers using LXC with:

- Bridged networking
- Static IP addressing
- Web server deployment (Apache + Nginx)
- Container cloning and templating
- Filesystem export/import
- Resource limits (CPU, RAM, Disk)
- SSH remote access

This lab simulates real-world container administration and security configuration.

---

## Technologies

- LXC
- Ubuntu Jammy / Focal
- Linux bridge (lxcbr0)
- Apache2 / Nginx
- Cgroups v2
- OpenSSH

---

## Architecture

Host
 ├── linuxcontainer (Apache) 10.0.3.50
 ├── web-server-02 (clone)
 ├── new-hacker-box (imported image)
 └── web-srv-nginx (Nginx)

---
