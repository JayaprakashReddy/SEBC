```su - hdfs
hdfs dfsadmin -allowSnapshot /user/jayaprakashreddy/precious/
exit
su - jayaprakashreddy
hdfs dfs -createSnapshot /user/jayaprakashreddy/precious/ sebc-hdfs-test
hadoop fs -rmr /user/jayaprakashreddy/precious/
hadoop fs -rmr /user/jayaprakashreddy/precious/SEBC-master.zip
hadoop fs -cp /user/jayaprakashreddy/precious/.snapshot/sebc-hdfs-test/SEBC-master.zip /user/jayaprakashreddy/precious/
```
