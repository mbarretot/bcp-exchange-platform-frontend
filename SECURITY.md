# Security Policy

## Scope

This repository is a portfolio implementation of a technical challenge and is not a production banking application. Do not use real customer data, production credentials, privileged Azure Functions keys, or reusable secrets when running it.

## Reporting a vulnerability

Please avoid publishing exploitable details in a public issue. Report security concerns privately to the repository owner through GitHub's private vulnerability-reporting feature when it is enabled.

Include the affected component, reproduction steps, expected impact, and any suggested mitigation. Do not test against systems or accounts you do not own or have explicit permission to assess.

## Configuration guidance

- Treat every value compiled into Angular environment files as publicly visible.
- Keep tenant credentials, client secrets, Terraform state credentials, and deployment tokens outside the repository.
- Enforce authorization in the backend; route guards and hidden controls are user-experience measures, not security boundaries.
- Validate access-token issuer, audience, signature, lifetime, and scopes or roles at the API boundary.
- Rotate any credential immediately if it is accidentally committed or exposed in a build artifact.
