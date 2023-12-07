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



# Zookeeper:

      ZOO_MY_ID: 1

      ZOO_SERVERS: server.1=zookeeper1:2888:3888 server.2=zookeeper2:2888:3888
      
      ZOO_TICK_TIME: 2000
      
      ZOO_INIT_LIMIT: 5
      
      ZOO_SYNC_LIMIT: 2
      
      ZOO_AUTOPURGE_PURGEINTERVAL: 0
      
      ZOO_AUTOPURGE_SNAPRETAINCOUNT: 3
      
      ZOO_STANDALONE_ENABLED: true
      
      ZOO_4LW_COMMANDS_WHITELIST: srvr, mntr
      
      ZOO_LOG4J_PROP: INFO,ROLLINGFILE

# Mysql:

      MYSQL_ROOT_PASSWORD: example_root_password

      MYSQL_DATABASE: example_database
      
      MYSQL_USER: example_user
      
      MYSQL_PASSWORD: example_user_password
      
      MYSQL_ALLOW_EMPTY_PASSWORD: "no"
      
      MYSQL_RANDOM_ROOT_PASSWORD: "no"
      
      MYSQL_LOG_CONSOLE: "true"
      
      MYSQL_LOG_QUERIES: "true"
      
      MYSQL_MAX_CONNECTIONS: 100
      
      MYSQL_MAX_ALLOWED_PACKET: 128M
      
      MYSQL_KEY_BUFFER_SIZE: 256M
      
      MYSQL_INNODB_BUFFER_POOL_SIZE: 512M
      
      MYSQL_INNODB_LOG_FILE_SIZE: 256M
      
      MYSQL_INNODB_LOG_BUFFER_SIZE: 64M
      
      MYSQL_INNODB_FLUSH_LOG_AT_TRX_COMMIT: 1

# Debezium

      GROUP_ID: 1
      
      CONFIG_STORAGE_TOPIC: my-connect-configs
      
      OFFSET_STORAGE_TOPIC: my-connect-offsets
      
      STATUS_STORAGE_TOPIC: my-connect-status
      
      BOOTSTRAP_SERVERS: kafka:9092
      
      KEY_CONVERTER: org.apache.kafka.connect.json.JsonConverter
      
      VALUE_CONVERTER: org.apache.kafka.connect.json.JsonConverter
      
      INTERNAL_KEY_CONVERTER: "org.apache.kafka.connect.json.JsonConverter"
      
      INTERNAL_VALUE_CONVERTER: "org.apache.kafka.connect.json.JsonConverter"
      
      CONNECT_KEY_CONVERTER_SCHEMA_REGISTRY_URL: "http://schema-registry:8081"
      
      CONNECT_VALUE_CONVERTER_SCHEMA_REGISTRY_URL: "http://schema-registry:8081"
      
      CONNECT_REST_ADVERTISED_HOST_NAME: debezium
      
      CONNECT_PLUGIN_PATH: /usr/share/java/debezium-connector-mysql
      
      TZ: "UTC"
      
      MYSQL_HOSTNAME: mysql
      
      MYSQL_PORT: "3306"
      
      MYSQL_USER: example_user
      
      MYSQL_PASSWORD: example_user_password
      
      MYSQL_DATABASE: example_database
      

# Airflow

      AIRFLOW_DATABASE_NAME: airflow
      
      AIRFLOW_DATABASE_USERNAME: airflow
      
      AIRFLOW_DATABASE_PASSWORD: airflow
      
      AIRFLOW_EXECUTOR: CeleryExecutor
      
      AIRFLOW__CORE__SQL_ALCHEMY_CONN: postgresql+psycopg2://airflow:airflow@postgres:5432/airflow
      
      AIRFLOW__CORE__FERNET_KEY: your_fernet_key
      
      AIRFLOW__WEBSERVER__SECRET_KEY: your_secret_key


# Airflow _ scheduler

      AIRFLOW_DATABASE_NAME: airflow
      
      AIRFLOW_DATABASE_USERNAME: airflow
      
      AIRFLOW_DATABASE_PASSWORD: airflow
      
      AIRFLOW_EXECUTOR: CeleryExecutor
      
      AIRFLOW__CORE__SQL_ALCHEMY_CONN: postgresql+psycopg2://airflow:airflow@postgres:5432/airflow
      
      AIRFLOW__CORE__FERNET_KEY: your_fernet_key

# Airflow - worker

      AIRFLOW_DATABASE_NAME: airflow
      
      AIRFLOW_DATABASE_USERNAME: airflow
      
      AIRFLOW_DATABASE_PASSWORD: airflow
      
      AIRFLOW_EXECUTOR: CeleryExecutor
      
      AIRFLOW__CORE__SQL_ALCHEMY_CONN: postgresql+psycopg2://airflow:airflow@postgres:5432/airflow
      
      AIRFLOW__CORE__FERNET_KEY: your_fernet_key

# Postgres:
      POSTGRES_USER: airflow
      
      POSTGRES_PASSWORD: airflow
      
      POSTGRES_DB: airflow
      
