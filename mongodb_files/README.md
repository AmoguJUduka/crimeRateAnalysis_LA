MongoDB Installation Guide
Prerequisites
Before installing MongoDB, ensure that:

Apache Spark is installed on your machine

For Spark installation guidance, follow this tutorial: YouTube: Apache Spark Installation Guide


Docker is installed on your machine
You have administrative privileges on your system

Installation Steps
1. Run MongoDB in Docker
Before installing MongoDB Compass, run the MongoDB server using Docker:
docker run --rm -it -p 27018:27017 --name dockerMongo -v "c:/volDocker/mongodb/data/db:/data/db" mongo:latest
This command:

Runs the latest MongoDB image
Maps port 27017 in the container to port 27018 on your host
Names the container "dockerMongo"
Mounts a volume from your local machine to persist data
Will remove the container when stopped (--rm flag)

Make sure to create the directory c:/volDocker/mongodb/data/db before running this command.
2. Download MongoDB and MongoDB Compass
Download MongoDB Community Server and MongoDB Compass from the official website:

Visit MongoDB Download Center
Select your operating system
Choose the MongoDB Community Server edition
Download the installer package
Download MongoDB Compass (version mongodb-compass-1.36.2-beta.1-win32-x64)

2. Install MongoDB
For Windows:

Run the downloaded installer (.msi file)
Follow the installation wizard
Select "Complete" installation type
Choose "Install MongoDB as a Service" for automatic startup
Complete the installation


Locate the MongoDB connector JAR files:

mongo-java-driver-3.10.2.jar
mongo-spark-connector_2.11-2.4.1.jar


Copy these files to your Spark's jars directory:
cp /path/to/mongo-java-driver-3.10.2.jar /path/to/spark/jars/
cp /path/to/mongo-spark-connector_2.11-2.4.1.jar /path/to/spark/jars/
Replace /path/to/ with the actual paths on your system.

5. Install and Configure MongoDB Compass
MongoDB Compass is the official GUI for MongoDB:

Install MongoDB Compass:

Run the MongoDB Compass installer (mongodb-compass-1.36.2-beta.1-win32-x64.exe)
Follow the installation wizard instructions
Complete the installation


