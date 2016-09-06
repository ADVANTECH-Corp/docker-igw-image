FROM armv7/armhf-ubuntu

#update and install npm 
RUN apt-get update
RUN apt-get install -y npm

# Install nodejs and npm node-red
RUN apt-get install -y nodejs-legacy
RUN npm install -g node-red

#Setting docker port and run node-red
EXPOSE 1880
CMD ["node-red"]

