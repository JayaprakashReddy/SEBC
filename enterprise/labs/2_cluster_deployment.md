```
{
  "timestamp" : "2016-12-07T03:42:08.963Z",
  "clusters" : [ {
    "name" : "JayaprakashReddy",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "229638144"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "229638144"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "1064199782"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "179"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-24-90.ap-southeast-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-157f71cb7f8a60bed8d4fe4ac4ac27f2",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-38e309b9"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-607d936b3d570a4a4d4f15b0b580791f",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-34e309b5"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-939f84879ffe7baac6e5815361bce9b3",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-37e309b6"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-b02a86b508f75d285227b83a2809b489",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-39e309b8"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-d25990ef2c7f3744f9eb7c96bc4529b9",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-36e309b7"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-157f71cb7f8a60bed8d4fe4ac4ac27f2",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-38e309b9"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "box4m2akm3doyv04p632a34m6"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-157f71cb7f8a60bed8d4fe4ac4ac27f2",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-38e309b9"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1zmxiequ6q9my3v5l3m3r1k6z"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "229638144"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-157f71cb7f8a60bed8d4fe4ac4ac27f2",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-38e309b9"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2cbwnkjdf67maaf1ya59r4s22"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-b02a86b508f75d285227b83a2809b489",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-39e309b8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5nd55f05mczg1xn8v5il4xtz1"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-d25990ef2c7f3744f9eb7c96bc4529b9",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-36e309b7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "12fh1axury15fscz4x35y6mej"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-24-90.ap-southeast-1.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "hue"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-157f71cb7f8a60bed8d4fe4ac4ac27f2"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-157f71cb7f8a60bed8d4fe4ac4ac27f2",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-38e309b9"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1ipbb4qhaygu9dkjrlxp8j1vq"
          }, {
            "name" : "secret_key",
            "value" : "SItcFAHLfUAqYLmTmVXYLZs3HQSTyZ"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-24-90.ap-southeast-1.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "229638144"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-157f71cb7f8a60bed8d4fe4ac4ac27f2",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-38e309b9"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8or5rryrqefg7c7figxzrx9t6"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "8"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "2"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "229638144"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "node_manager_java_heapsize",
            "value" : "962592768"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "1024"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "229638144"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "1024"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "yarn_nodemanagers_healthy_thresholds",
          "value" : "{\"warning\":95,\"critical\":\"never\"}"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "ETOUpmcRfas87L5alN8ie3yPFmAIL1"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-157f71cb7f8a60bed8d4fe4ac4ac27f2",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-38e309b9"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1gguykcudddpntu2vsdl95w7z"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-607d936b3d570a4a4d4f15b0b580791f",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-34e309b5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2z8awfivjfm7t7ol5yyxx3fds"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-939f84879ffe7baac6e5815361bce9b3",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-37e309b6"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "vccbriddjh2ka7d09gcqd0j"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-b02a86b508f75d285227b83a2809b489",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-39e309b8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6cwpmvgx2od00rq3wo6efly2n"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-d25990ef2c7f3744f9eb7c96bc4529b9",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-36e309b7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ac5bjg6c7ilfprtz5507uynjc"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-157f71cb7f8a60bed8d4fe4ac4ac27f2",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-38e309b9"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "53"
          }, {
            "name" : "role_jceks_password",
            "value" : "2ntuc7j9rwlsx2is19hznpz90"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "229638144"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3170683699"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/root/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "229638144"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "229638144"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "YsWEgLLgFjtcvHdIcHdnbx2XvYq11K"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "dfs_replication",
          "value" : "1"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "wuEqU2ZDkt44TTkpiFGgTb98YbNSrW"
        }, {
          "name" : "hdfs_datanodes_healthy_thresholds",
          "value" : "{\"warning\":95,\"critical\":\"never\"}"
        }, {
          "name" : "hdfs_free_space_thresholds",
          "value" : "{\"warning\":20,\"critical\":\"never\"}"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "tG2oeCCaNEE3tAJWhOM09szaOByKDS"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-157f71cb7f8a60bed8d4fe4ac4ac27f2",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-38e309b9"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-607d936b3d570a4a4d4f15b0b580791f",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-34e309b5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "12ub4f2u0enim9nqcciy5rrw8"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-939f84879ffe7baac6e5815361bce9b3",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-37e309b6"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b1p42guxgco9hmjvxs8j551nr"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-b02a86b508f75d285227b83a2809b489",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-39e309b8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6hork2w2qnupioljiygutuop"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-d25990ef2c7f3744f9eb7c96bc4529b9",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-36e309b7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cg01sasw38465tmzmm87i73z2"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-157f71cb7f8a60bed8d4fe4ac4ac27f2",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-38e309b9"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8i4exb1i9hjtx84q4f1501yym"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-b02a86b508f75d285227b83a2809b489",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-39e309b8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1e64esvb95gklo9rk3dd3a2hx"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-607d936b3d570a4a4d4f15b0b580791f",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-34e309b5"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/var/lib/hadoop-hdfs/jn"
          }, {
            "name" : "role_jceks_password",
            "value" : "5nolqfixt5rwjppgfy1f5etaz"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-939f84879ffe7baac6e5815361bce9b3",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-37e309b6"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/var/lib/hadoop-hdfs/jn"
          }, {
            "name" : "role_jceks_password",
            "value" : "6rar8uts2pmqwr2ohived1dx8"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-d25990ef2c7f3744f9eb7c96bc4529b9",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-36e309b7"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/var/lib/hadoop-hdfs/jn"
          }, {
            "name" : "role_jceks_password",
            "value" : "1zpxhw1yyc8o2vd1zbbowxa8d"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-157f71cb7f8a60bed8d4fe4ac4ac27f2",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-38e309b9"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "jphans"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "jphans"
          }, {
            "name" : "namenode_id",
            "value" : "55"
          }, {
            "name" : "role_jceks_password",
            "value" : "cqvvy3ile5yrhse5rbk779q5u"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-b02a86b508f75d285227b83a2809b489",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-39e309b8"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "jphans"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "jphans"
          }, {
            "name" : "namenode_id",
            "value" : "68"
          }, {
            "name" : "role_jceks_password",
            "value" : "6cpu2pv7xls4xmmgq02r6idmt"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-38e309b9",
    "ipAddress" : "172.31.24.86",
    "hostname" : "ip-172-31-24-86.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-39e309b8",
    "ipAddress" : "172.31.24.87",
    "hostname" : "ip-172-31-24-87.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-36e309b7",
    "ipAddress" : "172.31.24.88",
    "hostname" : "ip-172-31-24-88.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-37e309b6",
    "ipAddress" : "172.31.24.89",
    "hostname" : "ip-172-31-24-89.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-34e309b5",
    "ipAddress" : "172.31.24.90",
    "hostname" : "ip-172-31-24-90.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-157f71cb7f8a60bed8d4fe4ac4ac27f2",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "c8d190d68e57e8406f462c5ec9c046219eb9dd8a64b2e1f6d4ea5bddb783c0c3",
    "pwSalt" : -4450753808468814079,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-157f71cb7f8a60bed8d4fe4ac4ac27f2",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "a9c4d3cb9d9543a37dc4041762ea50f306bbcfe763391369e96b0489eaaf7da6",
    "pwSalt" : 1686107076305835064,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-157f71cb7f8a60bed8d4fe4ac4ac27f2",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "64737be6281bb62b7a9279ccd50f4ad38b8211256d505506984364e40fbaab6a",
    "pwSalt" : -2652036489278845025,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-157f71cb7f8a60bed8d4fe4ac4ac27f2",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "236606a80a5aeecdf18304e828bd72bcac733dacfc63a6f6fafc97a3564494ff",
    "pwSalt" : -2597266299575721022,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "751510664adf53990c924921259cac5e8596fe16ef6ced3311a8f3cb47a50c0d",
    "pwSalt" : 8205257521086047926,
    "pwLogin" : true
  }, {
    "name" : "jayaprakashreddy",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "00f3ac8e0253288c3b3c42127ab6b8902b43b2bf659e4544523e72c0cd0b72cb",
    "pwSalt" : -356304374506519683,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "90694e0863d9d55deb447cfb155288c651a32540d8a0fed543d3dfe429aae712",
    "pwSalt" : 4369176588529871649,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.8.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20160916-1426",
    "gitHash" : "d23c620f3a3bbd85d8511d6ebba49beaaab14b75",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "229638144"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "268435456"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-24-90.ap-southeast-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "268435456"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "268435456"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-157f71cb7f8a60bed8d4fe4ac4ac27f2",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-38e309b9"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "3hct14m5557gyl1q2616tsg4k"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-157f71cb7f8a60bed8d4fe4ac4ac27f2",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-38e309b9"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "b4clea6rk8mei25gzu9tvsvd"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-157f71cb7f8a60bed8d4fe4ac4ac27f2",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-38e309b9"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "65bkzovprsq592a7g9sdtgn8h"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-157f71cb7f8a60bed8d4fe4ac4ac27f2",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-38e309b9"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "135vvgw9wauftpywx19eg6qw4"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-157f71cb7f8a60bed8d4fe4ac4ac27f2",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-38e309b9"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "6g4zu60l4cspbpsis86m4m3wm"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/22/2012 8:50"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}
```