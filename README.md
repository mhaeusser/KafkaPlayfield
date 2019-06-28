# KafkaPlayground

See https://kafka.apache.org/quickstart

First, install [ZooKeeper](https://zookeeper.apache.org/).

~~~
bin\windows\zookeeper-server-start.bat config/zookeeper.properties

bin\windows\kafka-server-start.bat config/server.properties

bin\windows\kafka-topics.bat --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic test

bin\windows\kafka-topics.bat --list --bootstrap-server localhost:9092

bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic test
(type messages)

bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic test --from-beginning
~~~

copy and adapt config files as described [here](https://kafka.apache.org/quickstart) or unpack config.7z

~~~
bin\windows\kafka-topics.bat --create --bootstrap-server localhost:9092 --replication-factor 3 --partitions 1 --topic my-replicated-topic

bin\windows\kafka-topics.bat --describe --bootstrap-server localhost:9092 --topic my-replicated-topic
~~~


