#### Kafka常用命令

1.启用kafka
```shell
bin/kafka-server-start.sh -daemon config/server.properties
```

2.停止kafka
```shell
bin/kafka-server-stop.sh
```

3.消费者
```shell
bin/kafka-console-consumer.sh --bootstrap-server server11:9092 --topic first
```

4.生产者
```shell
bin/kafka-console-producer.sh --bootstrap-server server11:9092 --topic first
```

5.列出所以topic
```shell
bin/kafka-topics.sh --bootstrap-server server13:9092 --list
```

6.创建topic
```shell
bin/kafka-topics.sh --bootstrap-server server11:9092 --create --topic china --partitions 2 --replication-factor 2
```

7.查看topic详情
```shell
bin/kafka-topics.sh --bootstrap-server server11:9092 --describe --topic first
```

8.更新topic分区数
```shell
bin/kafka-topics.sh --bootstrap-server server11:9092 --alter --topic first --partitions 7
```
