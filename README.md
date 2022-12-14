# Kafka_Dataset_Generator

A python client that will produce hardware data such as clock, temperature, Load and Power of the CPU and GPU into a kafka topic.
  
The client consumes the data from kafka and generates a csv file. It also adds a target column called 'No Technical Intervention Required' in the generated dataset which can be used for a machine learning purpose.


##  Prerequisites:

   OpenHardwareMonitor software must be running before launching the *batchProducerConsumerKafka.bat* batch file.
   https://openhardwaremonitor.org/

   A subscription for a kafka topic in confluent cloud is necessary as well. 
   https://www.confluent.io/confluent-cloud/

   The following environmental variables in the .env file corresponding to the cluster and topic subscription must be specified:

   BOOTSTRAP.SERVERS
   
   KAFKA_CLUSTER_KEY
   
   KAFKA_CLUSTER_SECRET
   
   TOPIC_NAME


  The following batch can take up to 10 minutes to complete.

  In the command line:

  1. Go to the *kafka_python_client_dataset_generator* project folder:
          
          >cd C:\Users\...\kafka_python_client_dataset_generator
  
  2. Activate your virtual environment:
  
          C:\Users\...\kafka_python_client_dataset_generator>conda activate venv
         
  3. Install requirements:
  
          C:\Users\...\kafka_python_client_dataset_generator>pip install -r requirements.txt
  
  4. Run the *batchProducerConsumerKafka.bat* batch file as shown following:
    
          C:\Users\...\kafka_python_client_dataset_generator>batchProducerConsumerKafka.bat
  
  5. When the csv file is generated, press CTRL+C to stop the consumer. Then, press 'Y' to terminate the batch.
