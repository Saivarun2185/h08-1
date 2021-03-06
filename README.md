# H07 - Getting Started with Apache Kafka

Santhosh Bonala
Northwest Missouri State University
44-517 Big Data

## Overview

Short introduction to the Kafka distributed streaming platform

We will:

1. Start ZooKeeper (clientPort=2181)
2. Start Kafka (connects to Zookeeper)
3. Create a topic ("bearcat_messages")
4. List topics (to verify)
5. Run a producer. Send messages on our topic.
6. Run a consumer. Get messages on our topic.

## Getting Started

- Fork this repo to your Bitbucket.
- Clone your Bitbucket repo down to your local computer.

## Working in Windows vs Bash

This repo is set with helper batch files that work in Windows. Windows uses a backslash in file paths and accesses .bat Windows Command Line batch files found in the kafka bin/windows folder.

Bash uses a forward slash and must access the .sh shell scripts found in the kafka bin folder.

## Understand the Contents

These helper files are for convenience only - modify them and make them your own. You must understand the contents of the files and how they work.

## Start ZooKeeper on port 2181

In Windows File Explorer:

- Navigate to your h07 folder.
- Right-click on your repo folder and "Open Command Window Here as Administrator".
- Run the batch file to start the Zookeeper service. Keep this window open to keep the service running.

```dos
01start_zookeeper
```

## Start Kafka

Open another Command Window as Admin and start Kafka. Keep this window open to keep Kafka running.

```dos
02start_kafka
```

Kafka will start and connect to ZooKeeper

## Create topic (bearcat_messages)

Open another Command Window as Admin and create a topic.

```dos
03create_topic
```

This will create a new topic named bearcat_messages.

List topics to see all topics (including your new bearcat_messages).

```dos
04list_topics
```

## Create producer (on port 9092)

Open another Command Window as Admin and run a message producer.

```dos
producer
```
producer will automatically post the twitter feed into kafka system


## Create consumer (listening on port 9092)

Open another Command Window as Admin and run a message consumer.

```dos
consumer
```

Arrange your producer and consumer command windows beside each other to watch the results.

## Resources and References

Apache Kafka https://kafka.apache.org/

How to add "Open Command Window Here as Administrator" to context menu:
https://www.sevenforums.com/tutorials/47415-open-command-window-here-administrator.html

Verify Mrakdown with http://dillinger.io/