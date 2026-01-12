# Technology Stack

## Core Backend
- **Language:** Java 11
- **Framework:** Spring Boot 2.5.14
- **Security:** Spring Security (OAuth2, JOSE)
- **Validation:** Spring Boot Starter Validation
- **Hypermedia:** Spring Boot Starter HATEOAS

## Data & Persistence
- **Database (Production):** MySQL
- **Database (Development/Testing):** H2 (In-memory)
- **Abstraction:** Spring Data JPA (Hibernate)
- **Caching:** Redis (Spring Data Redis)
- **Migrations:** Flyway

## Frontend & Templating
- **Template Engine:** Thymeleaf (with Spring Security and Java 8 Time extras)
- **Build Tooling:** Webpack (sagan-client)
- **Styles:** SCSS
- **Parsing:** Jsoup (for HTML manipulation)

## Infrastructure & Integration
- **Build System:** Gradle
- **Content Conversion:** Asciidoctor (AsciidoctorJ)
- **Service Binding:** Java CloudFoundry Env (java-cfenv)
- **Feeds:** Rome (Atom feeds)
- **Mapping:** ModelMapper

## Testing
- **Framework:** JUnit 5 (JUnit Platform)
- **Isolation:** Testcontainers
- **API Documentation:** Spring Restdocs
- **Contract Testing:** Spring Cloud Contract
