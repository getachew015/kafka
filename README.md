# kafka
A docker image for kafka  and a zookeeper

# usage will be as below
to start in deamon process mode i.e. running in background, list running images and bring them down 

  --> docker-compose -f docker-compose.yml up -d
  
  --> docker-compose ps
  
  --> docker-compose down

# Topics, Producer, Consumer

**Create**
./bin/kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic dagim_demo_topic
**the below approach defaults to 1 partition and 1 replica**

./bin/kafka-topics.sh --create --topic temp_topic --bootstrap-server localhost:9092

list topics

./bin/kafka-topics.sh --list --zookeeper zookeeper:2181

show details about topics

./bin/kafka-topics.sh --describe --topic temp_topic --bootstrap-server localhost:9092

write messages/events in to topics

./bin/kafka-console-producer.sh --topic temp_topic --bootstrap-server localhost:9092

cosume a messages/events

./bin/kafka-console-consumer.sh --topic dagim_demo_topic --from-beginning --bootstrap-server localhost:9092

produce a messages/events

./bin/kafka-console-producer.sh --topic dagim_demo_topic --bootstrap-server localhost:9092

# visit the kafka documentation with the link below

https://kafka.apache.org/quickstart


