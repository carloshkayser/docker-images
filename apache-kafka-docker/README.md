# Kafka

#### docker run kafka /etc/initKafka.sh

#### docker build --rm -f "Dockerfile" -t kayser/kafka .

#### docker-compose -f "docker-compose-kafka.yml" up


### CRIAR TOPICO
#### $ /usr/lib/kafka/bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic my-topic-kafka
#### $ /usr/lib/kafka/bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic myTopic

 /usr/lib/kafka/bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic trump

/usr/lib/kafka/bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic trump --from-beginning

### LISTAR TOPICO
#### $ /usr/lib/kafka/bin/kafka-topics.sh --list --bootstrap-server localhost:9092

### ENVIAR MENSAGEM
#### $ /usr/lib/kafka/bin/kafka-console-producer.sh --broker-list localhost:9092 --topic my-topic-kafka
#### $ /usr/lib/kafka/bin/kafka-console-producer.sh --broker-list kafka-broker-2:9093 --topic my-topic-kafka

### RECEBER MENSAGEM
#### $ /usr/lib/kafka/bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic my-topic-kafka --from-beginning
#### $ /usr/lib/kafka/bin/kafka-console-consumer.sh --bootstrap-server kafka-broker-1:9092 --topic my-topic-kafka --from-beginning

# Kafka Job

#### docker build --rm -f "Dockerfile-kafka-job" -t kayser/kafka-job .

#### docker run kayser/kafka-job