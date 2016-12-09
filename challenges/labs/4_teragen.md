```
time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.9.0.jar teragen -D dfs.block.size=67108864 -Dmapreduce.job.maps=8 51200000 /user/raffles/tgen512m
```

```
time output 
real    0m58.896s
user    0m5.340s
sys     0m0.720s
```

```
[raffles@ip-10-0-0-105 ~]$ hdfs dfs -ls /user/raffles/tgen512m
Found 9 items
-rw-r--r--   3 raffles raffles          0 2016-12-09 02:44 /user/raffles/tgen512m/_SUCCESS
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 02:43 /user/raffles/tgen512m/part-m-00000
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 02:43 /user/raffles/tgen512m/part-m-00001
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 02:43 /user/raffles/tgen512m/part-m-00002
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 02:43 /user/raffles/tgen512m/part-m-00003
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 02:43 /user/raffles/tgen512m/part-m-00004
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 02:43 /user/raffles/tgen512m/part-m-00005
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 02:44 /user/raffles/tgen512m/part-m-00006
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 02:44 /user/raffles/tgen512m/part-m-00007

```


```
Blocks =80

[raffles@ip-10-0-0-105 ~]$ hdfs fsck /user/raffles/tgen512m/
Connecting to namenode via http://ip-10-0-0-104.ap-southeast-1.compute.internal:50070
FSCK started by raffles (auth:SIMPLE) from /10.0.0.105 for path /user/raffles/tgen512m/ at Fri Dec 09 02:48:20 UTC 2016
.........Status: HEALTHY
 Total size:    5120000000 B
 Total dirs:    1
 Total files:   9
 Total symlinks:                0
 Total blocks (validated):      80 (avg. block size 64000000 B)
 Minimally replicated blocks:   80 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Fri Dec 09 02:48:20 UTC 2016 in 6 millisecond
