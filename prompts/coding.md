# Coding Prompts — 20 Templates

## Debugging & Troubleshooting

### 1. Systematic Bug Diagnosis
```
I have a bug in my [LANGUAGE] application. Symptom: [DESCRIBE BEHAVIOR]. Expected behavior: [DESCRIBE EXPECTED]. Environment: [OS/RUNTIME/VERSIONS]. Here is the relevant code:

[PASTE CODE]

Walk me through a systematic diagnosis: (1) identify possible root causes ranked by probability, (2) suggest diagnostic steps for each, (3) provide the fix for the most likely cause, (4) explain why it works.
```

### 2. Error Message Decoder
```
I'm getting this error: [PASTE FULL ERROR/STACK TRACE]. Language: [LANGUAGE]. Framework: [FRAMEWORK]. What I was doing: [CONTEXT]. Explain: (1) what caused this error in plain English, (2) the most common fix, (3) how to prevent it in the future, (4) any related errors I should watch for.
```

### 3. Performance Profiling Guide
```
My [LANGUAGE] application has a performance issue: [DESCRIBE — slow startup, high memory, CPU spike, etc.]. Architecture: [MONOLITH/MICROSERVICE/SERVERLESS]. Scale: [REQUESTS/DATA VOLUME]. Generate a profiling plan: (1) which profiling tools to use, (2) what metrics to capture, (3) common culprits for this type of issue, (4) optimization strategies ranked by impact.
```

### 4. Memory Leak Detective
```
My [LANGUAGE] application's memory usage grows over time. Runtime: [NODE/PYTHON/JVM/etc.]. Observed: [CURRENT MEMORY BEHAVIOR]. Here is a code section I suspect:

[PASTE CODE]

Analyze for memory leaks: (1) identify leak patterns (circular refs, event listeners, closures, caches), (2) suggest fixes, (3) recommend monitoring setup to detect future leaks.
```

## Code Review & Refactoring

### 5. Code Review Checklist
```
Review this [LANGUAGE] code for production readiness:

[PASTE CODE]

Check against: (1) correctness — logic errors, edge cases, off-by-one, (2) security — injection, auth, data exposure, (3) performance — O(n) analysis, unnecessary allocations, (4) maintainability — naming, SRP, DRY, (5) error handling — failure modes, recovery. Rate each category GREEN/YELLOW/RED with specific findings.
```

### 6. Refactoring Advisor
```
Refactor this [LANGUAGE] code to improve [READABILITY/PERFORMANCE/TESTABILITY]:

[PASTE CODE]

Apply these principles: (1) extract method for any block >10 lines, (2) replace magic numbers with named constants, (3) simplify conditionals using guard clauses, (4) reduce nesting to max 3 levels. Show the refactored code with comments explaining each change.
```

### 7. Design Pattern Suggester
```
I have this code structure in [LANGUAGE]:

[DESCRIBE OR PASTE CODE]

Problem: [WHAT'S WRONG — tight coupling, repeated logic, complex conditionals, etc.]. Suggest the most appropriate design pattern(s) to address this. For each pattern: (1) why it fits, (2) refactored code example, (3) tradeoffs. Prefer simplicity — don't over-engineer.
```

### 8. Legacy Code Modernization
```
Modernize this [LANGUAGE] code from [OLD VERSION/STYLE] to current best practices:

[PASTE CODE]

Apply: (1) modern language features (async/await, pattern matching, type hints, etc.), (2) current framework conventions, (3) updated API usage if deprecated calls are present. Preserve behavior — this is a refactor, not a rewrite. Flag any behavioral differences.
```

## Architecture & Design

### 9. API Endpoint Designer
```
Design a REST API for [RESOURCE/DOMAIN]. Requirements: [LIST OPERATIONS NEEDED]. Constraints: [AUTH METHOD, RATE LIMITS, etc.]. For each endpoint: HTTP method, path, request body schema, response schema, status codes, and error responses. Follow REST conventions and include pagination for list endpoints. Provide OpenAPI 3.0 YAML.
```

### 10. Database Schema Designer
```
Design a database schema for [APPLICATION/DOMAIN]. Entities: [LIST]. Relationships: [DESCRIBE]. Expected scale: [ROWS/QUERIES PER SEC]. Database: [POSTGRES/MYSQL/MONGO/etc.]. Provide: (1) table definitions with types and constraints, (2) indexes for common queries, (3) migration script, (4) query examples for top 5 use cases. Consider normalization vs. read performance.
```

