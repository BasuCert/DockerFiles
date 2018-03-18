# Build & Run
## docker build -t burpff .
## docker run -v /tmp/.X11-unix/:/tmp/.X11-unix -e DISPLAY=$DISPLAY -p 8080:8080 -it burpff

# Base Image
FROM openjdk:8-jre-alpine

# Info
LABEL maintainer "lopqto <morpix@protonmail.com>"

ENV BURP_VERSION 1.7.32

# Configure
RUN apk --update add --no-cache dbus ttf-freefont fontconfig openssl ca-certificates ttf-dejavu 
RUN rm -f /var/cache/apk/*
RUN mkdir -p /opt/burp /work 
RUN adduser -D -s /bin/sh user user 
RUN chown -R user /work
RUN wget -q -O /opt/burp/burpsuite.jar "https://portswigger.net/Burp/Releases/Download?productId=100&version=$BURP_VERSION&type=Jar"

RUN chown -R user /home/user/.*
USER user

WORKDIR /work

ENTRYPOINT ["java", "-jar", "/opt/burp/burpsuite.jar"]
