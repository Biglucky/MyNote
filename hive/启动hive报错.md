#### Cannot create directory /tmp/hive/root. Name node is in safe mode.
报错处理方式。命令行推出safe mode
```shell
hdfs dfsadmin -safemode leave
```
