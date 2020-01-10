FROM ubuntu:latest

MAINTAINER sko <sko@student.42.us.org>

RUN apt-get update -y && apt-get upgrade -y && \
	apt-get install -y curl openssh-server ca-certificates && \
	apt-get install -y postfix && apt-get install -y tzdata

WORKDIR /tmp

RUN curl -LO https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh && chmod 777 script.deb.sh && ./script.deb.sh

RUN apt-get install -y gitlab-ce

EXPOSE 80 443 22 22222

RUN apt-get update && apt-get install nano

#docker run -it --rm -P --privileged ex03 bash
# Modify the gitlab.rb file
#nano/etc/gitlab/gitlab.rb
#unicorn ['worker_processes'] = 3

#(/opt/gitlab/embedded/bin/runsvdir-start &) && gitlab-ctl reconfigure && tail -f /dev/null
