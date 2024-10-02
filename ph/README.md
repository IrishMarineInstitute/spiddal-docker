# ph

```
docker build --build-arg HTTP_PROXY=http://172.16.255.226:3128 \
             --build-arg HTTPS_PROXY=http://172.16.255.226:3128 \
               -t ph .
```

```
   docker run -d --name=ph --restart=always \
             --add-host=gconode05:172.16.255.12 \
       -v /home/opsuser/dev/docker/ph/data:/data ph
```

if everything is working correctly, the service can be reached
from [ph.spiddal.dm.marine.ie](http://ph.spiddal.dm.marine.ie)

