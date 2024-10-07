# ADCP
# Create container instance
This flow runs the NodeRED base image with new data.
To create and run the container instance, use the following command:

```
	docker run -d --name=adcp --restart=always \
	--add-host=gconode05:172.16.255.12 \
	-v /path/to/repo/adcp/data:/data \
	-v /path/to/config/file:/data/device_config.csv
	spiddal-nodered:2.2
```

# Check results
You will have to restart the traefik container to make it aware of the latest container processes:

```
docker restart treafik
```

If everything is working correctly, the service can be reached from [adcp.spiddal.dm.marine.ie](http://adcp.spiddal.dm.marine.ie).
Otherwise, check that the container instance is running properly by consulting the logs:
```
docker logs adcp
```
