# Notes - Day 0
<br> 
This primarily consists of setting up the VM through a cloud provider or locally. These are some steps I would take post install:
1. sudo apt-get update
2. sudo apt-get upgrade

When you setup a VM, you usually know what OS is installed. Some important information that might be helpful for day 0 would be to figure out what version of the Linux kernel and distribution you are running. I found some ideas for [commands to figure out the kernel version](https://linuxize.com/post/how-to-check-the-kernel-version-in-linux/).

Get information about the system.
```
uname
-a - shows all information
-r - shows kernel release
-v - shows kernel version
-o - shows operating system name
```
Only thing I did not see is the distro name, e.g. Ubuntu, Debian, etc.

Get information about the system(part of systemd, not supported by WSL).
```
hostnamectl
```

