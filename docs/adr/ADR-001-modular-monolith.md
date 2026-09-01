# ADR-001: Use Modular Monolith Architecture

## Status

Accepted

## Context

The Expense Tracker SaaS needs a production-oriented architecture
while keeping the initial system manageable.

## Decision

We will initially implement the backend as a modular monolith.

Business capabilities will be separated into modules:

- Identity
- Tenants
- Accounts
- Categories
- Transactions
- Budgets
- Reports

Each module will have clear Domain, Application,
Infrastructure, and API boundaries.

## Consequences

### Positive

- Easier development
- Simpler deployment
- Lower infrastructure complexity
- Clear business boundaries
- Easier future extraction into microservices

### Negative

- Modules share the same deployment
- Some runtime isolation is lost compared with microservices