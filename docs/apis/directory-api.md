
---

`docs/apis/directory-api.md`
```md
# Directory API

## Overview
The Directory API provides alumni search and filtering capabilities for students, alumni, and admins.

## Base Path
`/api/v1/directory`

## Purpose
- View alumni directory
- Search alumni by keyword
- Filter alumni using company, batch year, department, location, and mentorship availability

## Supported Roles
- student
- alumni
- admin

## Authentication Type
Bearer JWT

## Endpoints Summary

| Method | Endpoint | Description | Auth Required |
|---|---|---|---|
| GET | `/api/v1/directory` | Get paginated directory | Yes |
| GET | `/api/v1/directory/search` | Search alumni by keyword | Yes |
| GET | `/api/v1/directory/filter` | Filter alumni using multiple query params | Yes |

## Endpoint Details

### 1. Get Directory
**Endpoint:** `GET /api/v1/directory`

**Use case:**  
Fetch the alumni directory in paginated form.

**Query Parameters**
- `page`
- `limit`

**Sample Response**
```json
{
  "total": 1,
  "page": 1,
  "limit": 10,
  "results": [
    {
      "id": "a101",
      "fullName": "Ishan Jain",
      "batchYear": 2022,
      "department": "Computer Science",
      "company": "HPE",
      "location": "Bangalore",
      "willingToMentor": true
    }
  ]
}