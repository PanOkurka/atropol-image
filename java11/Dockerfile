FROM        adoptopenjdk/openjdk11-openj9:alpine

LABEL       author="PanOkurka" maintainer="vedeni@atropol.eu"

RUN apk add --update --no-cache curl ca-certificates openssl git tar bash sqlite fontconfig \
    && adduser -D -h /home/container container
 
USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./entrypoint.sh /entrypoint.sh

CMD         ["/bin/ash", "/entrypoint.sh"]