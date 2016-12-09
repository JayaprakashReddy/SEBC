```
region, AMI ID, and OS
ap-southeast-1a, i-ac16d60b, CentOS 6.5 (x86_64)
ap-southeast-1a, i-ad16d60a, CentOS 6.5 (x86_64)
ap-southeast-1a, i-af16d608, CentOS 6.5 (x86_64)
ap-southeast-1a, i-b216d615, CentOS 6.5 (x86_64)
ap-southeast-1a, i-b316d614, CentOS 6.5 (x86_64)
```

```
Available disk volume =46GB

[root@ip-10-0-0-107 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        50G  845M   46G   2% /
tmpfs           3.7G     0  3.7G   0% /dev/shm

```

```
[root@ip-10-0-0-107 ~]# yum repolist enabled
Loaded plugins: fastestmirror, presto
Loading mirror speeds from cached hostfile
 * base: mirror.0x.sg
 * extras: mirror.0x.sg
 * updates: mirror.0x.sg
base                                                                                                              | 3.7 kB     00:00
extras                                                                                                            | 3.4 kB     00:00
updates                                                                                                           | 3.4 kB     00:00
repo id                                                     repo name                                                              status
base                                                        CentOS-6 - Base                                                        6,696
extras                                                      CentOS-6 - Extras                                                         62
updates                                                     CentOS-6 - Updates                                                       686
repolist: 7,444

```

```
[root@ip-10-0-0-107 ~]# grep 'orchard\|raffles' /etc/passwd
orchard:x:2800:500::/home/orchard:/bin/bash
raffles:x:2700:501::/home/raffles:/bin/bash


[root@ip-10-0-0-107 ~]# grep 'shops\|walks' /etc/group
shops:x:500:
walks:x:501:

```