```
Verify user privileges
[root@ip-172-31-24-86 ~]# kinit jayareddy@HADOOP.COM
Password for jayareddy@HADOOP.COM:
[root@ip-172-31-24-86 ~]# klist
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: jayareddy@HADOOP.COM

Valid starting     Expires            Service principal
12/08/16 03:36:14  12/09/16 03:36:14  krbtgt/HADOOP.COM@HADOOP.COM
        renew until 12/15/16 03:36:14
[root@ip-172-31-24-86 ~]# beeline
2016-12-08 03:36:30,026 WARN  [main] mapreduce.TableMapReduceUtil: The hbase-prefix-tree module jar containing PrefixTreeCodec is not present.  Continuing without it.
Beeline version 1.1.0-cdh5.9.0 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-24-86.ap-southeast-1.compute.internal@HADOOP.COM
scan complete in 3ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-24-86.ap-southeast-1.compute.internal@HADOOP.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.0)
Driver: Hive JDBC (version 1.1.0-cdh5.9.0)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20161208033737_aaa56797-a0e3-4a1d-b2db-b18ae7c27ead): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20161208033737_aaa56797-a0e3-4a1d-b2db-b18ae7c27ead); Time taken: 0.859 seconds
INFO  : Executing command(queryId=hive_20161208033737_aaa56797-a0e3-4a1d-b2db-b18ae7c27ead): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161208033737_aaa56797-a0e3-4a1d-b2db-b18ae7c27ead); Time taken: 0.281 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.538 seconds)

```
```
Create a Sentry role with full authorization
0: jdbc:hive2://localhost:10000/default> CREATE ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20161208034242_042decd0-943e-4ba7-8f77-ee5f390b7de6): CREATE ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20161208034242_042decd0-943e-4ba7-8f77-ee5f390b7de6); Time taken: 0.076 seconds
INFO  : Executing command(queryId=hive_20161208034242_042decd0-943e-4ba7-8f77-ee5f390b7de6): CREATE ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161208034242_042decd0-943e-4ba7-8f77-ee5f390b7de6); Time taken: 0.786 seconds
INFO  : OK
No rows affected (0.881 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT ALL ON SERVER HiveServer2 TO ROLE sentry_admin
. . . . . . . . . . . . . . . . . . . .> ;
INFO  : Compiling command(queryId=hive_20161208035858_f328f3ae-f478-4789-9929-4ea187138795): GRANT ALL ON SERVER HiveServer2 TO ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20161208035858_f328f3ae-f478-4789-9929-4ea187138795); Time taken: 0.104 seconds
INFO  : Executing command(queryId=hive_20161208035858_f328f3ae-f478-4789-9929-4ea187138795): GRANT ALL ON SERVER HiveServer2 TO ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161208035858_f328f3ae-f478-4789-9929-4ea187138795); Time taken: 0.064 seconds
INFO  : OK
No rows affected (0.222 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT ROLE sentry_admin TO GROUP sebc;
INFO  : Compiling command(queryId=hive_20161208035858_b09878ba-5394-4d63-b182-b476e5caa06f): GRANT ROLE sentry_admin TO GROUP sebc
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20161208035858_b09878ba-5394-4d63-b182-b476e5caa06f); Time taken: 0.069 seconds
INFO  : Executing command(queryId=hive_20161208035858_b09878ba-5394-4d63-b182-b476e5caa06f): GRANT ROLE sentry_admin TO GROUP sebc
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161208035858_b09878ba-5394-4d63-b182-b476e5caa06f); Time taken: 0.027 seconds
INFO  : OK
No rows affected (0.113 seconds)

0: jdbc:hive2://localhost:10000/default> GRANT ROLE sentry_admin TO GROUP sebc;
INFO  : Compiling command(queryId=hive_20161208034242_cf166fb5-ff31-44a0-81a5-b3de27135bdb): GRANT ROLE sentry_admin TO GROUP sebc
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20161208034242_cf166fb5-ff31-44a0-81a5-b3de27135bdb); Time taken: 0.087 seconds
INFO  : Executing command(queryId=hive_20161208034242_cf166fb5-ff31-44a0-81a5-b3de27135bdb): GRANT ROLE sentry_admin TO GROUP sebc
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161208034242_cf166fb5-ff31-44a0-81a5-b3de27135bdb); Time taken: 0.1 seconds
INFO  : OK
No rows affected (0.199 seconds)
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20161208034343_f97db709-26e4-4241-885f-079ea52b9fff): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20161208034343_f97db709-26e4-4241-885f-079ea52b9fff); Time taken: 0.082 seconds
INFO  : Executing command(queryId=hive_20161208034343_f97db709-26e4-4241-885f-079ea52b9fff): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161208034343_f97db709-26e4-4241-885f-079ea52b9fff); Time taken: 0.175 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.329 seconds)

```
```
kinit as george, then login to beeline and invoke SHOW TABLES
[root@ip-172-31-24-86 ~]# kinit george@HADOOP.COM
Password for george@HADOOP.COM:
[root@ip-172-31-24-86 ~]# beeline
2016-12-08 04:13:14,455 WARN  [main] mapreduce.TableMapReduceUtil: The hbase-prefix-tree module jar containing PrefixTreeCodec is not present.  Continuing without it.
Beeline version 1.1.0-cdh5.9.0 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-24-86.ap-southeast-1.compute.internal@HADOOP.COM
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-24-86.ap-southeast-1.compute.internal@HADOOP.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.0)
Driver: Hive JDBC (version 1.1.0-cdh5.9.0)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20161208042121_3b5a5dcb-08fd-45b2-86a1-d04eb0360402): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20161208042121_3b5a5dcb-08fd-45b2-86a1-d04eb0360402); Time taken: 0.085 seconds
INFO  : Executing command(queryId=hive_20161208042121_3b5a5dcb-08fd-45b2-86a1-d04eb0360402): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161208042121_3b5a5dcb-08fd-45b2-86a1-d04eb0360402); Time taken: 0.159 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.347 seconds)


```

