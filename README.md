# Docker-compose
This Repository is for all environments variables, If you know more add to this.
#KAFKA:

      KAFKA_ADVERTISED_LISTENERS: INSIDE://kafka:9093,OUTSIDE://localhost:9092
      
      KAFKA_LISTENER_SECURITY_PROTOCOL_MAP: INSIDE:PLAINTEXT,OUTSIDE:PLAINTEXT
      
      KAFKA_LISTENERS: INSIDE://0.0.0.0:9093,OUTSIDE://0.0.0.0:9092
      
      KAFKA_INTER_BROKER_LISTENER_NAME: INSIDE
      
      KAFKA_ZOOKEEPER_CONNECT: zookeeper:2181
      
      KAFKA_AUTO_CREATE_TOPICS_ENABLE: "false"
      
      KAFKA_DELETE_TOPIC_ENABLE: "true"
      
      KAFKA_LOG_DIRS: /var/lib/kafka/data
      
      KAFKA_LOG_RETENTION_HOURS: "168"
      
      KAFKA_LOG_SEGMENT_BYTES: "1073741824"
      
      KAFKA_NUM_PARTITIONS: "1"
      
      KAFKA_DEFAULT_REPLICATION_FACTOR: "1"
      
