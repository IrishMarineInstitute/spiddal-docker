# fluorometer

```
docker build --build-arg HTTP_PROXY=http://172.16.255.226:3128 \
             --build-arg HTTPS_PROXY=http://172.16.255.226:3128 \
               -t fluorometer .
```

```
   docker run -d --name=fluorometer --restart=always \
             --add-host=gconode05:172.16.255.12 \
       -v /home/opsuser/dev/docker/fluorometer/data:/data fluorometer
```

if everything is working correctly, the service can be reached
from [fluorometer.spiddal.dm.marine.ie](http://fluorometer.spiddal.dm.marine.ie)

