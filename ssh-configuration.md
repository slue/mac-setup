# SSH Configuration

### Copy old Keys and Config to new Server

* create folder `~/.ssh`
* copy keys into `~/.ssh`
* copy config into `~/.ssh`
* do not forget to copy any identity files used in `~/.ssh/config` \(best place them into `~/.ssh/IdentityFiles`\)

### Store passphrase of keys in Apples Keychain

For each private key use this

```
$ ssh-add -K path/to/privatekey
```

To see all stored keys in Keychain use:

```
$ ssh-add -l
```



