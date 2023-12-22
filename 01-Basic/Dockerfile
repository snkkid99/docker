FROM ubuntu:latest

RUN apt-get -y update && apt-get -y install python3

ADD file.py /example/file.py

WORKDIR /example/

CMD python3 file.py
