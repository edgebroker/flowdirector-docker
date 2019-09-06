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

## Configuration Changes

The configuration file of Flow Director is `fdserver/data/config/backend.json`. It is created on
the first start and preserved. Changes require a restart of Flow Director.
