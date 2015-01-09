FROM debian:jessie
#This dock file add system and networking programs.
MAINTAINER Magnus Kronnäs

#Basic apps
RUN apt-get update && apt-get install -y \
nano

#Basic System tools
RUN apt-get update && apt-get install -y \
htop

# Basic Networking tools
RUN apt-get update && apt-get install -y \
		openssh-server \
		wget
		

#Open up ssh port.
EXPOSE 22
