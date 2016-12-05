1. vm.swappiness

```[root@ip-10-0-0-20 ~]# sysctl vm.swappiness
vm.swappiness = 60

[root@ip-10-0-0-20 ~]# sudo sysctl -w vm.swappiness=1
vm.swappiness = 1
```
2.Show the mount attributes of all volumes
```
[root@ip-10-0-0-20 ~]# mount
/dev/xvde on / type ext4 (rw)
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
```

3.Show the reserve space of any non-root, ext-based volumes
```
No non-rrot ext based volumes
```
```
4.Show that transparent hugepages is disabled
Could not find the file where I am supposed to find this setting for CentOS 6.5 machine "/sys/kernel/mm/transparent_hugepage/enabled
```

```
5.Report the network interface attributes

[root@ip-10-0-0-20 ~]# netstat -i
Kernel Interface table
Iface       MTU Met    RX-OK RX-ERR RX-DRP RX-OVR    TX-OK TX-ERR TX-DRP TX-OVR Flg
eth0       9001   0     1055      0      0      0      715      0      0      0 BMRU
lo        16436   0        0      0      0      0        0      0      0      0 LRU
```

```
6.Show forward and reverse host lookups using getent and nslookup

[root@ip-10-0-0-20 ~]# getent hosts ec2-54-179-182-13.ap-southeast-1.compute.amazonaws.com
10.0.0.20       ec2-54-179-182-13.ap-southeast-1.compute.amazonaws.com
[root@ip-10-0-0-20 ~]# getent hosts 10.0.0.20
10.0.0.20       ip-10-0-0-20.ap-southeast-1.compute.internal
```
```
7.Verify the nscd service is running
[root@ip-10-0-0-20 ~]# sudo service nscd status
nscd (pid 4593) is running...
```
```
8.Verify the ntpd service is running
[root@ip-10-0-0-20 ~]# sudo service ntpd status
ntpd (pid  4659) is running...
```
