FROM ubuntu:18.04

WORKDIR /usr/src/app

COPY webby_scrippy.sh .

RUN apt-get update; apt-get install curl -y

RUN chmod +x webby_scrippy.sh

CMD /usr/src/app/webby_scrippy.sh