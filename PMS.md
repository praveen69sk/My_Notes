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
                 SPRING_SQL_INT_MODE=always