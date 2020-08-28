FROM openjdk:8-jdk

WORKDIR /usr/lib/

# Download Kafka
RUN apt-get -y update && \
    apt-get -y install nano && \
    apt-get install -y wget && \
    wget http://ftp.unicamp.br/pub/apache/kafka/2.3.0/kafka_2.12-2.3.0.tgz && \
    tar -xzf kafka_2.12-2.3.0.tgz && \
    mkdir kafka && \
    mv kafka_2.12-2.3.0/* kafka && \
    rm -r kafka_2.12-2.3.0 && \
    rm kafka_2.12-2.3.0.tgz

COPY server_properties/* /usr/lib/kafka/config/

EXPOSE 9092

WORKDIR /etc

# ENTRYPOINT ["/usr/lib/kafka/bin/kafka-server-start.sh", "/usr/lib/kafka/config/server.properties"]