FROM ubuntu:latest

WORKDIR /app

COPY . /app

RUN apt-get update && apt-get upgrade -y python3 python3-pip

CMD [ "python3", "app.py" ]