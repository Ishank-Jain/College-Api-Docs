
```md
# docs/environments.md

# Environments

This page describes the environments used in the documentation and deployment process.

## Main Environments

| Environment | Purpose | Example Base URL |
|---|---|---|
| Local | Development and testing on local machine | `http://localhost:3000` |
| Staging | Preview environment for testing docs and APIs | `https://staging.example.com` |
| Production | Released and published environment | `https://api.example.com` |

## Documentation Environment Mapping

| Branch | Environment | Purpose |
|---|---|---|
| `develop-docs` | Staging/Internal Preview | Draft and under-development APIs |
| `release-docs` | Production/Published Docs | Stable and released API docs |

## Why environment separation matters
- draft APIs should not be confused with released APIs
- testing can happen safely before public publishing
- version comparison becomes easier

## Current Server Configuration
In the OpenAPI files, the current default server is:
```text
http://localhost:3000