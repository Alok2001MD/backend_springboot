FROM maven:3.8.5-openjdk:17 AS build
COPY . .
RUN mvn clean package -DskipTests
From openjdk:17.0.1-jdk-slim
COPY --from=build/QuizApplication-0.0.1-SNAPSHOT.jar QuizApplication.jar
EXPOSE 8080
CMD ["java", "-jar", " QuizApplication.jar"]
