# Track Specification: Java 21 Migration and Virtual Threads

## Overview
This track involves upgrading the Sagan project from Java 17 to Java 21 (LTS) and enabling Java's Virtual Threads feature. This will modernize the runtime environment and improve the application's ability to handle high concurrency with lower resource overhead.

## Functional Requirements
- **Upgrade Runtime:** Update the project configuration to target Java 21 using the Adoptium (Eclipse Temurin) distribution.
- **Enable Virtual Threads:** Configure Spring Boot to use Virtual Threads for web request handling and task execution by setting `spring.threads.virtual.enabled=true`.

## Non-Functional Requirements
- **Maintain Compatibility:** Ensure the application remains fully functional after the upgrade, with no regressions in existing features.
- **Performance:** Leveraging Virtual Threads should theoretically improve scalability, though the primary goal is successful enablement without regression.

## Acceptance Criteria
- [ ] The project builds successfully using Java 21.
- [ ] The application starts up successfully with `spring.threads.virtual.enabled=true`.
- [ ] All existing unit and integration tests pass in the Java 21 environment.
- [ ] The `gradle.properties` or build files reflect the move to Java 21.

## Out of Scope
- Upgrading other major dependencies (unless strictly required for Java 21 compatibility).
- Refactoring existing code to use new Java 21 language features (e.g., Record Patterns, Switch Expressions) unless necessary.
