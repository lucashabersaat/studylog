# linux

* A nice general guide: [https://linuxjourney.com/](https://linuxjourney.com/)

## background

The Linux kernel, by Linus Torvalds, is a unified kernel.

Linux system is divided into three main parts:

* Hardware
* Linux kernel: core of a OS, manages hardware and how to interact with it
* User space

### distributions:

* Debian: stable
* RHEL: enterprise
* Ubuntu: personal, based on Debian
* Fedora: cheap red hat
* Linux Mint: light ubuntu
* Gentoo: for pros
* Arch: complete community, dirty hands

## some basic commands

* show os version: `$ lsb_release -a`
* show/concatenate `$ cat [file_name]`

  -

## PATH variable

The path variable are the directories the shell looks for the commands.

* [https://linuxize.com/post/how-to-add-directory-to-path-in-linux/](https://linuxize.com/post/how-to-add-directory-to-path-in-linux/)

To add directories permanently to the path variable, add the directory to `/etc/environment` and reboot the machine. The order of the directories in this file define the order in which a command is searched.

Path Var might look like: `PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"`

## permissions

For files, directories permissions can be set using the command `$ chmod ...`

Show permission: `$ ls -l fileordirectory` Might give: `drwxr-xr-x 2 pete penguins 4096 Dec 1 11:45`

First part gives type, next rights for user, then for groups and lastly for other users.

`d | rwx | r-x | r-x`

* r: readable
* w: writable
* x: executable
* -: empty

## pipes

## ports

Ports of machine are the doors to the world. When a request arrives, the port determines which application should handle the request.

* Overview: [https://www.thomas-krenn.com/de/wiki/Linux\_Netzwerk\_Analyse\_mit\_netstat](https://www.thomas-krenn.com/de/wiki/Linux_Netzwerk_Analyse_mit_netstat)

Use the command `netstat` to list ports. \(eg.`sudo netstat -tulpn`\)

