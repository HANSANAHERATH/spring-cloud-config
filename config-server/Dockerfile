FROM azul/zulu-openjdk-alpine:11

COPY target/config-server-0.0.1-SNAPSHOT.jar /config-service.jar
 
CMD ["java", "-jar", "/config-service.jar"]