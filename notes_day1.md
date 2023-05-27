# Notes - Day 1
**Root User**
* On the note of the root user, it's been awhile since I've ever used a distro that had me create a root user and rather a standard user that is part if the group sudo.

**Remote Access(SSH)**
* From my knowledge, the best practice for security is to use key based authentication for SSH. I've always used password based authentication.
[Setting up key based authentication](https://linuxize.com/post/how-to-setup-passwordless-ssh-login/)
* On my Windows host, I used PuttyGen to generate a 4096 bit key pair. I didn't use step 2 since I generated the key on my Windows host.
* On step 2, using a passphrase is great for extra security but usually not specified for automation purposes. Since I am just experimenting, I'll not opt for a passphrase.
* I was wondering how to copy the public key to the authorized_users file but PuttyGen gives you the output to paste.
* I think I had to install openssh-server on WSL, but I thought to start sshd it would be sshd or openssh-server. It was [sudo service ssh status](https://askubuntu.com/questions/1339980/enable-ssh-in-wsl-system).
* According to the Day 1 activity, SSH is already included in WSL.
* Step 3, I didn't know there was a specific program to copy a public ssh key, ssh-copy-id.
* In the ssh_config file, I set PasswordAuthentication no to test. I applied the private key in Putty on my Windows host. It worked but noticed a valid user is still required to login. This passwordless login is great to prevent compromise via keylogger.
* Misc specifics regarding the [~/.ssh/authorized_keys](https://www.howtouselinux.com/post/ssh-authorized_keys-file) file.
