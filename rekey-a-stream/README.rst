How to rekey a stream with a value
==================================

How can I add a key or change the key to a Kafka topic?

Example use case
----------------
Suppose you have an unkeyed stream of movie ratings from movie-goers. Because the stream is not keyed, ratings for the same movie aren't guaranteed to be placed into the same partition.
In this tutorial, we'll write a program that creates a new topic keyed by the movie's name. When the key is consistent, it becomes possible to process these ratings at scale and in
parallel.

- ``docker-compose up -d``: This launches the Confluent Platform

- ``docker exec -it ksqldb-cli ksql http://ksqldb-server:8088``: To begin developing interactively using the kSQLDB CLI

- ``docker exec ksqldb-cli ksql-test-runner -i /opt/app/test/input.json -s /opt/app/src/statements.sql -o /opt/app/test/output.json``: Invoke the tests

- `Test commands as shown in this tutorial: <https://kafka-tutorials.confluent.io/rekey-a-stream/ksql.html?_ga=2.255036111.658914180.1605291890-1093453177.1605291890>`

