
---

`docs/apis/mentorship-api.md`
```md
# Mentorship API

## Overview
The Mentorship API connects students with alumni mentors and manages mentorship requests.

## Base Path
`/api/v1/mentors` and `/api/v1/mentorship`

## Purpose
- View available mentors
- Request mentorship
- View mentorship requests
- Accept or reject mentorship requests

## Supported Roles
- student
- alumni
- admin

## Authentication Type
Bearer JWT

## Endpoints Summary

| Method | Endpoint | Description | Auth Required |
|---|---|---|---|
| GET | `/api/v1/mentors` | Get available mentors | Yes |
| POST | `/api/v1/mentorship/request` | Create mentorship request | Yes |
| GET | `/api/v1/mentorship/requests` | Get mentorship requests | Yes |
| PATCH | `/api/v1/mentorship/requests/{id}` | Update mentorship request status | Yes |

## Endpoint Details

### 1. Get Available Mentors
**Endpoint:** `GET /api/v1/mentors`

**Use case:**  
Fetch list of alumni available for mentorship.

### 2. Create Mentorship Request
**Endpoint:** `POST /api/v1/mentorship/request`

**Use case:**  
Student requests mentorship from an alumni mentor.

**Role-based access**
- only students can create mentorship requests
- alumni receive and manage requests

**Sample Request**
```json
{
  "mentorId": "m101",
  "topic": "Backend development guidance",
  "message": "I want mentorship on backend projects and interview prep."
}