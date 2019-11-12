#FROM maven:3.3-jdk-8 as builder
#COPY . /build/
#WORKDIR /build
#RUN mvn clean install

#FROM openjdk:8-jre-alpine
#COPY --from=builder /build/target/demoapp.jar /opt/
#EXPOSE 8080
#CMD ["java", "-jar", "/opt/target/demoapp.jar"]

FROM maven:3.6-jdk-8-alpine as builder
WORKDIR /app
COPY pom.xml .
RUN mvn -e -B dependency:resolve
COPY src ./src
RUN mvn -e -B package
CMD ["java", "-jar", "target/jb-hello-world-maven-0.1.0.jar"]

FROM openjdk:8-jre-alpine
COPY --from=builder /app/target/jb-hello-world-maven-0.1.0.jar /opt/
CMD ["java", "-jar", "/opt/jb-hello-world-maven-0.1.0.jar"]
