# adcp

```
docker build --build-arg HTTP_PROXY=http://172.16.255.226:3128 \
             --build-arg HTTPS_PROXY=http://172.16.255.226:3128 \
               -t adcp .
```

```
   docker run -d --name=adcp --restart=always \
             --add-host=gconode05:172.16.255.12 \
       -v /home/opsuser/dev/docker/adcp/data:/data adcp
```

if everything is working correctly, the service can be reached
from [adcp.spiddal.dm.marine.ie](http://adcp.spiddal.dm.marine.ie)

