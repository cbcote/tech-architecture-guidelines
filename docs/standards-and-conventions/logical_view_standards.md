# System Layers and Components

## Presentation Layer

### Responsibilities

- Implement user interface accessible through supported platforms.
- Collect data from Core Services and present to end user.
- Allow user to enter valid data into the system.
- Ensure user experience is in line with the organizational standards.

### Components

## Core Services Layer
- Implement core business logic.
- Provide CRUD API and business logic for domain entities modeled as RESTful resources.
- Services are consumed both by presentation layer and external systems.

## Infrastructure Layer

- Support other layers by centralizing implementation of cross-cutting concerns:
    - Security
    - Configuration
    - Monitoring
    - Caching
    - Messaging
    - Networking

## Integration Layer

- External services consumed by the application

