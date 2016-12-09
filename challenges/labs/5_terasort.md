```
Command
hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.9.0.jar terasort /user/raffles/tgen512m  /user/raffles/tgen512m.out

```

```
[root@ip-10-0-0-105 ~]# hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.9.0.jar terasort /user/raffles/tgen512m  /user/raffles/tgen512m.out
16/12/09 03:24:37 INFO terasort.TeraSort: starting
16/12/09 03:24:39 INFO hdfs.DFSClient: Created token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@JAYAPRAKASHREDDY.SG, renewer=yarn, realUser=, issueDate=1481253879338, maxDate=1481858679338, sequenceNumber=1, masterKeyId=2 on 10.0.0.104:8020
16/12/09 03:24:39 INFO security.TokenCache: Got dt for hdfs://ip-10-0-0-104.ap-southeast-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.0.104:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@JAYAPRAKASHREDDY.SG, renewer=yarn, realUser=, issueDate=1481253879338, maxDate=1481858679338, sequenceNumber=1, masterKeyId=2)
16/12/09 03:24:39 INFO input.FileInputFormat: Total input paths to process : 8
Spent 428ms computing base-splits.
Spent 3ms computing TeraScheduler splits.
Computing input splits took 431ms
Sampling 10 splits of 80
Making 8 from 100000 sampled records
Computing parititions took 800ms
Spent 1234ms computing partitions.
16/12/09 03:24:40 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-0-104.ap-southeast-1.compute.internal/10.0.0.104:8032
16/12/09 03:24:40 INFO mapreduce.JobSubmitter: number of splits:80
16/12/09 03:24:41 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1481253741791_0001
16/12/09 03:24:41 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.0.104:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@JAYAPRAKASHREDDY.SG, renewer=yarn, realUser=, issueDate=1481253879338, maxDate=1481858679338, sequenceNumber=1, masterKeyId=2)
16/12/09 03:24:42 INFO impl.YarnClientImpl: Submitted application application_1481253741791_0001
16/12/09 03:24:42 INFO mapreduce.Job: The url to track the job: http://ip-10-0-0-104.ap-southeast-1.compute.internal:8088/proxy/application_1481253741791_0001/
16/12/09 03:24:42 INFO mapreduce.Job: Running job: job_1481253741791_0001
16/12/09 03:24:52 INFO mapreduce.Job: Job job_1481253741791_0001 running in uber mode : false
16/12/09 03:24:52 INFO mapreduce.Job:  map 0% reduce 0%
16/12/09 03:25:04 INFO mapreduce.Job:  map 4% reduce 0%
16/12/09 03:25:11 INFO mapreduce.Job:  map 8% reduce 0%
16/12/09 03:25:18 INFO mapreduce.Job:  map 11% reduce 0%
16/12/09 03:25:25 INFO mapreduce.Job:  map 15% reduce 0%
16/12/09 03:25:32 INFO mapreduce.Job:  map 19% reduce 0%
16/12/09 03:25:39 INFO mapreduce.Job:  map 22% reduce 0%
16/12/09 03:25:46 INFO mapreduce.Job:  map 26% reduce 0%
16/12/09 03:25:53 INFO mapreduce.Job:  map 30% reduce 0%
16/12/09 03:26:00 INFO mapreduce.Job:  map 34% reduce 0%
16/12/09 03:26:07 INFO mapreduce.Job:  map 36% reduce 0%
16/12/09 03:26:08 INFO mapreduce.Job:  map 38% reduce 0%
16/12/09 03:26:14 INFO mapreduce.Job:  map 40% reduce 0%
16/12/09 03:26:16 INFO mapreduce.Job:  map 41% reduce 0%
16/12/09 03:26:21 INFO mapreduce.Job:  map 44% reduce 0%
16/12/09 03:26:24 INFO mapreduce.Job:  map 45% reduce 0%
16/12/09 03:26:28 INFO mapreduce.Job:  map 47% reduce 0%
16/12/09 03:26:32 INFO mapreduce.Job:  map 49% reduce 0%
16/12/09 03:26:35 INFO mapreduce.Job:  map 51% reduce 0%
16/12/09 03:26:39 INFO mapreduce.Job:  map 52% reduce 0%
16/12/09 03:26:42 INFO mapreduce.Job:  map 55% reduce 0%
16/12/09 03:26:46 INFO mapreduce.Job:  map 56% reduce 0%
16/12/09 03:26:49 INFO mapreduce.Job:  map 59% reduce 0%
16/12/09 03:26:53 INFO mapreduce.Job:  map 60% reduce 0%
16/12/09 03:26:56 INFO mapreduce.Job:  map 63% reduce 0%
16/12/09 03:27:00 INFO mapreduce.Job:  map 64% reduce 0%
16/12/09 03:27:04 INFO mapreduce.Job:  map 66% reduce 0%
16/12/09 03:27:08 INFO mapreduce.Job:  map 68% reduce 0%
16/12/09 03:27:11 INFO mapreduce.Job:  map 70% reduce 0%
16/12/09 03:27:15 INFO mapreduce.Job:  map 71% reduce 0%
16/12/09 03:27:18 INFO mapreduce.Job:  map 74% reduce 0%
16/12/09 03:27:22 INFO mapreduce.Job:  map 75% reduce 0%
16/12/09 03:27:25 INFO mapreduce.Job:  map 77% reduce 0%
16/12/09 03:27:29 INFO mapreduce.Job:  map 79% reduce 0%
16/12/09 03:27:32 INFO mapreduce.Job:  map 81% reduce 0%
16/12/09 03:27:36 INFO mapreduce.Job:  map 82% reduce 0%
16/12/09 03:27:39 INFO mapreduce.Job:  map 85% reduce 0%
16/12/09 03:27:43 INFO mapreduce.Job:  map 86% reduce 0%
16/12/09 03:27:49 INFO mapreduce.Job:  map 86% reduce 7%
16/12/09 03:27:50 INFO mapreduce.Job:  map 88% reduce 7%
16/12/09 03:27:56 INFO mapreduce.Job:  map 89% reduce 7%
16/12/09 03:28:02 INFO mapreduce.Job:  map 90% reduce 7%
16/12/09 03:28:04 INFO mapreduce.Job:  map 90% reduce 8%
16/12/09 03:28:08 INFO mapreduce.Job:  map 91% reduce 8%
16/12/09 03:28:14 INFO mapreduce.Job:  map 93% reduce 8%
16/12/09 03:28:20 INFO mapreduce.Job:  map 94% reduce 8%
16/12/09 03:28:27 INFO mapreduce.Job:  map 95% reduce 8%
16/12/09 03:28:34 INFO mapreduce.Job:  map 96% reduce 8%
16/12/09 03:28:40 INFO mapreduce.Job:  map 98% reduce 8%
16/12/09 03:28:46 INFO mapreduce.Job:  map 99% reduce 8%
16/12/09 03:28:52 INFO mapreduce.Job:  map 100% reduce 8%
16/12/09 03:28:55 INFO mapreduce.Job:  map 100% reduce 17%
16/12/09 03:28:58 INFO mapreduce.Job:  map 100% reduce 20%
16/12/09 03:29:01 INFO mapreduce.Job:  map 100% reduce 23%
16/12/09 03:29:02 INFO mapreduce.Job:  map 100% reduce 31%
16/12/09 03:29:05 INFO mapreduce.Job:  map 100% reduce 34%
16/12/09 03:29:08 INFO mapreduce.Job:  map 100% reduce 36%
16/12/09 03:29:11 INFO mapreduce.Job:  map 100% reduce 38%
16/12/09 03:29:13 INFO mapreduce.Job:  map 100% reduce 50%
16/12/09 03:29:16 INFO mapreduce.Job:  map 100% reduce 55%
16/12/09 03:29:19 INFO mapreduce.Job:  map 100% reduce 59%
16/12/09 03:29:21 INFO mapreduce.Job:  map 100% reduce 67%
16/12/09 03:29:22 INFO mapreduce.Job:  map 100% reduce 69%
16/12/09 03:29:24 INFO mapreduce.Job:  map 100% reduce 71%
16/12/09 03:29:27 INFO mapreduce.Job:  map 100% reduce 73%
16/12/09 03:29:30 INFO mapreduce.Job:  map 100% reduce 75%
16/12/09 03:29:32 INFO mapreduce.Job:  map 100% reduce 88%
16/12/09 03:29:35 INFO mapreduce.Job:  map 100% reduce 93%
16/12/09 03:29:38 INFO mapreduce.Job:  map 100% reduce 97%
16/12/09 03:29:40 INFO mapreduce.Job:  map 100% reduce 100%
16/12/09 03:29:40 INFO mapreduce.Job: Job job_1481253741791_0001 completed successfully
16/12/09 03:29:40 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=2286477715
                FILE: Number of bytes written=4542173189
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=5120012560
                HDFS: Number of bytes written=5120000000
                HDFS: Number of read operations=264
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=80
                Launched reduce tasks=8
                Data-local map tasks=75
                Rack-local map tasks=5
                Total time spent by all maps in occupied slots (ms)=488231
                Total time spent by all reduces in occupied slots (ms)=273014
                Total time spent by all map tasks (ms)=488231
                Total time spent by all reduce tasks (ms)=273014
                Total vcore-seconds taken by all map tasks=488231
                Total vcore-seconds taken by all reduce tasks=273014
                Total megabyte-seconds taken by all map tasks=499948544
                Total megabyte-seconds taken by all reduce tasks=279566336
        Map-Reduce Framework
                Map input records=51200000
                Map output records=51200000
                Map output bytes=5222400000
                Map output materialized bytes=2244685660
                Input split bytes=12560
                Combine input records=0
                Combine output records=0
                Reduce input groups=51200000
                Reduce shuffle bytes=2244685660
                Reduce input records=51200000
                Reduce output records=51200000
                Spilled Records=102400000
                Shuffled Maps =640
                Failed Shuffles=0
                Merged Map outputs=640
                GC time elapsed (ms)=10702
                CPU time spent (ms)=476720
                Physical memory (bytes) snapshot=46923366400
                Virtual memory (bytes) snapshot=138082750464
                Total committed heap usage (bytes)=42638770176
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=5120000000
        File Output Format Counters
                Bytes Written=5120000000
16/12/09 03:29:40 INFO terasort.TeraSort: done


```

