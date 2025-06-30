FROM maven:3.8.3-openjdk-17-slim

LABEL env=backend

WORKDIR /app

COPY . .

EXPOSE 8080

RUN mvn clean package -DskipTests

CMD ["java", "-jar", "target/student-registration-backend-0.0.1-SNAPSHOT.jar"]
