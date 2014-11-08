FROM debian:jessie
#This dock file add system and networking programs.
MAINTAINER Magnus Kronnäs

#Basic apps
RUN apt-get update && apt-get install -y \
		nano

#Basic System tools
RUN apt-get update && apt-get install -y \
		htop \
		tmux

#Basic Networking tools
RUN apt-get update && apt-get install -y \
		curl \
		nmap \
		openssh-client \
		openssh-server \
		traceroute \
		wget
