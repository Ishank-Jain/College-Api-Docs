
```md
# docs/swagger-ui.md

# Swagger UI

Swagger UI is used in this project to render OpenAPI specifications as interactive API documentation.

## Why Swagger UI is used
- interactive endpoint testing
- request and response visualization
- grouped APIs using tags
- quick validation of API structure

## What Swagger shows well
- paths
- methods
- request bodies
- query parameters
- path parameters
- responses
- authentication requirements

## Swagger Strengths in this Project
- endpoints grouped using tags
- request/response examples visible
- reusable schemas rendered cleanly
- bearer JWT security shown
- error responses displayed properly

## Difference Between Swagger and Redoc

| Tool | Main Use |
|---|---|
| Swagger UI | interactive API testing and exploration |
| Redoc | clean and polished reference rendering |
| MkDocs | full project documentation portal |

## Recommended Demo Use
During presentation:
1. open Swagger UI
2. show grouped APIs
3. open one endpoint
4. show schema reuse
5. show bearer auth
6. show error responses
7. show `/api/v1` versioning in paths