FROM maven:3-jdk-8 AS builder

MAINTAINER phithon <root@leavesongs.com>

COPY ./ /usr/src/

WORKDIR /usr/src

RUN cd /usr/src; \
    mvn clean install

# production
FROM openjdk:8-jre

LABEL maintainer="phithon <root@leavesongs.com>"

COPY --from=builder /usr/src/target/spring-boot-websocket-1.0.jar /spring-boot-websocket-1.0.jar

CMD ["java", "-Djava.security.egd=file:/dev/./urandom", "-jar", "/spring-boot-websocket-1.0.jar"]