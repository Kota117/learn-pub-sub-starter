# learn-pub-sub-starter (Peril)

This is the starter code used in Boot.dev's [Learn Pub/Sub](https://learn.boot.dev/learn-pub-sub) course.

# Helpful commands

## RabbitMQ

RabbitMQ uses Docker. Ensure Docker Desktop is open to start the Daemon before running any `docker` commands. Also, if a `docker` command fails, ensure Docker Desktop isn't showing the engine is in "Resource Saving Mode"; this can be seen in the bottom left of the UI. You want to see "Engine running".

### Start a RabbitMQ server with Docker in the background:

```bash
./rabbit.sh start
```

or, after the end of CH2,

```bash
docker run -d --name peril_rabbitmq -p 5672:5672 -p 15672:15672 -p 61613:61613 rabbitmq-stomp
```

### Stop the RabbitMQ server:

```bash
./rabbit.sh stop
```

### View the RabbitMQ management UI

Navigate to `http://localhost:15672` in a browser and login with username `guest` and password `guest`.

## Game server

### Start the game server:

From the root directory:
```bash
go run ./cmd/server
```

### Close the game server:

```bash
Ctrl + C
```
