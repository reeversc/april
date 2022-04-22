FROM rasa/rasa:latest

WORKDIR /app
COPY . /app
USER root

COPY ./data /app/data

RUN  rasa train 

VOLUME /app
VOLUME /app/data
VOLUME /app/models

CMD [ "run","-m","/app/models","--enable-api","--cors","*","--debug" ]