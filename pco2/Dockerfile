FROM nodered/node-red
USER node-red
RUN npm config set https-proxy http://172.16.255.226:3128
RUN npm config set proxy http://172.16.255.226:3128
RUN npm install node-red-dashboard
RUN npm install node-red-contrib-kafka-manager
