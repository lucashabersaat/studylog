# linux

- A nice general guide: [https://linuxjourney.com/](https://linuxjourney.com/)

## PATH variable
The path variable are the directories the shell looks for the commands.
- [https://linuxize.com/post/how-to-add-directory-to-path-in-linux/](https://linuxize.com/post/how-to-add-directory-to-path-in-linux/)

To add directories permanently to the path variable, add the directory to `/etc/environment` and reboot the machine. The order of the directories in this file define the order in which a command is searched.

Path Var might look like: `PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"`

## Permissions

For files, directories permissions can be set using the command `$ chmod ...`

Show permission: `$ ls -l fileordirectory`
Might give: `drwxr-xr-x 2 pete penguins 4096 Dec 1 11:45`

First part gives type, next rights for user, then for groups and lastly for other users.

`d | rwx | r-x | r-x`

- r: readable
- w: writable
- x: executable
- -: empty
