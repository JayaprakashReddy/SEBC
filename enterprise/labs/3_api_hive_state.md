```

```
Starting hive serice
curl -X POST  -u jayaprakashreddy:passw0rd 'http://ec2-52-221-230-106.ap-southeast-1.compute.amazonaws.com:7180/api/v2/clusters/JayaprakashReddy/services/hive/commands/start'
{
  "id" : 430,
  "name" : "Start",
  "startTime" : "2016-12-07T03:56:07.017Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
  
```

```
Stopppiing Hive service

{
  "id" : 435,
  "name" : "Stop",
  "startTime" : "2016-12-07T04:03:28.401Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}


```
Finding the hive service status


{
  "id" : 430,
  "name" : "Start",
  "startTime" : "2016-12-07T03:56:07.017Z",
  "endTime" : "2016-12-07T03:56:29.419Z",
  "active" : false,
  "success" : true,
  "resultMessage" : "Successfully started service.",
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  },
  "children" : {
    "items" : [ {
      "id" : 432,
      "name" : "Start",
      "startTime" : "2016-12-07T03:56:07.083Z",
      "endTime" : "2016-12-07T03:56:29.418Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully started process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVESERVER2-157f71cb7f8a60bed8d4fe4ac4ac27f2"
      }
    }, {
      "id" : 431,
      "name" : "Start",
      "startTime" : "2016-12-07T03:56:07.036Z",
      "endTime" : "2016-12-07T03:56:29.415Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully started process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVEMETASTORE-157f71cb7f8a60bed8d4fe4ac4ac27f2"
      }
    } ]
  }
}

```
