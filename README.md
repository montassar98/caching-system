# Docker Compose Setup for Caching System

This project includes a Docker Compose configuration for running a test environment with Kafka, Redis, Postgres, Kafdrop, and RedisInsight. Below are the instructions to run the system and access the respective tools.

## Prerequisites

Ensure you have Docker and Docker Compose installed on your machine.

## Running the Environment

### Test Environment

To run the test environment, use the following command:

```bash
docker-compose -f docker-compose.base.yml -f docker-compose.override.yml up -d
```

This will start the following services:

Kafka: For event streaming.
Redis: For caching.
Postgres: For database storage.
Kafdrop: A web UI to view Kafka topics and messages.
RedisInsight: A web UI to access Redis.
Production Environment
For the production environment, use the docker-compose.prod.yml file:

### Production Environment

For the production environment, use the docker-compose.prod.yml file:

```bash
docker-compose -f docker-compose.prod.yml up -d
```

### Accessing the Tools

Once the services are up and running, you can access the following web UIs:

1. **Kafdrop (Kafka UI)**

   - Access Kafdrop to view Kafka topics and messages at:
   - [http://localhost:9000](http://localhost:9000)

2. **RedisInsight (Redis UI)**
   - Access RedisInsight to view and manage Redis at:
   - [http://localhost:8001](http://localhost:8001)

## Stopping the Environment

To stop and remove the containers, run:

```bash
docker-compose -f docker-compose.base.yml -f docker-compose.override.yml down
```

This will stop and remove all the containers, networks, and volumes defined in your Docker Compose files.
