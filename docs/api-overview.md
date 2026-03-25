
```md
# docs/api-overview.md

# API Overview

This page provides a summary of all documented APIs in the College Alumni Application.

## API Summary Table

| API Name | Main Purpose | Spec File |
|---|---|---|
| Auth API | Signup, login, logout, current user | `openapi/auth-api.yaml` |
| Alumni Profile API | View and update alumni profile | `openapi/alumni-profile-api.yaml` |
| Directory API | Search and filter alumni | `openapi/directory-api.yaml` |
| Events API | Event listing, creation, registration, webhook | `openapi/events-api.yaml` |
| Mentorship API | Mentor listing and mentorship requests | `openapi/mentorship-api.yaml` |
| Alumni Community API | FAQs, donations, connections, messaging, jobs | `openapi/alumni-api.yaml` |

## API Design Principles Used
- OpenAPI 3.0.3
- `/api/v1` versioning
- JWT bearer authentication
- reusable schemas
- request/response examples
- standard error responses
- role-based access notes

## Roles Used Across APIs
- `student`
- `alumni`
- `admin`

## Grouping Logic
Instead of making too many tiny API files, related features were grouped into domain-level APIs:
- profile operations together
- directory operations together
- mentorship operations together
- community operations together

## Why this structure is good
- easier to manage
- cleaner Swagger rendering
- more professional documentation structure
- simple to maintain in development and release branches