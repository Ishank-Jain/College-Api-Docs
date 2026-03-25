# Auth API

## Overview
The Auth API handles user registration, login, logout, and fetching the currently authenticated user for the College Alumni platform.

## Base Path
`/api/v1/auth`

## Purpose
- Register new users
- Authenticate users
- Issue JWT-based access tokens
- Protect secured endpoints using bearer authentication

## Supported Roles
- student
- alumni
- admin

## Authentication Type
Bearer JWT

## Endpoints Summary

| Method | Endpoint | Description | Auth Required |
|---|---|---|---|
| POST | `/api/v1/auth/signup` | Register a new user | No |
| POST | `/api/v1/auth/login` | Login and get JWT token | No |
| POST | `/api/v1/auth/logout` | Logout current user | Yes |
| GET | `/api/v1/auth/me` | Get current logged-in user | Yes |

## Endpoint Details

### 1. Signup
**Endpoint:** `POST /api/v1/auth/signup`

**Use case:**  
Register a student, alumni, or admin account.

**Sample Request**
```json
{
  "fullName": "Ishan Jain",
  "email": "ishan.alumni@example.com",
  "password": "Password@123",
  "role": "alumni",
  "batchYear": 2022,
  "department": "Computer Science"
}