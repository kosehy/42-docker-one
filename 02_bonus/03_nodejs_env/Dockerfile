#git clone https://github.com/self-tuts/Nodejs-application-with-docker app
FROM alpine:latest
RUN apk add --no-cache nodejs npm git && \
	git clone https://github.com/self-tuts/Nodejs-application-with-docker app

#make folder inside the docker container
WORKDIR /app

RUN npm install

EXPOSE 9005
#run command "node server.js"
ENTRYPOINT ["node"]

CMD ["server.js"]

#build docker image
#docker build -t node-app:latest .

#running docker container
#docker run -it -d -p 9002:9005 node-app:latest
