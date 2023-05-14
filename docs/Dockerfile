FROM maven:3-eclipse-temurin-17
ENV http_proxy=http://host.docker.internal:7890 \
    https_proxy=http://host.docker.internal:7890

WORKDIR /build
COPY . .

RUN mkdir -p /root/.m2
COPY ./docs/settings.xml /root/.m2/settings.xml

RUN mvn dependency:go-offline