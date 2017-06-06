Hadoop Map Reduce
Create a Directory
hdfs dfs -mkdir /bigdata
List diretory
hadoop fs -ls /
Download a file csv
wget -c http://compras.dados.gov.br/contratos/v1/contratos.csv
Copy file to the HDFS directory created above
hadoop fs -copyFromLocal contratos.csv /bigdata
Read file
hadoop fs -cat /bigdata/contratos.csv
Test word count with mapreduce
hadoop jar /opt/hadoop/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.8.0.jar wordcount /bigdata/contratos.csv /output
Read result
hdfs dfs -cat /output/*