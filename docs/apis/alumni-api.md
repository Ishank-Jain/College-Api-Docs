
---

`docs/apis/alumni-api.md`
```md
# Alumni Community API

## Overview
The Alumni Community API covers support and community features such as FAQs, donations, student-alumni connections, messaging, and job opportunities.

## Base Path
`/api/v1`

## Purpose
- Provide FAQ support
- Handle alumni donations
- Allow student and alumni connection requests
- Support messaging between connected users
- Publish and view job opportunities with role-based access

## Supported Roles
- student
- alumni
- admin

## Authentication Type
Bearer JWT for protected routes

## Functional Areas
- FAQ
- Donations
- Connections
- Messaging
- Jobs

## Endpoints Summary

| Method | Endpoint | Description | Auth Required |
|---|---|---|---|
| GET | `/api/v1/faqs` | Get FAQs | No |
| POST | `/api/v1/donations` | Create donation | Yes |
| POST | `/api/v1/connections/request` | Send connection request | Yes |
| GET | `/api/v1/connections` | Get user connections | Yes |
| POST | `/api/v1/messages` | Send message | Yes |
| GET | `/api/v1/messages/thread/{id}` | Get message thread | Yes |
| GET | `/api/v1/jobs` | Get job opportunities | Yes |
| POST | `/api/v1/jobs` | Post a job opportunity | Yes |

## Endpoint Details

### 1. FAQs
**Endpoint:** `GET /api/v1/faqs`

**Use case:**  
Fetch common questions and answers for users.

### 2. Donations
**Endpoint:** `POST /api/v1/donations`

**Use case:**  
Create alumni donation entry.

**Role-based access**
- alumni and admin can create donations
- students can mainly view donation initiatives depending on platform policy

**Sample Request**
```json
{
  "amount": 5000,
  "purpose": "Scholarship Fund",
  "paymentMethod": "UPI"
}