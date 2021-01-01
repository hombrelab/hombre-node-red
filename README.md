# hombre-node-red
![Docker Pulls](https://img.shields.io/docker/pulls/hombrelab/hombre-node-red) ![Docker Image Version (latest by date)](https://img.shields.io/docker/v/hombrelab/hombre-node-red) ![GitHub commit activity](https://img.shields.io/github/last-commit/hombrelab/hombre-node-red)

The [hombre-node-red](https://hub.docker.com/repository/docker/hombrelab/hombre-node-red) image is based on the [hombre-node](https://hub.docker.com/repository/docker/hombrelab/hombre-node) image and [Node-RED v1.2.6](https://nodered.org/).  
It is a customized Docker image for and by [@Hombrelab](me@hombrelab.com).

You can read more about Node-RED [nodered.org](https://nodered.org/) and on [GitHub](https://github.com/node-red).

Installed dependencies:
- [node-red](https://nodered.org)  
- [node-red-dashboard](https://flows.nodered.org/node/node-red-dashboard)  
- [node-red-node-base64](https://flows.nodered.org/node/node-red-node-base64)  
- [node-red-node-msgpack](https://flows.nodered.org/node/node-red-node-msgpack)  
- [node-red-node-suncalc](https://flows.nodered.org/node/node-red-node-suncalc)  
- [node-red-node-random](https://flows.nodered.org/node/node-red-node-random)    
- [node-red-node-snmp](https://flows.nodered.org/node/node-red-node-snmp)  
- [node-red-node-wol](https://flows.nodered.org/node/node-red-node-wol)    
- [node-red-contrib-amqp-ack](https://flows.nodered.org/node/node-red-contrib-amqp-ack)
- [node-red-contrib-better-sonos](https://flows.nodered.org/node/node-red-contrib-better-sonos)  
- [node-red-contrib-bigtimer](https://flows.nodered.org/node/node-red-contrib-bigtimer)  
- [node-red-contrib-buienradar](https://flows.nodered.org/node/node-red-contrib-buienradar)  
- [node-red-contrib-combine](https://flows.nodered.org/node/node-red-contrib-combine)  
- [node-red-contrib-credentials](https://flows.nodered.org/node/node-red-contrib-credentials)  
- [node-red-contrib-docker-stream](https://flows.nodered.org/node/node-red-contrib-docker-stream)  
- [node-red-contrib-home-assistant-websocket](https://flows.nodered.org/node/node-red-contrib-home-assistant-websocket)  
- [node-red-contrib-huemagic](https://flows.nodered.org/node-red-contrib-huemagic)
- [node-red-contrib-influxdb](https://flows.nodered.org/node/node-red-contrib-influxdb)  
- [node-red-contrib-key-value-store](https://flows.nodered.org/node/node-red-contrib-key-value-store)  
- [node-red-contrib-mongo-client](https://flows.nodered.org/node/node-red-contrib-mongo-client)  
- [node-red-contrib-node-hue](https://flows.nodered.org/node/node-red-contrib-node-hue)  
- [node-red-contrib-pi-hole](https://flows.nodered.org/node/node-red-contrib-pi-hole)  
- [node-red-node-ping](https://flows.nodered.org/node/node-red-node-ping)
- [node-red-contrib-plex](https://flows.nodered.org/node/node-red-contrib-plex)  
- [node-red-contrib-python-function](https://flows.nodered.org/node/node-red-contrib-python-function)
- [node-red-contrib-re-postgres](https://flows.nodered.org/node/node-red-contrib-re-postgres)  
- [node-red-contrib-rsync](https://flows.nodered.org/node/node-red-contrib-rsync)
- [node-red-contrib-slack](https://flows.nodered.org/node/node-red-contrib-slack)  
- [node-red-contrib-startup-trigger](https://flows.nodered.org/node/node-red-contrib-startup-trigger)  
- [node-red-contrib-ssh](https://flows.nodered.org/node/node-red-contrib-ssh)  
- [node-red-contrib-stoptimer](https://flows.nodered.org/node/node-red-contrib-stoptimer)  
- [node-red-contrib-tado-client](https://flows.nodered.org/node/node-red-contrib-tado-client)  
- [node-red-contrib-tahoma](https://flows.nodered.org/node/node-red-contrib-tahoma)
- [node-red-contrib-tcp-client](https://flows.nodered.org/node/node-red-contrib-tcp-client)  
- [node-red-contrib-tcp-server](https://flows.nodered.org/node/node-red-contrib-tcp-server)  
- [node-red-contrib-time-range-switch](https://flows.nodered.org/node/node-red-contrib-time-range-switch)  
- [node-red-contrib-timecheck](https://flows.nodered.org/node/node-red-contrib-timecheck)  
- [node-red-contrib-timerswitch](https://flows.nodered.org/node/node-red-contrib-timerswitch)  
- [node-red-contrib-traffic](https://flows.nodered.org/node/node-red-contrib-traffic)  
- [node-red-contrib-uibuilder](https://flows.nodered.org/node/node-red-contrib-uibuilder)  
- [node-red-contrib-unifi](https://flows.nodered.org/node/node-red-contrib-unifi)  
- [node-red-contrib-uuid](https://flows.nodered.org/node/node-red-contrib-uuid)  
- [node-red-contrib-web-watch](https://flows.nodered.org/node/node-red-contrib-web-watch)

Deployment example:

Command line
```shell script
docker run \
    --name node-red \
    --detach \
    --restart unless-stopped \
    --user root \
    --volume /home/data/node-red/data:/data \
    --volume /etc/localtime:/etc/localtime:ro \
    --publish 1880:1880 \
    hombrelab/hombre-node-red
```

DockerCompose
```yaml
  node-red:
    container_name: node-red
    restart: unless-stopped
    image: hombrelab/hombre-node-red
    user: root
    volumes:
      - /home/data/node-red/data:/data
      - /etc/localtime:/etc/localtime:ro
    ports:
      - 1880:1880
```