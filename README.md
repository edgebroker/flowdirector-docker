# Flowdirector Docker Compose Templates

This repository contains docker compose templates to start/stop 

- Flowdirector with SwiftMQ
- Flowdirector standalone

Please clone this repository and open a shell within the root directory `flowdirector-docker`.

## Flowdirector with SwiftMQ

Use

    ./fd-swiftmq start
  
to start Flowdirector and a single SwiftMQ Router. Both are started as demon. Flowdirector listens
on port `8080`, SwiftMQ on port `4001`.

Use

    ./fd-swiftmq stop
    
to stop both.

Use 

    ./fd-swiftmq status
    
to see the status of the docker containers.

## Flowdirector Standalone

Use

    ./fd-standalone start
  
to start Flowdirector standalone. It is started as demon. Flowdirector listens
on port `8080`.

Use

    ./fd-standalone stop
    
to stop both.

Use 

    ./fd-standalone status
    
to see the status of the docker containers.

## Configuration Changes

The configuration file of Flowdirector is `fdserver/data/config/backend.json`. It is created on
the first start and preserved. Changes require a restart of Flowdirector.
