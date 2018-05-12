# Kafka

### install jdk
- download oracle jdk tar
- tar zxvf jdk.tar.gz
- `vi .bashrc`
  - `export JAVA_HOME=/../..`
  - `export PATH=$JAVA_HOME/bin:$PATH`


### start zookeeper server
- 


### start Kafka server



### test 
- test Producer
- test Consumer


### init action
- create 'test' topic: `./bin/kafka-topic.sh --zookeeper localhost:2181 --create --replication-factor 1 --partitions 1 --topic test`
- list topics: `./bin/kafka-topic.sh --zookeeper localhost:2181 --list`
- selcet data from topic
- delete topic



