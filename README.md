# kafka-java-test

Steps to install apache kafka on windows machine.

1. Download latest version of Apache Kafka Binary (zip file) from the link http://kafka.apache.org/downloads.html.
2. Extract the zip file kafka_2.11-1.0.0.tgz the into a folder. (assuming you have downloaded this version)
3. Open a command prompt or windows power shell and point to current directory.
4. Start the zookeeper server using following command.
    .\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
    
5. Open another command prompt window or windows power shell and point to extracted Kafka directory.
6. Start the kafka server using following command.
    .\bin\windows\kafka-server-start.bat .\config\server.properties
7. Open another command prompt window or windows power shell and point to extracted kafka directory.
8. Create a topic on which where messages can be produced and consumed. Run the following command to create the topic.
   .\bin\windows\kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test

Now ZooKeeper Server is started, Kafka server is started and Topic has been created.

Steps to run this Java Project.

1. Download the zip file of this Java Project from this repository.
2. Extract the zip file into a folder.
3. Open Eclipse, Go to File Menu, and select import maven project and provide the path of the folder.
4. Run TestKafkaProducr.java and TestKafkaConsumer.java as java application.
5. Type anything on console of TestKafkaProducer.java and press Enter. Same text will appear on console of TestKafkaConsumer.java.
