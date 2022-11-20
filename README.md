# java-kafka-poc

- in a telecom company "Orange" we have a db with a table called "Customer" contains 1000,000 customer data 
    - name : String
    - phone : String
    - balance : float
- and we need to send a message (SMS) to all these customers with format "Hello [name] you got 2X of your balance . you current balance is 2*[balance]"


- Assumptions :
  - our database is mysql or postgres (choose your favourite ) 
  - Table structure 
      name :String
      phone:String
      balance:float
  - we will simulate the sms gateway by just write these massges to file(s)
  

Request:
 - Start your db locally
 - import 1M records (users.sql.zip) in project files
 - start your Kafka locally
 - buils a java program using Kafka to read the 1M users from db in batches and write it to "messages" topic
 - prepare a message for each user and write this message to kafka topic 
 - build a java consumer(s) to read these messages from "messages" topic and write them to file(s)
 
 
