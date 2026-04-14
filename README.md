# Dockerized

A collection of Docker Compose configurations for running common development services locally.

## Required Tools

- **Docker** - Container platform
- **Docker Compose** - Multi-container orchestration

## Available Services

- **Portainer** - Docker container management platform
- **PostgreSQL** - Relational database
- **MySQL** - Relational database
- **phpMyAdmin** - Web-based MySQL administration tool
- **RabbitMQ** - Message broker
- **Redis** - In-memory data store and cache
- **Elasticsearch** - Distributed search and analytics engine
- **Logstash** - Data processing pipeline for ingesting and transforming logs
- **Kibana** - Visualization and management UI for Elasticsearch

## Example: Running PostgreSQL

Here's a complete example to run PostgreSQL:

```bash
# Navigate to postgres directory
cd postgres

# Setup environment
cp .env.example .env

# Edit .env with your values (optional, defaults work for development)
nano .env

# Start the service
docker compose up -d

# Check status
docker compose ps

# Stop when done
docker compose down
```

## Notes

- Each service runs in its own directory with isolated configuration
- Data persists in Docker volumes unless you run `docker compose down -v`
- Default ports are configured in the `.env` files
