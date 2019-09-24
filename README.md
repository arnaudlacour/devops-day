# Devops Day
Simply Git clone this repository to get started

## Instructions

### Start a first directory instance
Simply start the pingdirectory service as a daemon (in the background)

`docker-compose up -d pingdirectory`

Wait a while for the service to successfully start the first container, this may take a few minutes.

### Scale up
Scale the service up to add a second PingDirectory container.

`docker-compose up -d --scale pingdirectory=2 pingdirectory`

The second will join the first in the service to become a cluster.
Docker will make them both accessible via the service name: pingdirectory

### Start a PingFederate service using the pingdirectory service
`docker-compose up -d pingfederate`

This should be up in 30 seconds or so.

### Start the PingDirectory console
If you want to look around configuration or edit schema, the PingDirectory can be useful.

`docker-compose up -d pingdataconsole`
