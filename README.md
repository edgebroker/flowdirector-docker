# Flow Director Docker Compose Template

This repository contains docker compose templates to start/stop Flow Director.

Please clone this repository and open a shell within the root directory `flowdirector-docker`.

Use

    ./flowdirector start
  
to start Flow Director and a single embedded SwiftMQ Router. Flow Director listens
on port `8080` (HTTP), SwiftMQ on port `4001` (JMS), `5672` (AMQP) and `1883` (MQTT).

Use

    ./flowdirector stop
    
to stop both.

Use 

    ./flowdirector status
    
to see the status of the docker containers.
