#mkdir src; touch src/index.php
#<?php
#	echo "Hello, World from Docker! <br>";
#	echo "Hello ECS! <br>";
#	echo '<img src="https://www.docker.com/sites/default/files/horizontal.png">';
#?>
FROM php:7.2-apache
RUN apt-get update && apt-get upgrade -y && apt-get install -y vim git
COPY ./src /var/www/html/
EXPOSE 80
#docker run -d --rm -P b02