### 11. System Architecture Reviewer
```
Review this system architecture for [APPLICATION]:

[DESCRIBE ARCHITECTURE — components, communication, data flow]

Evaluate: (1) scalability bottlenecks, (2) single points of failure, (3) data consistency risks, (4) operational complexity, (5) cost efficiency. For each issue found, suggest a fix with tradeoffs. Rate overall architecture maturity: MVP/Growth/Scale-ready.
```

### 12. Microservice Boundary Definer
```
I'm decomposing a [MONOLITH/APPLICATION] into microservices. Current modules: [LIST MODULES]. Data dependencies: [DESCRIBE]. Team structure: [DESCRIBE]. Help me define service boundaries using domain-driven design. For each proposed service: (1) bounded context, (2) owned data, (3) API surface, (4) inter-service communication pattern, (5) team ownership suggestion.
```

## Testing & Quality

### 13. Test Case Generator
```
Generate test cases for this [LANGUAGE] function:

[PASTE CODE]

Include: (1) happy path tests — normal inputs, expected outputs, (2) edge cases — boundary values, empty inputs, max values, (3) error cases — invalid inputs, null/undefined, type mismatches, (4) integration considerations. Format as [UNITTEST/PYTEST/JEST/etc.] test code ready to run.
```

### 14. Test Strategy Designer
```
Design a test strategy for [APPLICATION/FEATURE]. Architecture: [DESCRIBE]. CI/CD: [TOOL]. Current coverage: [%]. Create a testing pyramid with: (1) unit tests — what to cover, target count, (2) integration tests — critical paths, (3) E2E tests — user journeys, (4) performance tests — load targets, (5) security tests — OWASP top 10 coverage. Include a CI pipeline stage recommendation.
```

### 15. Mock & Stub Generator
```
Generate mocks/stubs for testing this [LANGUAGE] code:

[PASTE CODE — showing external dependencies]

For each external dependency (API, database, file system, etc.): (1) create a mock with configurable responses, (2) add assertion helpers to verify calls, (3) include failure simulation (timeout, error, empty response). Framework: [JEST/PYTEST/MOCKITO/etc.].
```

## DevOps & Deployment

### 16. Dockerfile Optimizer
```
Optimize this Dockerfile:

[PASTE DOCKERFILE]

Apply: (1) multi-stage build to reduce image size, (2) layer caching optimization for faster rebuilds, (3) security hardening (non-root user, minimal base image, no secrets in layers), (4) .dockerignore recommendations. Show the optimized Dockerfile with comments. Report expected size reduction.
```

### 17. CI/CD Pipeline Designer
```
Design a CI/CD pipeline for a [LANGUAGE] [APPLICATION TYPE] deployed to [TARGET — AWS/GCP/K8s/etc.]. Repo: [MONO/MULTI]. Team size: [NUMBER]. Include stages: lint, test, build, security scan, deploy (staging → production). Provide the pipeline config in [GITHUB ACTIONS/GITLAB CI/JENKINS] format with environment variables and secrets management.
```

### 18. Infrastructure as Code Template
```
Write [TERRAFORM/PULUMI/CDK] code to provision: [LIST INFRASTRUCTURE — e.g., VPC, ECS cluster, RDS, S3]. Region: [REGION]. Environment: [DEV/STAGING/PROD]. Requirements: [HIGH AVAILABILITY, COST OPTIMIZED, etc.]. Include: (1) resource definitions, (2) variables file, (3) outputs, (4) estimated monthly cost comment.
```

## Documentation

### 19. API Documentation Generator
```
Generate comprehensive API documentation for:

[PASTE CODE — route handlers/controllers]

For each endpoint: (1) description, (2) authentication requirements, (3) request parameters with types and validation rules, (4) request/response examples (JSON), (5) error responses, (6) rate limiting. Format as Markdown suitable for a docs site. Include a quick-start section with curl examples.
```

### 20. Architecture Decision Record (ADR)
```
Write an ADR for: [DECISION — e.g., "Use PostgreSQL over MongoDB for user data"]. Context: [WHY THIS DECISION CAME UP]. Options considered: [LIST WITH BRIEF DESCRIPTION]. Decision: [WHAT WE CHOSE]. Consequences: [POSITIVE AND NEGATIVE]. Follow the format: Title, Status, Context, Decision, Consequences, Compliance notes. Keep under 500 words.
```
