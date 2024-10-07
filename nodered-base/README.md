# nodered-base
Base image for NodeRED containers in Spiddal Shorestation, including proxy parameters. 

## Version
Currently using NodeRED v2.2 (newest versions create incompatibility with Kafka extension).
Custom image versionning follows NodeRED versions to avoid confusion.

## Build
The base image should already be built. If needed, it can be rebuilt using the following command:
```
docker build --build-arg HTTP_PROXY=http://172.16.255.226:3128 \
             --build-arg HTTPS_PROXY=http://172.16.255.226:3128 \
               -t spiddal-nodered:2.2 .
```

## Usage
Use the following command to deploy a new NodeRED container instance:
```
   docker run -d --name=<new-instance-name> --restart=always \
             --add-host=gconode05:172.16.255.12 \
       -v <local/path/to/flow/data>:/data spiddal-nodered:2.2
```

## To do
Once a container registry is available, have this image in it.