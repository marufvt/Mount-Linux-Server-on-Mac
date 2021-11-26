# Mount Linux Server on Mac

This readme file contains the commands to mount linus server file system onto Mac file system (finder). 

## STEP 1. Installation

First, we need to install macFUSE and SSHFS. I have downloaded both of them from [here](https://osxfuse.github.io/) and finished installation by running the .dmg/.pkg files.

## STEP 2. Create New Directory in Local Machine

On my mac, I created a local directory `lambdapgml` into my desktop folder. I want to mount `/home/maruf` directory of `lambdapgml.cs.vt.edu` linux server into that folder.

## STEP 3. Terminal Commands

I follow the following instruction to mount the desired folder into my local machine:

```
sshfs maruf@lambdapgml.cs.vt.edu:/home/maruf/ /Users/samu/Desktop/lambdapgml -ovolname=lambdapgml
```

To unmount I follow this:

```
umount -f /Users/samu/Desktop/lambdapgml
```

To mount a different folder of `lambdapgml.cs.vt.edu` linux server:

```
sshfs maruf@lambdapgml.cs.vt.edu:/raid/maruf/ /Users/samu/Desktop/raid-maruf -ovolname=raid-maruf
```

To unmount it:

```
umount -f /Users/samu/Desktop/raid-maruf
```
