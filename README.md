# kafkaconsumer

Prerequisite:

You should have Java (JDK) installed on your windows machine.

Apache Kafka official website: https://kafka.apache.org/downloads
 
Required Commands:

.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

.\bin\windows\kafka-server-start.bat .\config\server.properties

kafka-topics.bat --create --bootstrap-server localhost:9092 --replication-factor 1 --partition 1 --topic test


it is used to create push the message 

kafka-console-producer.bat --broker-list localhost:9092 --topic test
-------------------------------------------------------------------------------------------------------
Sample Data:

{"Name: "John", "Age":"31", "Gender":"Male"}
{"Name: "Emma", "Age":"27", "Gender":"Female"}
{"Name: "Ronald", "Age":"17", "Gender":"Male"}
---------------------------------------------------------------------------------------------------------
it is used to consume the messaages check which data is consumed :

kafka-console-consumer.bat --topic test --bootstrap-server localhost:9092 --from-beginning


used to stop the zookeepr server 
.\bin\windows\zookeeper-server-stop.bat .\config\zookeeper.properties

it is used to stop the kafka server 

.\bin\windows\kafka-server-stop.bat .\config\server.properties
