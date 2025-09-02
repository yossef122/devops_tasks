FROM maven:3.9.6-eclipse-temurin-17-alpine

WORKDIR /app

COPY . .

RUN ./mvnw clean  package

EXPOSE 8080

CMD java -jar target/*.jar
