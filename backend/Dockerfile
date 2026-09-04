# Etapa 1: build da aplicação usando Gradle + JDK 21
FROM gradle:8.10-jdk21 AS build
WORKDIR /app
COPY . .
RUN gradle build -x test --no-daemon

# Etapa 2: imagem final, só com o JRE e o jar gerado
FROM eclipse-temurin:21-jre
WORKDIR /app
COPY --from=build /app/build/libs/*.jar app.jar
EXPOSE 8083
ENTRYPOINT ["java", "-jar", "app.jar"]