# Flume_Spooldir_Kafka_Kerberos
Agent Flume Source SpoolDir to Kafka Sink

$ flume-ng agent -n agent-from -f agent-from.properties -Djava.security.auth.login.config=/etc/conf/kafka/jaas.conf -c conf

jaas.conf:

KafkaClient {<br>
com.sun.security.auth.module.Krb5LoginModule required<br>
useKeyTab=true<br>
keyTab="/etc/conf/kafka/kafka.keytab"<br>
principal="kafka/brxptolnxslp005.xpto.sl@HADOOP.PRD.XPTO";<br>
};<br>
