# dotfiles-manager

This is a tool to manage your dotfiles and other configuration files that reside in your home folder. The scripts collects them and then you can do the versioning. It has the feature to deploy the files on a new computer.

```
./dotfiles [collect|deploy] {OPTIONS}
Options
        -d|--dry        Simulate a run
        -v|--verbose    Show the name of the files copied
```

For making sure that only the files that you want are copied it has a global whitelist and a locel one. The global blacklist resides in the repository and the local one is in your home folder `~/.dotfiles/whitelist.txt`. You need to whitelist the folders or the files that you want to copy. The purpose of the local whitelist is to allow to backup certain files only for specific computers.

The blacklist is used to ignore files and folders inside the whitelisted folders. It has a globbing feature to ignore files and folders like this `.ssh/id_rsa*`. 

If you don't want to deploy a file from the repository on a specific machine you can blacklist it in the local file.
