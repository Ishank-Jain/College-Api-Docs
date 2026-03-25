# docs/authentication.md

# Authentication

This project uses **Bearer JWT authentication** for protected API endpoints.

## Authentication Flow
1. User signs up using Auth API
2. User logs in with email and password
3. Backend returns JWT token
4. Token is used in protected API requests

## Authorization Header Format
```http
Authorization: Bearer <jwt-token>