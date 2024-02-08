## Getting Started 
---

1. An altsch login user is to be created using `sudo passwd altsch`
   
1. Set up password for the user created using `sudo passwd altsch` note: follow the password prompt

1. Switch to the user `altsch` using the `su -altschool` command.

1. Create 4 directories with `mkdir code tests personal misc` command on the `altsch home directory`

## Questions & Solutions
____
1. Change directory to the tests directory using absolute pathname `cd /home/altsch/tests`

1. Change directory to the tests directory using relative pathname `cd ./tests`

1. Use echo command to create a file named fileA with text content ‘Hello A’ in the misc directory `echo "Hello A" > /home/altsch/misc/fileA or echo "Hello A"> ./misc/fileA`

1. Create an empty file named fileB in the misc directory. Populate the file with a dummy content afterwards `touch /home/altsch/misc/fileB`
   
1. Copy contents of fileA into fileC `cp /home/altsch/misc/fileA /home/altsch/misc/fileC`

1. Move contents of fileB into fileD `mv /home/altsch/misc/fileB /home/altsch/misc/fileD`

1. Create a tar archive called misc.tar for the contents of misc directory `tar -cvf misc.tar misc`

1. gCompress the tar archive to create a misc.tar.gz file `gzip misc.tar`

1. Create a user and force the user to change his/her password upon login `a user was created with useradd -m -s /usr/bin/bash 'username' and set the default password of the user with sudo chage -d 0 'username'`

1. Lock a users password `sudo passwd -l 'username'`

1. Create a user with no login shell `sudo useradd -s /usr/sbin/nologin 'username'`

1. Disable password based authentication for ssh `change to root with cd /; cd /etc; find sshd_config file(copy the file before you continue if neccesary); in the file, after disable tunneled clear text password...uncomment PasswordAuthentication no`

1. Disable root login for ssh `in the same sshd_config, after permit RootLogin prohibit password, write PermitRootLogin no`