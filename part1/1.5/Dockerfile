FROM ubuntu:16.04 

RUN apt-get update && apt-get install -y curl git

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs

RUN git clone https://github.com/docker-hy/frontend-example-docker.git frontend

WORKDIR frontend

RUN npm install

EXPOSE 5000

CMD ["npm", "start"]
