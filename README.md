# Flow Director Docker Compose Templates

This repository contains docker compose templates to start/stop 

- Flow Director with SwiftMQ
- Flow Director standalone

Please clone this repository and open a shell within the root directory `Flow Director-docker`.

## Flow Director with SwiftMQ

Use

    ./fd-swiftmq start
  
to start Flow Director and a single SwiftMQ Router. Both are started as demon. Flow Director listens
on port `8080`, SwiftMQ on port `4001`.

Use

    ./fd-swiftmq stop
    
to stop both.

Use 

    ./fd-swiftmq status
    
to see the status of the docker containers.

## Flow Director Standalone

This mode is used to connect Flow Director to an existing SwiftMQ Router.

Use

    ./fd-standalone start
  
to start Flow Director standalone. It is started as demon. Flow Director listens
on port `8080`.

Use

    ./fd-standalone stop
    
to stop both.

Use 

    ./fd-standalone status
    
to see the status of the docker containers.

Flow Director saves its configuration file `fdserver/data/config/backend.json` on the first start. Stop
it and change the configuration. Specify the hostname, port and credentials of your SwiftMQ Router. 
In case it runs on the same machine as Flow Director, use `dockerhost` as hostname. Then start Flow Director
again. It should now be connected to your SwiftMQ Router.

## Configuration Changes

The configuration file of Flow Director is `fdserver/data/config/backend.json`. It is created on
the first start and preserved. Changes require a restart of Flow Director.
