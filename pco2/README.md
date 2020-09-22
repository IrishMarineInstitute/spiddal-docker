# pco2

```
docker build --build-arg HTTP_PROXY=http://172.16.255.226:3128 \
             --build-arg HTTPS_PROXY=http://172.16.255.226:3128 \
               -t pco2 .
```

```
   docker run -d --name=pco2 --restart=always \
             --add-host=gconode05:172.16.255.12 \
       -v /home/opsuser/dev/docker/pco2/data:/data pco2
```

if everything is working correctly, the service can be reached
from [pco2.spiddal.dm.marine.ie](http://pco2.spiddal.dm.marine.ie)

