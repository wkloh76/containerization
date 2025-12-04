# n8n with Sqlite

Starts n8n with default sqlite as database.

## Start

To start n8n with sqlite simply start docker-compose by executing the following
command in the current folder.

```
docker-compose up -d
```

To stop it execute:

```
docker-compose stop
```

## Configuration

```
# Data will keep into docker volume. The data will keep forever unless the volume corruption.
# This method will predict data lost during docker images upgrading and container recreating.
# Mean that all will work find
volumes:
  n8n_storage:

services:
  n8n:
    image: docker.n8n.io/n8nio/n8n
    restart: always
    environment:
      - N8N_HOST=localhost
      - N8N_PORT=5678
      - N8N_PROTOCOL=http
      - NODE_ENV=production
    ports:
      - 5678:5678
    volumes:
      - n8n_storage:/home/node/.n8n
      - ./public:/public  # The host folder mount to container /public folder.
```

## Upgrade n8n procedure

1. Backup database to avoid database corruption

   - Run `Docker ps -a` to find n8n container name or id.

   - Run `docker cp <container name/id>:<source file with path> < host target folder>`. My example: `docker cp withsqlite-n8n-1:/home/node/.n8n/database.sqlite ./bak`. After that the file will save into the host folder

2. Destroy and remove n8n container.

   - Run `docker compose down`.

3. Upgrade n8n images

   - Run `docker pull docker.n8n.io/n8nio/n8n:latest`. It will pull the latest images to local machine.

4. Create new n8n container

   - Run `docker compose up -d`.

5. Restore database and restart container

   - Run `docker compose up -d`.
   - Run `docker cp ./bak/database.sqlite withsqlite-n8n-1:/home/node/.n8n/database.sqlite`.
   - Run `docker compose restart`.

6. Reset admin password if for get
   - Run `docker exec -it withsqlite-n8n-1 n8n user-management:reset`
   - Run `docker compose restart`.
