FROM debian
MAINTAINER sko <sko@student.42.us.org>
WORKDIR /home
EXPOSE 9987/udp 10011 30033
RUN apt-get update && \
	apt-get install -y wget bzip2 && \
	wget files.teamspeak-services.com/releases/server/3.10.0/teamspeak3-server_linux_amd64-3.10.0.tar.bz2 && \
	tar xvf *.tar.bz2 && \
	rm -rf teamspeak3-server_linux_amd64-3.10.0.tar.bz2
WORKDIR teamspeak3-server_linux_amd64
ENTRYPOINT sh ts3server_minimal_runscript.sh license_accepted=1

# how to build docker image
# docker build -t kosehy/teamspeak .

# how to run container
# docker run ocker run --rm  -it -p 9987:9987/udp -p 10011:10011 -p 30033:30033 kosehy/teamspeak

# Resources:
# https://hub.docker.com/r/aheil/teamspeak3-server/
# https://github.com/TeamSpeak-Systems/teamspeak-linux-docker-images/blob/master/alpine/Dockerfile
# https://hub.docker.com/_/teamspeak
