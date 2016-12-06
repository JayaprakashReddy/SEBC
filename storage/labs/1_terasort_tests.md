```
teragen command
time hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.8.3.jar teragen -D dfs.block.size=33554432 100000000 /user/jayaprakashreddy/teragen.out
time output
real    1m45.964s
user    0m5.835s
sys     0m0.724s
```

```
terasort command
time hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.8.3.jar terasort /user/jayaprakashreddy/teragen.out /user/jayaprakashreddy/terasort.out
time output
16/12/06 07:45:20 INFO terasort.TeraSort: done

real    15m13.027s
user    0m11.048s
sys     0m1.298s
```