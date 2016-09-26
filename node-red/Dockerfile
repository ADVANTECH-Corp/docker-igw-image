FROM armv7/armhf-ubuntu

MAINTAINER Advantech

#update and install npm
RUN apt-get update
RUN apt-get install -y npm

# Install nodejs and npm node-red
RUN apt-get install -y nodejs-legacy
RUN npm install -g node-red

# Can not Install SUSI node
#RUN npm install node-susi
#RUN npm install node-red-contrib-susi -g

# Install alljoyn node
RUN npm install node-alljoyn
RUN npm install node-red-contrib-alljoyn -g

# Install wsn node
RUN npm install node-red-contrib-wsn -g

# Install sennet-wise_3310
COPY sennet* /home
RUN ["/bin/bash", "-c", "./home/sennet-wise_3310-1.3.00.0354.run"]

#Setting docker port and run node-red
EXPOSE 1880

# Run Node-red
ENTRYPOINT ["node-red"]

