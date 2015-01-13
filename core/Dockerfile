FROM debian:jessie
#This dockfile add some basic system and networking programs.
MAINTAINER Magnus Kronnäs

################################################################
#       Basic apps                                             #
################################################################

RUN apt-get update && apt-get install -y \
		nano
		git
		htop
		wget

################################################################
#       Create a start script.                                 #
################################################################

# Create an empty file to be our start script.
RUN echo "" > start.sh
RUN chmod 700 start.sh

# Use our startup script every time someone start our dockers.
CMD ["start.sh"]
