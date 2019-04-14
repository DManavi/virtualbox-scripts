
1. On guest OS run

1.1 Linux: 
```sh
dd if=/dev/zero of=/var/tmp/bigemptyfile bs=4096k ; rm /var/tmp/bigemptyfile
```
1.2 Windows
Download SDelete from http://technet.microsoft.com/en-us/sysinternals/bb897443 and then run it.

```sh
sdelete.exe c: -z
```

2. Shutdown guest OS
3. Run the command below on the host OS.

```sh
vboxmanage modifymedium --compact /path/to/thedisk.vdi
```
