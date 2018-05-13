# Kafka

### install jdk
- download oracle jdk tar
- tar zxvf jdk.tar.gz
- `vi .bashrc`
  - `export JAVA_HOME=/../..`
  - `export PATH=$JAVA_HOME/bin:$PATH`

### let 9092 port open 
- `sudo ufw allow in 9092`




### start zookeeper server
- 


### start Kafka server
- vi server-config
  - `advertised.listeners=PLAINTEXT://X.X.X.X:9092`
- start zookeeper-server
- start kafka server
-


### test 
- test Producer
- test Consumer


### init action
- create 'test' topic: `./bin/kafka-topic.sh --zookeeper localhost:2181 --create --replication-factor 1 --partitions 1 --topic test`
- list topics: `./bin/kafka-topic.sh --zookeeper localhost:2181 --list`
- selcet data from topic: 
- delete topic


### tmp notes
http://windrocblog.sinaapp.com/?p=1860

