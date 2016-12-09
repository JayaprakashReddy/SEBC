```
Command

hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.9.0.jar  pi 10 100

```

```
[root@ip-10-0-0-104 ~]# kinit  orchard@JAYAPRAKASHREDDY.SG
Password for orchard@JAYAPRAKASHREDDY.SG:
[root@ip-10-0-0-104 ~]# hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.9.0.jar  pi 10 100
Number of Maps  = 10
Samples per Map = 100
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Wrote input for Map #5
Wrote input for Map #6
Wrote input for Map #7
Wrote input for Map #8
Wrote input for Map #9
Starting Job
16/12/09 03:32:31 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-0-104.ap-southeast-1.compute.internal/10.0.0.104:8032
16/12/09 03:32:31 INFO hdfs.DFSClient: Created token for orchard: HDFS_DELEGATION_TOKEN owner=orchard@JAYAPRAKASHREDDY.SG, renewer=yarn, realUser=, issueDate=1481254351878, maxDate=1481859151878, sequenceNumber=2, masterKeyId=2 on 10.0.0.104:8020
16/12/09 03:32:31 INFO security.TokenCache: Got dt for hdfs://ip-10-0-0-104.ap-southeast-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.0.104:8020, Ident: (token for orchard: HDFS_DELEGATION_TOKEN owner=orchard@JAYAPRAKASHREDDY.SG, renewer=yarn, realUser=, issueDate=1481254351878, maxDate=1481859151878, sequenceNumber=2, masterKeyId=2)
16/12/09 03:32:32 INFO input.FileInputFormat: Total input paths to process : 10
16/12/09 03:32:32 INFO mapreduce.JobSubmitter: number of splits:10
16/12/09 03:32:32 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1481253741791_0002
16/12/09 03:32:32 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.0.104:8020, Ident: (token for orchard: HDFS_DELEGATION_TOKEN owner=orchard@JAYAPRAKASHREDDY.SG, renewer=yarn, realUser=, issueDate=1481254351878, maxDate=1481859151878, sequenceNumber=2, masterKeyId=2)
16/12/09 03:32:32 INFO impl.YarnClientImpl: Submitted application application_1481253741791_0002
16/12/09 03:32:33 INFO mapreduce.Job: The url to track the job: http://ip-10-0-0-104.ap-southeast-1.compute.internal:8088/proxy/application_1481253741791_0002/
16/12/09 03:32:33 INFO mapreduce.Job: Running job: job_1481253741791_0002
16/12/09 03:32:42 INFO mapreduce.Job: Job job_1481253741791_0002 running in uber mode : false
16/12/09 03:32:42 INFO mapreduce.Job:  map 0% reduce 0%
16/12/09 03:32:50 INFO mapreduce.Job:  map 30% reduce 0%
16/12/09 03:32:55 INFO mapreduce.Job:  map 60% reduce 0%
16/12/09 03:32:59 INFO mapreduce.Job:  map 80% reduce 0%
16/12/09 03:33:00 INFO mapreduce.Job:  map 90% reduce 0%
16/12/09 03:33:04 INFO mapreduce.Job:  map 100% reduce 0%
16/12/09 03:33:05 INFO mapreduce.Job:  map 100% reduce 100%
16/12/09 03:33:06 INFO mapreduce.Job: Job job_1481253741791_0002 completed successfully
16/12/09 03:33:06 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=99
                FILE: Number of bytes written=1367618
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=3020
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=43
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=10
                Launched reduce tasks=1
                Data-local map tasks=9
                Rack-local map tasks=1
                Total time spent by all maps in occupied slots (ms)=44527
                Total time spent by all reduces in occupied slots (ms)=3703
                Total time spent by all map tasks (ms)=44527
                Total time spent by all reduce tasks (ms)=3703
                Total vcore-seconds taken by all map tasks=44527
                Total vcore-seconds taken by all reduce tasks=3703
                Total megabyte-seconds taken by all map tasks=45595648
                Total megabyte-seconds taken by all reduce tasks=3791872
        Map-Reduce Framework
                Map input records=10
                Map output records=20
                Map output bytes=180
                Map output materialized bytes=340
                Input split bytes=1840
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=340
                Reduce input records=20
                Reduce output records=0
                Spilled Records=40
                Shuffled Maps =10
                Failed Shuffles=0
                Merged Map outputs=10
                GC time elapsed (ms)=386
                CPU time spent (ms)=7590
                Physical memory (bytes) snapshot=4713332736
                Virtual memory (bytes) snapshot=17285226496
                Total committed heap usage (bytes)=4830789632
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=1180
        File Output Format Counters
                Bytes Written=97
Job Finished in 34.919 seconds
Estimated value of Pi is 3.14800000000000000000


```