```
[root@ip-10-0-0-105 ~]# hadoop fs -ls /user/raffles/tgen512m.out

Found 10 items
-rw-r--r--   1 raffles raffles          0 2016-12-09 03:29 /user/raffles/tgen512m.out/_SUCCESS
-rw-r--r--  10 raffles raffles         77 2016-12-09 03:24 /user/raffles/tgen512m.out/_partition.lst
-rw-r--r--   1 raffles raffles  640432100 2016-12-09 03:29 /user/raffles/tgen512m.out/part-r-00000
-rw-r--r--   1 raffles raffles  634806600 2016-12-09 03:29 /user/raffles/tgen512m.out/part-r-00001
-rw-r--r--   1 raffles raffles  641525200 2016-12-09 03:29 /user/raffles/tgen512m.out/part-r-00002
-rw-r--r--   1 raffles raffles  635537600 2016-12-09 03:29 /user/raffles/tgen512m.out/part-r-00003
-rw-r--r--   1 raffles raffles  645818900 2016-12-09 03:29 /user/raffles/tgen512m.out/part-r-00004
-rw-r--r--   1 raffles raffles  641189600 2016-12-09 03:29 /user/raffles/tgen512m.out/part-r-00005
-rw-r--r--   1 raffles raffles  639047500 2016-12-09 03:29 /user/raffles/tgen512m.out/part-r-00006
-rw-r--r--   1 raffles raffles  641642500 2016-12-09 03:29 /user/raffles/tgen512m.out/part-r-00007

```
