```
What is ubertask optimization?
Form CM help it is---
"ubertask optimization, which runs "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings."

```

```
Where in CM is the Kerberos Security Realm value displayed?
Adminstration ->  Settings -> kerberos 
Kerberos Security Realm = HADOOP.COM
```

```
Which CDH service(s) host a property for enabling Kerberos authentication?
zookeeper, YARN, HDFS
```
Look through each service -- you'll notice all of them have a Kerberos property setting.
```
How do you upgrade the CM agents?
Steps to upgrade CM agents.
1.Upgrade CM server
2.Once the upgrdaded server is restarted , CM server Admin Console takes through the rest of the CM agents upgradation process
```

```
Give the tsquery statement used to chart Hue's CPU utilization?
select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName=hue
```
```
Name all the roles that make up the Hive service
Hive Metastore Server, WebHCat Server, HiveServer2, Hive Gateway
```
```
What steps must be completed before integrating Cloudera Manager with Kerberos?
1.Install openldap-clients on the Cloudera Manager Server host
2.krb5-workstation, krb5-libs on ALL hosts
3.Verify the type of encryption used by KDC  (make sure it is AES 256 )
4.Create the Kerberos principal for the Cloudera Manager Server
5. Then use CM wizard to to enable Kerberos integration.
```
* On a strictly technical point, LDAP isn't necessary to install Kerberos. Practically speaking, it's rather pointless not to have some kind of directory service, of course.
* It's more important to note that the encryption type is negotiable among all realm principals.
