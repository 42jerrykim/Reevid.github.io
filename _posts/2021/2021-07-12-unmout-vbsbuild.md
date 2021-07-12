``` bash
error: there're mounted directories to build root. Please unmount them manually to avoid being deleted unexpectly:
        / ==> /home1/jong-min.kim/VBS-ROOT/local/BUILD-ROOTS/scratch.armv7l.0/dev/shm
error: <gbs>some packages failed to be built
```
``` bash
$ sudo umount -n /home1/jong-min.kim/VBS-ROOT/local/BUILD-ROOTS/scratch.armv7l.0/dev/shm
[sudo] password for jong-min.kim:
umount: /home1/jong-min.kim/VBS-ROOT/local/BUILD-ROOTS/scratch.armv7l.0/dev/shm: device is busy.
        (In some cases useful info about processes that use
         the device is found by lsof(8) or fuser(1))
```
``` bash
$ sudo umount -nl /home1/jong-min.kim/VBS-ROOT/local/BUILD-ROOTS/scratch.armv7l.0/dev/shm
```
