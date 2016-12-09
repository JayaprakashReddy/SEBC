```
[hdfs@ip-10-0-0-105 ~]$ hdfs dfs -ls /user
Found 6 items
drwxrwxrwx   - mapred  hadoop           0 2016-12-09 02:21 /user/history
drwxrwxr-t   - hive    hive             0 2016-12-09 02:22 /user/hive
drwxrwxr-x   - hue     hue              0 2016-12-09 02:23 /user/hue
drwxrwxr-x   - oozie   oozie            0 2016-12-09 02:23 /user/oozie
drwxr-xr-x   - orchard orchard          0 2016-12-09 02:26 /user/orchard
drwxr-xr-x   - raffle  raffles          0 2016-12-09 02:26 /user/raffles
```

```
CM API Call
curl -u admin:admin  'http://ip-10-0-0-106.ap-southeast-1.compute.internal:7180/api/v14/hosts'

{
  "items" : [ {
    "hostId" : "i-b316d614",
    "ipAddress" : "10.0.0.104",
    "hostname" : "ip-10-0-0-104.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-0-106.ap-southeast-1.compute.internal:7180/cmf/hostRedirect/i-b316d614",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 7829045248
  }, {
    "hostId" : "i-b216d615",
    "ipAddress" : "10.0.0.105",
    "hostname" : "ip-10-0-0-105.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-0-106.ap-southeast-1.compute.internal:7180/cmf/hostRedirect/i-b216d615",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 7829045248
  }, {
    "hostId" : "i-ad16d60a",
    "ipAddress" : "10.0.0.106",
    "hostname" : "ip-10-0-0-106.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-0-106.ap-southeast-1.compute.internal:7180/cmf/hostRedirect/i-ad16d60a",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 7829045248
  }, {
    "hostId" : "i-ac16d60b",
    "ipAddress" : "10.0.0.107",
    "hostname" : "ip-10-0-0-107.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-0-106.ap-southeast-1.compute.internal:7180/cmf/hostRedirect/i-ac16d60b",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 7829045248
  }, {
    "hostId" : "i-af16d608",
    "ipAddress" : "10.0.0.108",
    "hostname" : "ip-10-0-0-108.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-0-106.ap-southeast-1.compute.internal:7180/cmf/hostRedirect/i-af16d608",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 7829045248
  } ]
}
```