FROM maven:3.5-jdk-8-alpine as builder
WORKDIR /build
COPY pom.xml .
RUN mvn dependency:go-offline

COPY src/ /build/src/
RUN mvn package

FROM openjdk:8-jre-alpine
COPY --from=builder /build/target/worker-jar-with-dependencies.jar .
CMD java -jar worker-jar-with-dependencies.jar
