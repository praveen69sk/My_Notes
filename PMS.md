# Patient Service
1. URL --> http://localhost:4000/patients

2. H2 Console --> http://localhost:4000/h2-console/

3. Swagger UI --> http://localhost:4000/swagger-ui/index.html#/

4. POSTGRES DB --> Docker
                  * POSTGRES_USER  admin_user
                  * POSTGRES_PASSWORD password
                  * POSTGRES_DB db

5. DOCKER    --> SPRING_DATASOURCE_URL=jdbc:postgresql://patient-service-db:5432/db
                 SPRING_DATASOURCE_USERNAE=admin_user;
                 SPRING_DATASOURCE_PASSWORD=password;
                 SPRING_JPA_HIBERNATE_DDL_AUTO=update;
                 SPRING_SQL_INIT_MODE=always


spring.datasource.url=jdbc:postgresql://patient-service-db:5432/db
spring.datasource.username=admin_user
spring.datasource.password=password
spring.jpa.hibernate.ddl-auto=update
spring.sql.init.mode=always

## Billing Service Docker File

``` DockerFile
FROM maven:3.9.9-eclipse-temurin-21 AS builder

WORKDIR /app

COPY pom.xml .

RUN mvn dependency:go-offline -B

COPY src ./src

RUN mvn clean package

FROM openjdk:21-jdk AS runner

WORKDIR /app

COPY --from=builder ./app/target/billing-service-0.0.1-SNAPSHOT.jar ./app.jar

EXPOSE 4001

EXPOSE 9001

ENTRYPOINT ["java", "-jar", "app.jar"]
```

***

## Kafka
        * --> Add kafka intellij plugin
        * --> Setup Kafka Broker using docker image

## Integration Test --> Using Rest Assured