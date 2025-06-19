# Copilot Coding Agent Instructions

## Overview
This project uses Copilot Coding Agent for code generation and automation. Please follow these conventions and requirements:

## Folder Structure & Technology
- **Backend:** Node.js, Express, TypeScript, Prisma, PostgreSQL
- **Frontend:** React (Vite), TypeScript

## Code Style
- Use [Prettier](https://prettier.io/) and [ESLint](https://eslint.org/) for formatting and linting.
- Use PascalCase for types and interfaces, camelCase for variables and functions.
- All new code must include type annotations.

## Testing
- Use Jest for all unit and integration tests.
- Write tests **before** implementing features (TDD).
- All PRs must include relevant tests and achieve >90% coverage.

## Prisma & Database
- All database changes must use Prisma migrations.
- Keep schema in `prisma/schema.prisma`.
- Add sample queries in README.

## Authentication
- Use Azure AD SSO (OAuth2/OpenID Connect).
- Store secrets using environment variables only.

## Pull Request Workflow
- All PRs must pass tests and linting.
- PR description must reference related tasks and acceptance criteria.
- Code review is mandatory.

## Acceptance Criteria
- Each feature/task must have clear Acceptance Criteria before implementation.

## API Specification & Documentation
- All REST API endpoints must be documented using OpenAPI (Swagger) specification.
- The OpenAPI spec file should be maintained at `openapi.yaml` or `docs/openapi.yaml`.
- Integrate Swagger UI (e.g., `swagger-ui-express`) to serve interactive documentation at `/api-docs`.
- Update the API spec whenever new endpoints are added or changed.
- Example requests, responses, enums, and error codes must match the actual implementation and Prisma schema.
- Document authentication methods (OAuth2/Azure AD) and all required headers or tokens.
- Reference the OpenAPI spec in the project README and keep it up-to-date.

## Branch Naming Convention
- Use the format `feature/<short-description>` for new features.
- Use `fix/<short-description>` for bug fixes.
- The <short-description> should be kebab-case, concise, and reflect the task (e.g., `feature/po-email-tracking`, `feature/prisma-schema-init`).
- Always create a new branch for each task.

## Example Acceptance Criteria
- API endpoint created with validation and error handling.
- Unit tests included and passing.
- All business rules implemented as described.
- API endpoint is documented and visible in Swagger UI.

## Security
- Validate all inputs.
- Mask sensitive fields as specified.

---

_See README for project-specific details._
