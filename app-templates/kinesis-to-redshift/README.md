
## Description

The Kinesis to Redshift application template demonstrates continuous big data sync from a source to destination while reading data messages from a configured Kinesis stream. This could be easily utilized and extended by any developer to create a fast,  fault tolerant and scalable Big Data Sync or Retention Application to serve business with continuous data.

 It ingests records separated by delimiter '|' from configured AWS kinesis streams and writes each message as a record in AWS Redshift data warehouse. This application uses PoJoEvent as an example schema, which can be customized to use custom schema based on business requirements.

- The application scales linearly with number of Kinesis shards.
- The application is fault tolerant and can withstand node and cluster outages without data loss.
- The application is also highly performance and can perform as fast as the network bandwidth allows.
- The only configuration user needs to provide is source Kinesis credentials, stream name and destination redshift database table, bucket name, path and credentials.
- This enterprise grade application template will dramatically reduce your time to market and cost of operations.

Import the application from DataTorrent AppFactory and launch it to ingest records separated by '|' from configured AWS Kinesis Stream and writes each message as a record in AWS Redshift data warehouse. Please follow the walkthrough document below to understand the configurable properties. Moreover, one could easily add customized business logic to further process the data during sync.

## Implementation details
- Logical flow diagram
![Logical Plan](https://www.datatorrent.com/wp-content/uploads/2017/08/kinesis-to-redshift-dag.png)

- It uses following operators
  - KinesisByteArrayInputOperator Input operator (Read from AWS Kinesis)
  - RedshiftOutputModule Output Operator (Write to AWS Redshift)
- Supported data source
    - AWS Kinesis version 1.10.x
    - Tested with AWS Kinesis driver: com.amazonaws:aws-java-sdk-kinesis:jar:1.10.73
- Supported sinks
    - AWS Redshift JDBC version 1.2.1.x
    - Tested with AWS Redshift JDBC driver: com.amazon.redshift:redshift-jdbc4:jar:1.2.1.1001

## Supported visualizations
|Metric|Widget|
|------|-------|
|Bytes read per second from Kinesis |Line Chart|
|Bytes written per second to Redshift |Line Chart|
|Events read per second from Kinesis |Line Chart|
|Events written per second to Redshift |Line Chart|
|Total events read from Kinesis |Single Value|
|Total events written to Redshift |Single Value|
|Total bytes read from Kinesis |Single Value|
|Total bytes written to Redshift |Single Value|

## Resources

- Detailed documentation for this application template is available at:

    [http://docs.datatorrent.com/app-templates/0.10.0/kinesis-to-redshift](http://docs.datatorrent.com/app-templates/0.10.0/kinesis-to-redshift)
- Source code for this app-template is available at:

   [https://github.com/DataTorrent/moodI/tree/master/app-templates/kinesis-to-redshift](https://github.com/DataTorrent/moodI/tree/master/app-templates/kinesis-to-redshift)

- Please send feedback or feature requests to:
 <a href="mailto:feedback@datatorrent.com"  class="feedback" id="feedback" ga-track="feedback">feedback@datatorrent.com</a>

- Join our user discussion group at:
  <a href="mailto:dt-users@googlegroups.com"  class="maillist" id="maillist" ga-track="maillist">dt-users@googlegroups.com</a>
