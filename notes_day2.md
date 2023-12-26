# Notes - Day 2
**RTFM**
Windows equivalent to man is *Get-Help* and/or *help*. 

**Basic outline of Get-Help**
```Get-Help -Name Get-Command -Full/Detailed/Examples/Online/Parameter Noun/ShowWindow```

**help has support of wildcards.**
```help *partialNameOfCommand*```

* *Man* is useful but has a lot of information to parse through.
* *tldr* is an optional addon that can be used to get a summary of a command.
* If you know a keyword or part of a description you can use *apropos* or *man -k*.
```
apropos "ssh"
authorized_keys (5)  - OpenSSH daemon
EVP_KDF-SSHKDF (7ssl) - The SSHKDF EVP_KDF implementation
git-shell (1)        - Restricted login shell for Git-only SSH access
rrsync (1)           - a script to setup restricted rsync users via ssh logins

tldr ssh
authorized_keys (5)  - OpenSSH daemon
EVP_KDF-SSHKDF (7ssl) - The SSHKDF EVP_KDF implementation
git-shell (1)        - Restricted login shell for Git-only SSH access
rrsync (1)           - a script to setup restricted rsync users via ssh logins
```
* Builtin commands within the shell and other commands may not have a manual that can be read by *man*.
* If *man* doesn't have it, *help* can possibly be used to look up information on a command.

**Check type of command**
```
user@vm:~$ type ssh
ssh is /usr/bin/ssh
user@vm:~$ type export
export is a shell builtin
```
* *Info* is used to display documentation in info format.

**Navigate The File Structure**
```man heir``` - gives you a man page of the file structure.
```pwd``` - shows where you currently are in the folder structure.
* *Note the prompt in shell gives you information to as to where you are.*
* Relative vs explicit path, you can cd directly to a location by specifying the full path or relative path if you change the cd to a folder down the path.
* Returning to home folder(~ or %USERPROFILE%)
```
MacOS/Linux
cd

Windows
cd\
```

* ls with attributes, owners(grp and usr), size, date, folder/file name
```
ls -l -t -r

Show hidden files/folders
ls -l -t -r -a

Show hidden files/folders with colors
ls -ltra --color=auto
```
*Note: For MacOS, you have to set color to **always** to get the directories to output a different color. In Linux(Debian), the auto parameter works and displays directories in a different color.*

* Can combine multiple switches with a single -.
* The output of the left hand column 
* A . before a file/folder means it is hidden and ignored by ls unless you use the -a switch.

* Move and remove directories
```
mv sourceDir/folderToMove destFolder/

If directories are empty
rmdir targetFolder

If directories still have files, -r is recursive deletion switch
rm -r targetFolder
```

* Touch - allows you to create files and update the modication time/date for a file.
```
touch fileName
```

**Pushd and popd**
* ```cd -``` moves you back to the previous working directory.
* Pushd and popd operates like a stack data structure.
```
Adds directory to the stack
pushd someDir/someFolder


pushd
Pops the current working directory from memorized working paths and returns you to the previous working directory that is being tracked.
popd
```

