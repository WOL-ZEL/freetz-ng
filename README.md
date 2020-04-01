# Welcome to Freetz-NG

```
 _____              _            _   _  ____
|  ___| __ ___  ___| |_ ____    | \ | |/ ___|
| |_ | '__/ _ \/ _ \ __|_  /____|  \| | |  _
|  _|| | |  __/  __/ |_ / /_____| |\  | |_| |
|_|  |_|  \___|\___|\__/___|    |_| \_|\____|

```

Freetz-NG is a fork of Freetz.
All commits not by administrator (svn),
cuma (trac) or fda77 (git) are merged.

### LIBCTEST branch - EXPERIMENTAL!
 - Experimental new devices: 6591 6660 7581 7582
 - Experimental labor for: 6591 7490 7530 7590 1750 1200 2400 3000
 - No AVM sources for labor: 6490 6590 and latest 6591
 - No libmultid: No custom DNS and DHCP server
 - No libctlmgr: No /etc/passwd and /etc/group
    * Run ```modusers load``` to load freetz users
 - ~~LABOR: The whole freetz-config is stored in debug.cfg~~
    * ~~This overwrites your debug.cfg!~~
    * ~~Problem: /var/flash/freetz is empty after a reboot,<br>
      maybe because of missing nick name in kernel for ID.~~
    * ~~To migrate you settings *before* flash a labor:<br>
      ```mknod /var/flash/debug.cfg c $(sed -n 's/ tffs//p' /proc/devices) 98```<br>
      ```cat /var/flash/freetz > /var/flash/debug.cfg```<br>
      ```rm /var/flash/freetz```<br>
      ```mv /var/flash/debug.cfg /var/flash/freetz```<br>~~
 - LABOR: There is no reproducible problem saving the freetz config.<br>
   Maybe it was caused by kernel or systemd experiments, don't know.<br>
   To revert the above in case you executed it: ```modsave char```

### Quickstart:
```
  git clone -b libctest https://github.com/Freetz-NG/freetz-ng ~/libctest
  cd ~/libctest
  make help
  make menuconfig
  make
  make push-firmware
```

### Mirrors:
```
  svn co https://github.com/Freetz-NG/freetz-ng/branches/libctest ~/libctest
  git clone -b libctest https://gitlab.com/Freetz-NG/freetz-ng ~/libctest
  git clone -b libctest https://bitbucket.org/Freetz-NG/freetz-ng ~/libctest
```
### Documentation:
See [docs/](docs/README.md) or [https://freetz-ng.github.io/](https://freetz-ng.github.io/).

