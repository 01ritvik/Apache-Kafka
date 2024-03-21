# Apache-Kafka

Environment Setup:
1.	Install Java:
a.	Check if Java is installed: Open Command Prompt and type java -version. If Java is installed, you'll see the version details. If not, you'll need to install it.
2.	Download Kafka:
a.	https://kafka.apache.org/downloads
b.	Navigate to Kafka using the given URL above and download the .tgz file.
3.	Extract Kafka to the C folder. 
 These steps will help you download the Apache Kafka into your system.
After all this done, we will have to setup and start Kafka server into the command prompt PowerShell.

Setting up Kafka into CMD:
1.	Set up Zookeeper:
a.	Open CMD PowerShell.
b.	Navigate to the Kafka directory.
c.	Use the following command to setup zookeeper.
d.	.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
e.	This will take a few seconds to start.
f.	After this step is done move on the next step.

2.	Set up Kafka Server:
a.	Open a new CMD PowerShell window.
b.	Navigate to the Kafka directory.
c.	Use the following command to setup Kafka server.
d.	.\bin\windows\kafka-server-start.bat .\config\server.properties
3.	Create Kafka topic:
a.	Open a new CMD PowerShell window.
b.	Navigate to the Kafka directory.
c.	Use the following command to create a topic.
d.	.\bin\windows\kafka-topics.bat --create --partitions 1 --replication-factor 1 --topic METCS777 --bootstrap-server localhost:9092
e.	METCS777 is the topic name, and we can use any name we want. 
f.	This step will create a Kafka Topic.
4.	Start Kafka Producer.
a.	Open a new CMD PowerShell window.
b.	Navigate to the Kafka directory.
c.	Use the following command to setup Kafka Producer.
d.	.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic METCS777
e.	Use the same topic name as used earlier.
5.	Start Kafka Consumer.
a.	Open a new CMD PowerShell window.
b.	Navigate to the Kafka directory.
c.	Use the following command to setup Kafka Consumer.
d.	.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic METCS777 --from-beginning
e.	Use the same topic name.
So, this will help you set up Kafka environment in your system.


How to run the code
Example 1:
This one is using Jupyter notebook, for this we have uploaded 2 .ipynb files. 1 for the producer side and the other for the consumer side.
Step to run this:
1. Setup the Apache Kafka with any topic name (For ex: METCS777)
2. First run the KafkaProducer(example1).ipynb then after running this file run the KafkaConsumer.ipynb file.
3. Then the output will be displayed on the CMD PowerShell Producer cell. 

Example 2:
This one is also using Jupyter notebook, for this we have uploaded 2 .ipynb files. 1 for the producer side and the other for the consumer side.
The working is the as in example 1 but this example uses a CSV file for the producer side.
Steps to run:
1.	Set up Kafka on CMD PowerShell.
2.	First run the KafkaProducer(example2).ipynb then after running this file run the KafkaConsumer.ipynb file.
3.	Then again the output will be on the same consumer CMD cell.


Result
•	Direct Interaction via CMD: Highlighted the basic functionality of Kafka through direct input into the Producer CMD, with messages being relayed to the Consumer side, showcasing real-time data streaming capabilities.
•	Integration with Jupyter Notebooks:
o	Example 2 & 3: Leveraged Jupyter notebooks to interact with Kafka, both for direct message streaming and for consuming messages from a CSV file. This demonstrates the flexibility of Kafka with different data sources and the potential for integration into data pipelines.
o	Visual Output: The process and outcomes were documented through screenshots, illustrating the setup, execution, and successful message passing within your Kafka environment.
Conclusion
o	Direct Interaction through CMD
o	Initiating my exploration of Apache Kafka, I embarked on a foundational exercise: direct message production and consumption via CMD. This initial foray provided not only a practical demonstration of Kafka's real-time messaging capabilities but also served as a foundational understanding of its operational mechanics.
o	Integration with Jupyter Notebooks: Initial Experiment
o	Progressing to a more sophisticated application, I integrated Kafka with Jupyter notebooks to leverage the dynamic execution environment for running Python scripts that interact with Kafka. This experiment highlighted the seamless interoperability between Kafka and Python, expanding the utility of Kafka into data processing and analytical endeavors. It was a demonstrative exercise in bridging data production with consumption in real-time, utilizing familiar analytical tools. 
o	Advanced Data Handling:UsingCSV Data
o	In a further exploration of Kafka's capabilities, I introduced a CSV file as a data source for the Kafka producer. This experiment was pivotal in showcasing Kafka's flexibility in handling various data formats and sources, reinforcing its adaptability in diverse data ingestion scenarios. 



