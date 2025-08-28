FROM maven:3.9.6-eclipse-temurin-17-alpine AS CopyBuilder

WORKDIR /app

COPY . .

FROM maven:3.9.6-eclipse-temurin-17-alpine AS RunBuilder

WORKDIR /app

COPY --from=CopyBuilder /app /app
# should copy only jar file
RUN ./mvnw clean  package


FROM eclipse-temurin:17-jre-alpine

WORKDIR /app

COPY --from=RunBuilder /app /app

EXPOSE 8080

CMD java -jar target/*.jar
