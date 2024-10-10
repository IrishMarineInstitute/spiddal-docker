# ADCP
## Create container instance
This flow runs the NodeRED base image with new data.
To create and run the container instance, use the following command:

```
	docker run -d --name=adcp --restart=always \
	--add-host=gconode05:172.16.255.12 \
	--mount type=bind,source=/path/to/repo/adcp/data,target=/data \
	--mount type=bind,source=/path/to/config/file,target=/conf/device_config.csv,readonly \
        --mount type=bind,source=/path/to/command/config/file,target=/conf/device_config.txt,readonly
	spiddal-nodered:2.2
```
## Updating configuration
Configuration files are mounted from a local copy of the repository gathering sensor configuration files.
They are generically mounted as /conf/device_config.csv and /conf/device_config.txt (if initialisation commands available).
Note:
* if mounting these files in /data, this ends up in having a copy of the file in the target /data folder. To avoid
* in order for updates to be synchronized with the container, proper rights must be set to the target files (currently 777, to refine)

## Check results
You must wait for the container to be fully started before traefik picks it up.

If everything is working correctly, the service can be reached from [adcp.spiddal.dm.marine.ie](http://adcp.spiddal.dm.marine.ie).
Otherwise, check that the container instance is running properly by consulting the logs:
```
docker logs adcp
```
