# ctd

```
docker build --build-arg HTTP_PROXY=http://172.16.255.226:3128 \
             --build-arg HTTPS_PROXY=http://172.16.255.226:3128 \
               -t ctd .
```

```
   docker run -d --name=ctd --restart=always \
             --add-host=gconode05:172.16.255.12 \
       -v /home/opsuser/dev/docker/ctd/data:/data ctd
```

if everything is working correctly, the service can be reached
from [ctd.spiddal.dm.marine.ie](http://ctd.spiddal.dm.marine.ie)

