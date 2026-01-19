# Dependency Analysis Report - Track modernize_deps_20260119

## Current State
- Spring Boot: 2.5.14
- Spring Cloud: 3.0.4 (Contract)
- Java: 11
- Gradle: 7.3.1

## Target Versions (Phase 2: Bridge to 2.7.x)
- Spring Boot: 2.7.18 (Latest of 2.7.x)
- Spring Dependency Management: 1.1.0
- Spring Cloud: 2021.0.8 (Compatible with Spring Boot 2.7.x)
- Flyway: 8.5.13 (Compatible with Spring Boot 2.7.x)
- H2: 2.1.214

## Target Versions (Future: 3.x/4.x)
- Spring Boot: 4.0.1
- Java: 17+ (Required for SB 3+)
- Jakarta EE migration required.

## Migration Notes (SB 2.6/2.7)
- **Circular References:** Now prohibited by default. May need `spring.main.allow-circular-references: true` if refactoring is too complex.
- **Path Matching:** Default changed to `PathPatternParser`. Might need `spring.mvc.pathmatch.matching-strategy: ant-path-matcher` for compatibility with older security configs.
- **H2 Upgrade:** H2 2.1+ is backward incompatible. Database files might need recreation.
- **Flyway:** Flyway 8.5+ requires separate modules for specific databases (e.g., `flyway-mysql`).
- **Auto-configuration:** `spring.factories` is deprecated in favor of `META-INF/spring/org.springframework.boot.autoconfigure.AutoConfiguration.imports`.
