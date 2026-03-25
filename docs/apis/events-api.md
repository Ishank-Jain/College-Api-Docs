
---

`docs/apis/events-api.md`
```md
# Events API

## Overview
The Events API manages alumni events and event registrations. It also includes an event notification webhook endpoint.

## Base Path
`/api/v1/events`

## Purpose
- View events
- Create events
- Fetch event details
- Register for events
- Receive webhook notifications for event-related updates

## Supported Roles
- student
- alumni
- admin

## Authentication Type
Bearer JWT for protected routes

## Endpoints Summary

| Method | Endpoint | Description | Auth Required |
|---|---|---|---|
| GET | `/api/v1/events` | Get all events | Yes |
| POST | `/api/v1/events` | Create event | Yes |
| GET | `/api/v1/events/{id}` | Get event by ID | Yes |
| POST | `/api/v1/events/{id}/register` | Register for event | Yes |
| POST | `/api/v1/webhooks/event-notification` | Receive event notification webhook | No |

## Endpoint Details

### 1. Get All Events
**Endpoint:** `GET /api/v1/events`

**Use case:**  
Fetch all events for the platform.

### 2. Create Event
**Endpoint:** `POST /api/v1/events`

**Use case:**  
Create a new event.

**Role-based access**
- alumni and admin can create events
- students can only view and register

**Sample Request**
```json
{
  "title": "Alumni Networking Meetup 2025",
  "description": "A networking event for alumni and students.",
  "type": "meetup",
  "mode": "offline",
  "dateTime": "2026-04-15T10:00:00Z",
  "venue": "College Auditorium",
  "organizer": "Alumni Association",
  "registrationDeadline": "2026-04-10T23:59:59Z"
}