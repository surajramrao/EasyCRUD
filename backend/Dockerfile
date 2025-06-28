From maven:3.8.3-openjdk-17-slim

Label env=backend

Workdir /app

Copy . .

Run mvn clean package -DskipTests

CMD ["java", "-jar", "target/student-registration-backend-0.0.1-SNAPSHOT.jar"]

