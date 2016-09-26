FROM armv7/armhf-ubuntu

MAINTAINER Advantech

# Update
RUN apt-get update

# Install minicom
RUN apt-get install -y minicom

# Install sennet-wise_3310
COPY sennet* /home
RUN ["/bin/bash", "-c", "./home/sennet-wise_3310-1.3.00.0354.run"]

# Creates a mount path for other containers
VOLUME /usr/lib/Advantech/iotgw

# Run WSN API
ENTRYPOINT ["/usr/bin/sampleSNManagerAPI"]

