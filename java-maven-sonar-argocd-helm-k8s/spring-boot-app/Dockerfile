# You can change this base image to anything else
# But make sure to use the correct version of Java
FROM adoptopenjdk/openjdk11:alpine-jre

# Simply the artifact path
ARG artifact=target/spring-boot-web.jar
RUN apt-get update && apt-get install -y openjdk-17-jdk maven git curl \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /opt/app

COPY ${artifact} app.jar

# This should not be changed
ENTRYPOINT ["tail", "-f", "/dev/null"]




