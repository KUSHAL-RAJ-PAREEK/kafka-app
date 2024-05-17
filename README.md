the apache kafka which is real-time distributed event streaming platform which is use in most of industries due to its great throughput.
so here is simple implementation with working demo.

JUST CLONE IT AND OPEN IN VS CODE:-
PRE:- 1. NEED DOCKER
      2. PULL ZOOKEEPPER IMAGE
      3. KEEP RUNNING IT IN ONE TERMINAL OR RUN IT IN BACKGROUND WITH -d IN DOCKER.
      4. IN VS CODE IN TERMINAL TYPE yarn init
      5.THEN ADD yarn add kafkajs
      6.NOW IN TERMINAL TYPE THIS LINES MAKE SURE DOCKER IS RUNING IN BACKGROUND
      
      ```
      docker run -p 9092:9092 \
      -e KAFKA_ZOOKEEPER_CONNECT=<PRIVATE_IP>:2181 \
      -e KAFKA_ADVERTISED_LISTENERS=PLAINTEXT://<PRIVATE_IP>:9092 \
      -e KAFKA_OFFSETS_TOPIC_REPLICATION_FACTOR=1 \
      confluentinc/cp-kafka
      ```

      7.NOW OPEN 3 TERMINAL AND WRITE EACH LINE RESPECTIVLY:-
      ```
       node producer.js
       node consumer.js user-1
       node consumer.js user-1
    ```

    YOU CAN ALSO TRY THIS TO UNDERSTAND KAFKA GROUPING IN 4 TERMINAL.
    ```
    node consumer.js group-2
    ```

THANK YOU.
