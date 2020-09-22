# kafdrop
```
docker build -t kafdrop .
docker run -d --name=kafdrop --restart=always \
       --add-host=gconode05:172.16.255.12 \
       -e KAFKA_BROKERCONNECT=gconode05:9092 \
        -e "JVM_OPTS=-Xms32M -Xmx64M" \
        -e SERVER_SERVLET_CONTEXTPATH=/ kafdrop
```
Now if it works you should be able to visit 
[kafdrop.spiddal.dm.marine.ie](http://kafdrop.spiddal.dm.marine.ie)
