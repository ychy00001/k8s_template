FROM openjdk:8-jre-alpine

ENV ENV_JAR_RUN_PROFILE dev
ENV APP_NAME smsclient

COPY smsclient-0.0.1-SNAPSHOT.jar /app/smsclient-0.0.1-SNAPSHOT.jar

EXPOSE 8080

ENTRYPOINT ["java","-jar","/app/smsclient-0.0.1-SNAPSHOT.jar"]
