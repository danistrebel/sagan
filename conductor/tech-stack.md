# Technology Stack

## Core Backend
- **Language:** Java 17
- **Framework:** Spring Boot 3.2.0 (Jakarta EE)
- **Security:** Spring Security 6 (OAuth2, JOSE)
- **Validation:** Spring Boot Starter Validation (Jakarta Bean Validation)
- **Hypermedia:** Spring Boot Starter HATEOAS
- **Logging:** Logback (SLF4J 2.0 compatible)

## Data & Persistence
- **Database (Production):** MySQL
- **Database (Development/Testing):** H2 (In-memory, MySQL mode)
- **Abstraction:** Spring Data JPA (Hibernate 6)
- **Caching:** Redis (Spring Data Redis)
- **Migrations:** Flyway

## Frontend & Templating
- **Template Engine:** Thymeleaf (with Spring Security 6 extras)
- **Build Tooling:** Webpack (sagan-client, Node 18.17.0)
- **Styles:** SCSS
- **Parsing:** Jsoup (for HTML manipulation)

## Infrastructure & Integration
- **Build System:** Gradle 8.12
- **Content Conversion:** Asciidoctor (AsciidoctorJ)
- **Service Binding:** Java CloudFoundry Env (java-cfenv 2.4.0)
- **Feeds:** Rome (Atom feeds 1.18.0)
- **Mapping:** ModelMapper 2.4.5
- **Redirects:** UrlRewriteFilter 5.1.3 (Jakarta compatible)

## Testing
- **Framework:** JUnit 5 (JUnit Platform)
- **Isolation:** Testcontainers 1.16.3
- **API Documentation:** Spring Restdocs 3.0.1
- **Contract Testing:** Spring Cloud Contract 4.1.0