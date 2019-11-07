FROM  openjdk:8-jre-alpine
VOLUME  /tmp
EXPOSE 8761
ADD ./target/service-registry-1.0-SNAPSHOT.jar app.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
