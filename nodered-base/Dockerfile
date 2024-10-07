FROM nodered/node-red:2.2
USER node-red
RUN npm config set https-proxy http://172.16.255.226:3128 \
&& npm config set proxy http://172.16.255.226:3128
RUN npm install node-red-dashboard node-red-contrib-kafka-manager node-red-contrib-tcp-client2
