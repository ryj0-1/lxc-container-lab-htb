# LXC Resource Limiting

## Memory

lxc.cgroup2.memory.max = 512M
lxc.cgroup.memory.memsw.limit_in_bytes = 1G

---

## CPU

lxc.cgroup2.cpu.max = 50000 100000
lxc.cgroup.cpu.shares = 512

---

## Disk

lxc.rootfs.options = size=5G

---

## Verification

free -m

cat /sys/fs/cgroup/memory/lxc/linuxcontainer/memory.limit_in_bytes

df -h /

---
