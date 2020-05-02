# Flow Director Docker Compose Template

This repository contains a docker compose template to start/stop Flow Director.

Please clone this repository and open a shell within the root directory `flowdirector-docker`.

Use

    ./flowdirector start
  
to start Flow Director. 

Flow Director embeds a SwiftMQ Router and listens on port `8080` (HTTP), `4001` (JMS), `5672` (AMQP), `1883` (MQTT),
and `4100` (Routing listener).

Use

    ./flowdirector stop
    
to stop it.

Use 

    ./flowdirector status
    
to see the status of the docker container.

# Access via Browser

Point your browser to [http://localhost:8080](http://localhost:8080) to use Flow Director.

# Data

After the first start you'll find the data of the Flow Director server under directory `fdserver/data`. The data of the 
embedded SwiftMQ Router under `router/data`. This is informational as very seldom need to touch it. 


