# r/dataengineering

## tools to learn

Intentionally keeping the list short... Here's my 5 tools:

1. Learn the basics: bash, python, SQL (#1 skills on Dice report)
1. Docker & Kubernetes (fast growing on Dice report, GREAT for Cloud agnostics skills)
1. Apache Spark (GCP Dataproc, Azure Databricks, AWS EMR)
1. Apache Kafka (GCP Pub/Sub, Azure Event Hub, AWS Kinesis)
1. Apache Airflow (GCP Cloud Composer, AWS/Azure managed service backed by Astronomer)

LEARN THESE SKILLS ON THE CLOUD.

It's completely daunting the amount of different opinions you get for this question :D
It's mainly because data engineers know a little about a lot of things and they are very opinionated :)

With that said, here was my (humble) opinion. I've been a data engineer for over 20yrs, founding member of a few big companies you might know, and an apache software foundation contributor... The tools I give you bellow are back by a Dice report of analyzing over 6 million jobs...

I will guarantee you these 5 will land you a great DE job.

## consulting work

YES... Specially if you wanna quickly become a level-II or level-II data engineer/solution architect quickly!

Here's why you want to start as consultant:

1. Data Engineers need to know a little about a lot of things. Jack of all trade, master of none; specially senior DEs. Consulting gives you that, a lot of projects, a lot of exposure, a lot of problems to solve.

1. Consulting companies (mid-tier) are always hiring and there's a lot of room for growth

BUT do NOT work for the big guys, their quality is s**t (please no offense) and they tend to put you on loner staff aug kind of projects.

# real-time tools

Here's some topics/tools to consider or research ;)

High water marketing: good for DB tables with last_modified timestamp column

CDC - Change Data Capture: good for DB tables without last_modified ts

Apache Kafka: good for streaming sources

Apache Airflow: good for a bunch of things but also making file triggers

It really depends on your source and how easy it is for you to identify "new" records; but these are some essential techniques and tools.

High water marketing is good for databases tables that provide a reliable last_modified timestamp field on every row. You can store your last process timestamp and query rows for anything greater. This is probably the most efficient DB solution.

There are a number of CDC tools for database tables that do NOT have a reliable last_modified column. They tend to be very expensive and complex to implement.

Kafka is a great open source real-time middleware. You have the concept of publishers and consumers. Publishers post records to a topic (a highly scalable queue) and multiple consumers can read records exactly from where they left off. Kafka keeps track of what every consumer has seen. I use this religiously in my data pipelines. All Cloud vendors have their own name for this service: GCP Cloud Pu/Sub, Azure Event Hub, AWS Kinesis.

For file sources, I recommend a tool like Airflow. Airflow is a pull fledged python orchestration tool good for just about everything! It also provides file triggers so it will automatically kick off your process when new files appear in a directory.
