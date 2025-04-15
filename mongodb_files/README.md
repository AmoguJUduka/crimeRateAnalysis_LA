# MongoDB Installation Guide

## Prerequisites

Before installing MongoDB, ensure that the following are installed on your machine:

- **Apache Spark**  
  For Spark installation guidance, follow this tutorial:  
  📺 [YouTube: Apache Spark Installation Guide](#)

- **Docker**

- You have **administrative privileges** on your system

---

## Installation Steps

### 1. Run MongoDB in Docker

Before installing MongoDB Compass, start the MongoDB server using Docker:

```bash
docker run --rm -it -p 27018:27017 --name dockerMongo -v "c:/volDocker/mongodb/data/db:/data/db" mongo:latest
```

This command:
- Runs the latest MongoDB image
- Maps port `27017` in the container to port `27018` on your host
- Names the container **dockerMongo**
- Mounts a volume from your local machine to persist data
- Removes the container when stopped (`--rm` flag)

> **Important:** Make sure to create the directory `c:/volDocker/mongodb/data/db` before running the command.

---

### 2. Download MongoDB and MongoDB Compass

Download both from the [MongoDB Download Center](https://www.mongodb.com/try/download/community):

- Select your operating system
- Choose **MongoDB Community Server**
- Download the installer package

Also download **MongoDB Compass**:  
📦 Version: `mongodb-compass-1.36.2-beta.1-win32-x64`

---

### 3. Install MongoDB (Windows)

1. Run the downloaded installer (`.msi` file)
2. Follow the installation wizard
3. Select **Complete** installation type
4. Choose **Install MongoDB as a Service** for automatic startup
5. Complete the installation

---

### 4. Add MongoDB Connector JAR Files to Spark

Locate and copy the following JAR files:

- `mongo-java-driver-3.10.2.jar`
- `mongo-spark-connector_2.11-2.4.1.jar`

Copy them into Spark's `jars` directory:

```bash
cp /path/to/mongo-java-driver-3.10.2.jar /path/to/spark/jars/
cp /path/to/mongo-spark-connector_2.11-2.4.1.jar /path/to/spark/jars/
```

> 🔁 Replace `/path/to/` with the actual file paths on your system.

---

### 5. Install and Configure MongoDB Compass

MongoDB Compass is the official GUI for MongoDB.

- Run the MongoDB Compass installer (`mongodb-compass-1.36.2-beta.1-win32-x64.exe`)
- Follow the installation wizard
- Complete the setup
