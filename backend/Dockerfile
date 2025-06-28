From maven:3.8.3-openjdk-17-slim

Label env=backend

Workdir /app

copy . .

Run maven clean package -DskipTests

CMD ["-jar","java","target/*.jar"]