```
[root@ip-10-0-0-106 yum.repos.d]# ls /etc/yum.repos.d
CentOS-Base.repo       CentOS-Media.repo  cloudera-manager.repo  mysql-community-source.repo
CentOS-Debuginfo.repo  CentOS-Vault.repo  mysql-community.repo

```

```
[root@ip-10-0-0-106 yum.repos.d]# sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql -h  ip-10-0-0-107.ap-southeast-1.compute.internal -utemp -ptemp --scm-host  ip-10-0-0-106.ap-southeast-1.compute.internal scm scm scm

```