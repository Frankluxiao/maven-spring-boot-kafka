Setup
1. zookeeper-server-start /usr/local/etc/kafka/zookeeper.properties
2. kafka-server-start /usr/local/etc/kafka/server.properties
3. kafka-topics --bootstrap-server localhost:9092 --topic maven-spring-boot-kafka --create --partitions 1 --replication-factor 1

Test 1 : Command Line
1. kafka-console-consumer --bootstrap-server localhost:9092 --topic maven-spring-boot-kafka --from-beginning
2. kafka-console-producer --broker-list localhost:9 --topic maven-spring-boot-kafka

Test 2 : Postman
1. POST: URL http://localhost:8080/send with the body {“key1”: “value1”}:
2. GET: URL http://localhost:8080/receive 