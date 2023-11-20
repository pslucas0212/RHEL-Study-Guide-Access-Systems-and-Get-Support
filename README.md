# Access Systems and Get Support

[RHEL Study Guide - Table of Contents](https://github.com/pslucas0212/RHEL-Study-Guide)

### Edit Text Files
Use vi or vim to edit text files
```
$ vim filename
```

Four modes of vim:
1. Edit mode - insert
2. Command mode
3. Visual edit mode
4. Extended command mode

Configuration file for vim is located in:
```
$ cat ~/.vimrc
```
## Configure SSH Keys  
Default private and public keys are located in ~/.ssh/id_rsa for the private key and ~/.ssh/id_rsa.pub for the public key

Generate ssh key:
```
$ ssh-keygen
```

Generate ssh keys and specific key names
```
$ ssh-keygen -f ~/.ssh/key_name
```

Copy key to remote host
```
$ ssh-copy-id -i .ssh/key_name user@remote.host.com
```

Non-interactive Authentication when using passphrase (cache passphrase)
```
$ eval $(ssh-agent)
$ ssh-add
```

Troubleshooting ssh keys access.  Add -v, -vv, -vvv for verbose information
```
$ ssh -v user@rmote.host.com
```
