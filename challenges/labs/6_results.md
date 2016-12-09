```
Add raffles as a Sentry administrator

CREATE ROLE sentry_admin;
GRANT ALL ON SERVER server1 TO ROLE sentry_admin;
GRANT ROLE sentry_admin TO GROUP walks;
SHOW TABLES;

```

```

CREATE ROLE overlord;
GRANT ALL ON SERVER server1 TO ROLE overlord;
GRANT ROLE overlord to GROUP walks;


CREATE ROLE worker;
GRANT SELECT ON DATABASE default TO ROLE worker;
GRANT ROLE worker TO GROUP shops;
```
```
[root@ip-10-0-0-104 ~]# kinit orchard@JAYAPRAKASHREDDY.SG
Password for orchard@JAYAPRAKASHREDDY.SG:
[root@ip-10-0-0-104 ~]# klist
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: orchard@JAYAPRAKASHREDDY.SG

Valid starting     Expires            Service principal
12/09/16 05:23:41  12/10/16 05:23:41  krbtgt/JAYAPRAKASHREDDY.SG@JAYAPRAKASHREDDY.SG
        renew until 12/16/16 05:23:41
[root@ip-10-0-0-104 ~]# beeline
2016-12-09 05:23:55,347 WARN  [main] mapreduce.TableMapReduceUtil: The hbase-prefix-tree module jar containing PrefixTreeCodec is not present.  Continuing without it.
Beeline version 1.1.0-cdh5.9.0 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-10-0-0-104.ap-southeast-1.compute.internal@JAYAPRAKASHREDDY.SG
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-10-0-0-104.ap-southeast-1.compute.internal@JAYAPRAKASHREDDY.SG
Connected to: Apache Hive (version 1.1.0-cdh5.9.0)
Driver: Hive JDBC (version 1.1.0-cdh5.9.0)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20161209052424_9290a8ef-2192-415a-9369-a7b851b2982f): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20161209052424_9290a8ef-2192-415a-9369-a7b851b2982f); Time taken: 0.077 seconds
INFO  : Executing command(queryId=hive_20161209052424_9290a8ef-2192-415a-9369-a7b851b2982f): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161209052424_9290a8ef-2192-415a-9369-a7b851b2982f); Time taken: 0.131 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.311 seconds)

```

```
[root@ip-10-0-0-104 ~]# kinit raffles@JAYAPRAKSHREDDY.SG
kinit: Cannot find KDC for requested realm while getting initial credentials
[root@ip-10-0-0-104 ~]# kinit raffles@JAYAPRAKASHREDDY.SG
Password for raffles@JAYAPRAKASHREDDY.SG:
[root@ip-10-0-0-104 ~]# beeline
2016-12-09 05:09:34,349 WARN  [main] mapreduce.TableMapReduceUtil: The hbase-prefix-tree module jar containing PrefixTreeCodec is not present.  Continuing without it.
Beeline version 1.1.0-cdh5.9.0 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-10-0-0-104.ap-southeast-1.compute.internal@JAYAPRAKASHREDDY.SG
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-10-0-0-104.ap-southeast-1.compute.internal@JAYAPRAKASHREDDY.SG
Connected to: Apache Hive (version 1.1.0-cdh5.9.0)
Driver: Hive JDBC (version 1.1.0-cdh5.9.0)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20161209050909_8252954e-a2bc-419d-a525-8c71d21bd80e): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20161209050909_8252954e-a2bc-419d-a525-8c71d21bd80e); Time taken: 0.072 seconds
INFO  : Executing command(queryId=hive_20161209050909_8252954e-a2bc-419d-a525-8c71d21bd80e): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161209050909_8252954e-a2bc-419d-a525-8c71d21bd80e); Time taken: 0.166 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.343 seconds)
```

