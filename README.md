## Mosquitto MQTT broker image

### Expose

tcp/1883  MQTT port  
tcp/9001  websocket

### Container Quickstart

Run for MQTT only:  
`docker run -d -p 1883:1883 --name=mosquitto sourceperl/mosquitto`

Run for MQTT + websocket:  
`docker run -d -p 1883:1883 -p 9001:9001 --name=mosquitto sourceperl/mosquitto`

Link to mosquitto from another container:  
`docker run -d --link mosquitto --name=mqttwarn sourceperl/mqttwarn`

### Build local images

    # git clone https://github.com/sourceperl/docker.mosquitto.git
    # cd docker.mosquitto
    # docker build -t sourceperl/mosquitto .