```
kinit as ferdinand, then login to beeline and invoke SHOW TABLES
[root@ip-172-31-24-86 ~]# kinit ferdinand@HADOOP.COM
Password for ferdinand@HADOOP.COM:
[root@ip-172-31-24-86 ~]# klist
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: ferdinand@HADOOP.COM

Valid starting     Expires            Service principal
12/08/16 04:22:03  12/09/16 04:22:03  krbtgt/HADOOP.COM@HADOOP.COM
        renew until 12/15/16 04:22:03
[root@ip-172-31-24-86 ~]# !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-24-86.ap-southeast-1.compute.internal@HADOOP.COM
-bash: !connect: event not found
[root@ip-172-31-24-86 ~]# beeline
2016-12-08 04:23:02,881 WARN  [main] mapreduce.TableMapReduceUtil: The hbase-prefix-tree module jar containing PrefixTreeCodec is not present.  Continuing without it.
Beeline version 1.1.0-cdh5.9.0 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-24-86.ap-southeast-1.compute.internal@HADOOP.COM
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-24-86.ap-southeast-1.compute.internal@HADOOP.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.0)
Driver: Hive JDBC (version 1.1.0-cdh5.9.0)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20161208042323_ed2ddb9c-c6b0-4ca2-9c8a-5610cf913cc2): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20161208042323_ed2ddb9c-c6b0-4ca2-9c8a-5610cf913cc2); Time taken: 0.078 seconds
INFO  : Executing command(queryId=hive_20161208042323_ed2ddb9c-c6b0-4ca2-9c8a-5610cf913cc2): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161208042323_ed2ddb9c-c6b0-4ca2-9c8a-5610cf913cc2); Time taken: 0.152 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.338 seconds)


```