FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl git

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs   

RUN git clone https://github.com/docker-hy/frontend-example-docker.git frontend

RUN cd /frontend && npm install

RUN git clone https://github.com/docker-hy/backend-example-docker.git backend

RUN cd /backend && npm install

EXPOSE 8000 5000

ENV API_URL="http://localhost:8000"

ENV FRONT_URL="http://localhost:5000"

COPY ./start.sh .

CMD ["sh", "/start.sh"]
