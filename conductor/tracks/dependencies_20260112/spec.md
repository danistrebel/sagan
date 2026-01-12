# Track Specification: Refactor and Update Project Dependencies

## Context
The Sagan project is currently running on older versions of Spring Boot (2.5.14) and other dependencies. To ensure security, performance, and maintainability, these dependencies need to be updated. This track focuses on upgrading the build system and core frameworks.

## Goals
1.  **Upgrade Build System:** Update Gradle Wrapper to a recent stable version compatible with newer Java versions.
2.  **Upgrade Spring Boot:** Attempt to upgrade Spring Boot to a newer 2.x version or prepare for 3.x if feasible (checking for breaking changes).
3.  **Dependency Alignment:** Ensure all related dependencies (Spring Security, Spring Data, etc.) are aligned with the new Spring Boot version.
4.  **Verify Stability:** Ensure the application builds and all tests pass after the upgrades.

## Non-Goals
- Adding new features.
- Major architectural refactoring beyond what is required for dependency compatibility.
- Upgrading to Java 17+ (unless strictly required by the new Spring Boot version, though Java 17 is the new baseline for Spring Boot 3). *Note: The project is currently on Java 11.*

## Technical Considerations
- **Breaking Changes:** Watch out for deprecated APIs in Spring Boot and Spring Security.
- **Gradle Plugins:** Ensure third-party Gradle plugins are compatible with the new Gradle version.
- **Transitive Dependencies:** Use `gradle dependencies` to check for conflict resolutions.
