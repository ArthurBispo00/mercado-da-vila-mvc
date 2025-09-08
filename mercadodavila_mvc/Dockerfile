# Etapa 1: Usar uma imagem base oficial com Java 21
FROM openjdk:17-jdk-slim

# Etapa 2: Definir o diretório de trabalho dentro do container
WORKDIR /app

# Etapa 3: Copiar os arquivos do Maven e dar permissão de execução
COPY .mvn/ .mvn
COPY mvnw pom.xml ./
RUN chmod +x mvnw

# Etapa 4: Baixar todas as dependências
RUN ./mvnw dependency:go-offline

# Etapa 5: Copiar o código-fonte da sua aplicação
COPY src ./src

# Etapa 6: Compilar o projeto e empacotar em um arquivo .jar
RUN ./mvnw package -DskipTests

# Etapa 7: Expor a porta que sua aplicação usa
EXPOSE 8082

# Etapa 8: Definir o comando para iniciar sua aplicação
ENTRYPOINT ["java", "-jar", "target/mercado-da-vila-mvc-0.0.1-SNAPSHOT.jar"] 
# ATENÇÃO: Verifique no seu pom.xml se o nome do .jar gerado é este mesmo!