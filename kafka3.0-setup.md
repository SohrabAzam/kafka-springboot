# Setup Kafka
## Setup Zookeeper
```
zookeeper-server-start.bat ..\..\config\zookeeper.properties
```
**Runs on port 2181**



## Setup Kafka Broker
- In server.properties
```
listeners=PLAINTEXT://localhost:9092
auto.create.topics.enable=false
```
```
kafka-server-start.bat ..\..\config\server.properties
```

## Create a topic
```
kafka-topics.bat --create --topic test-topic  --replication-factor 1 --partitions 4 --bootstrap-server localhost:2181
```
