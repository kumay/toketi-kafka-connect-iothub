# Kafka Connect Azure IoT Hub (fixed version)

This is forked project from https://github.com/Azure/toketi-kafka-connect-iothub.


### Reason for the fork

I had a need to use Azure IoTHub with Kafka (Confluent version) and faced some difficulty using original **toketi-kafka-connect-iothub** connector.

The original repo is archived and no activity observed so I created a fork.
I updated the versions of related packages, fixes related to sbt version update and some package name change in codes.
No functionality or performance improvement is implemented.
All the credit gose to original creater of this plugins. 

(I may have some credit making this connector buildable again)


### how to build

```
$ sbt assembly
```

this commend will create fat jar under "target" directry.

### how to use

Intended for use with confluent connect cluster.

Please see confluent documentation.

**How to prepare connector .jar file**

https://docs.confluent.io/platform/current/connect/devguide.html#packaging

**How to install prepared connector .jar file to connect**

https://docs.confluent.io/home/connect/self-managed/userguide.html#installing-kconnect-plugins


#### prerequisite

1. install scala 2.1X (will not work with scala 3)
2. install sbt


#### tested environment

Windows 10,  WSL2 with ubuntu 18.04.


## Orignal Readme text about this connector
________________________

Kafka Connect Azure IoT Hub consists of 2 connectors - a source connector and a sink connector. The source connector
is used to pump data from [Azure IoT Hub](https://azure.microsoft.com/en-us/services/iot-hub/) to
[Apache Kafka](https://kafka.apache.org/), whereas the sink connector reads messages from Kafka and sends them to IoT
 devices via [Azure IoT Hub](https://azure.microsoft.com/en-us/services/iot-hub/). When used in tandem, the 2
 connectors allow communicating with IoT devices by simply posting and reading messages to/from Kafka topics. This
 should
 make it easier for open source systems and other systems that already interface with Kafka to communicate with
 Azure IoT devices.

For more information on the capabilities of the connectors and how to use them, please refer to the links below -

### [Source Connector](README_Source.md)

### [Sink Connector](README_Sink.md)


## Contribute Code

If you want to contribute, we ask you to sign a [CLA](https://cla.microsoft.com/)(Contribution License Agreement). A
friendly bot will remind you about it when you submit a pull-request.

If you are sending a pull request, we kindly request to check the code style with IntelliJ IDEA, importing the settings
from `Codestyle.IntelliJ.xml`.


