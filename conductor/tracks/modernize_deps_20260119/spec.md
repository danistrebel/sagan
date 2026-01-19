# Track Specification: Modernize Dependencies and Improve Observability

## Goal
Update the project's core dependencies, specifically Spring Boot, to the latest stable versions compatible with the codebase (targeting Spring Boot 2.7.x or 3.x if feasible, starting with incremental updates). Enhance system observability by configuring Spring Boot Actuator and adding custom health indicators.

## Context
The current application uses Spring Boot 2.5.14 and Java 11. Keeping dependencies up-to-date is crucial for security, performance, and access to new features. Enhanced observability will improve production monitoring and issue diagnosis.

## Requirements

### Dependency Updates
- [ ] Upgrade Spring Boot from 2.5.14 to the latest 2.7.x release (as a bridge to 3.x).
- [ ] Upgrade Spring Data, Spring Security, and other managed dependencies.
- [ ] Upgrade frontend dependencies (Webpack, etc.) where applicable and safe.
- [ ] Ensure Java 11 compatibility is maintained (or upgrade to 17 if 3.x is chosen, but starting with 2.7.x/Java 11 is safer).

### Observability
- [ ] Ensure `spring-boot-starter-actuator` is properly configured.
- [ ] Expose relevant endpoints (health, info, metrics, env, loggers) securely.
- [ ] Implement a custom `HealthIndicator` for Redis connectivity.
- [ ] Implement a custom `HealthIndicator` for critical external services (e.g., GitHub API if used).

### Quality Assurance
- [ ] All existing unit and integration tests must pass.
- [ ] The application must start successfully without deprecation warnings (where possible).
- [ ] Basic manual verification of the site functionality.

## Out of Scope
- Full migration to Spring Boot 3.0 (if it requires Jakarta EE migration and Java 17 upgrade that is too large for this single track). We will target 2.7.x first.
- Major UI redesigns.
