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


      #Zookeeper:

      ZOO_MY_ID:

Description: Unique identifier for the Zookeeper server in the ensemble.
Example: ZOO_MY_ID: 1
ZOO_SERVERS:

Description: Defines the list of Zookeeper servers in the ensemble. Each entry has the format server.ID=host:port1:port2.
Example: ZOO_SERVERS: server.1=zookeeper1:2888:3888 server.2=zookeeper2:2888:3888
ZOO_TICK_TIME:

Description: The basic time unit in milliseconds used by Zookeeper for heartbeats and timeouts.
Example: ZOO_TICK_TIME: 2000
ZOO_INIT_LIMIT:

Description: The amount of time, in ticks, to allow followers to connect and sync with a leader.
Example: ZOO_INIT_LIMIT: 5
ZOO_SYNC_LIMIT:

Description: The maximum number of ticks that a follower is allowed to be out of sync with the leader.
Example: ZOO_SYNC_LIMIT: 2
ZOO_AUTOPURGE_PURGEINTERVAL:

Description: The time interval in hours for which the purge task has to be triggered.
Example: ZOO_AUTOPURGE_PURGEINTERVAL: 0
ZOO_AUTOPURGE_SNAPRETAINCOUNT:

Description: Number of snapshots to retain after autopurge.
Example: ZOO_AUTOPURGE_SNAPRETAINCOUNT: 3
ZOO_STANDALONE_ENABLED:

Description: Specifies whether the Zookeeper instance should run in standalone mode.
Example: ZOO_STANDALONE_ENABLED: true
ZOO_4LW_COMMANDS_WHITELIST:

Description: Comma-separated list of commands that are allowed by 4-letter word commands.
Example: ZOO_4LW_COMMANDS_WHITELIST: srvr, mntr
ZOO_LOG4J_PROP:

Description: Configuration for log4j properties, allowing customization of Zookeeper logging.
Example: ZOO_LOG4J_PROP: INFO,ROLLINGFILE
