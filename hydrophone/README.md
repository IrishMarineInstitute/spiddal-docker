# hydrophone

```
docker build --build-arg HTTP_PROXY=http://172.16.255.226:3128 \
             --build-arg HTTPS_PROXY=http://172.16.255.226:3128 \
               -t hydrophone .
```

```
   docker run -d --name=hydrophone --restart=always \
             --add-host=gconode05:172.16.255.12 \
         -v /home/opsuser/.ssh:/usr/src/node-red/.ssh \
       -v /home/opsuser/dev/docker/hydrophone/data:/data hydrophone
```

if everything is working correctly, the service can be reached
from [hydrophone.spiddal.dm.marine.ie](http://hydrophone.spiddal.dm.marine.ie)

