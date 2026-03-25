
---

`docs/apis/alumni-profile-api.md`
```md
# Alumni Profile API

## Overview
The Alumni Profile API manages alumni profile viewing and profile updates.

## Base Path
`/api/v1/profile`

## Purpose
- View alumni profile by ID
- View own profile
- Update own profile
- Maintain alumni academic and professional details

## Supported Roles
- alumni
- admin
- student (view access only where allowed)

## Authentication Type
Bearer JWT

## Endpoints Summary

| Method | Endpoint | Description | Auth Required |
|---|---|---|---|
| GET | `/api/v1/profile/me` | Get current user's profile | Yes |
| GET | `/api/v1/profile/{id}` | Get alumni profile by ID | Yes |
| PATCH | `/api/v1/profile/{id}` | Update alumni profile | Yes |

## Endpoint Details

### 1. Get My Profile
**Endpoint:** `GET /api/v1/profile/me`

**Use case:**  
Returns the current logged-in user's profile.

**Sample Response**
```json
{
  "id": "a101",
  "fullName": "Ishan Jain",
  "email": "ishan.alumni@example.com",
  "role": "alumni",
  "batchYear": 2022,
  "department": "Computer Science",
  "company": "HPE",
  "jobTitle": "Software Engineer Intern",
  "location": "Bangalore",
  "skills": ["Node.js", "MongoDB", "Docker"],
  "bio": "Passionate alumni helping students with mentorship and referrals."
}