FROM maven:3-openjdk-11 AS builder
WORKDIR /app
COPY . .
RUN mvn clean install 
FROM openjdk:11.0.10-jre
WORKDIR /app
COPY --from=builder /app/target/shoes-0.0.1-SNAPSHOT.jar .
EXPOSE 1002
CMD ["java","-jar","shoes-0.0.1-SNAPSHOT.jar"]

