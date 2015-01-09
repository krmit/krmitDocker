FROM debian:jessie
#This dock file add system and networking programs.
MAINTAINER Magnus Kronnäs

################################################################

#    >> Basic apps <<

RUN apt-get update && apt-get install -y \
		nano
		git
		htop
		wget
		
################################################################

#    >> SSH server <<

RUN apt-get install -y openssh-server

# Create a directory to be used by ssh deamon.
RUN mkdir /var/run/sshd

# Create a password for root user.
RUN echo 'root:screencast' | chpasswd

# Chnage ssh config to allow  
RUN sed -i 's/PermitRootLogin without-password/PermitRootLogin yes/' /etc/ssh/sshd_config

# SSH login fix. Otherwise user is kicked off after login FIXME!
RUN sed 's@session\s*required\s*pam_loginuid.so@session optional pam_loginuid.so@g' -i /etc/pam.d/sshd

# FIXME!
ENV NOTVISIBLE "in users profile"
RUN echo "export VISIBLE=now" >> /etc/profile

################################################################

# Open up ssh port.
EXPOSE 22

# Start the ssh deamon.
CMD ["/usr/sbin/sshd", "-D"]
