# Example using React (with Apollo) to make GraphQL call to Spring Boot Data JPA backed by Oracle via UCP

See soon to be released blog under: https://blogs.oracle.com/authors/paulparkinson

## Instructions
1. `cd spring-data-jpa-graphql-ucp-oracle`
2. Modify `src/main/resources/application.properties` to set values for `spring.datasource.url`, `spring.datasource.username`, and `spring.datasource.password`
3. Run `mvn clean install`
4. Run `java -jar target/spring-data-jpa-graphql-oracle-0.0.1-SNAPSHOT.jar`
5. (In a separate terminal/console) `cd react-graphql`
6. Run `yarn add @apollo/client graphql` (this is only necessary once for the project)
7. Run `npm run build`
8. Run `npm start` 

#### A browser window should open to http://localhost:3000/ which is a React app that will use Apollo to make a GraphQL query against a Spring Boot service running on localhost:8080 which in turn uses JPA to query an Oracle database via a connection obtained from UCP.