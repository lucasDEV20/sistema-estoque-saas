# Usa uma imagem base com Java 17 (ou a versão que você estiver usando)
FROM eclipse-temurin:17-jdk-alpine
VOLUME /tmp
# Copia o seu arquivo .jar gerado para dentro do container
COPY target/*.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]