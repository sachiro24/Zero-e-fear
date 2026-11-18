# ZERO FEAR – API Specification

## 1. Overview

The React Native application communicates with the Django REST Framework backend through REST APIs.

- Communication: HTTPS
- Data format: JSON
- Authentication: Bearer JWT tokens
- Example development base URL: `http://localhost:8000/api/v1/`

The production API must use HTTPS.

## 2. API Conventions

- Use plural resource names where appropriate.
- Use HTTP methods consistently.
- Validate all request data on the backend.
- Require authentication for private resources.
- Verify resource ownership.
- Return consistent error responses.
- Use pagination for potentially large collections.

## 3. Authentication Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/auth/register/` | Register a new user |
| POST | `/auth/login/` | Authenticate a user |
| POST | `/auth/refresh/` | Refresh access token |
| GET | `/auth/me/` | Retrieve current user profile |

## 4. Vehicle Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/vehicles/` | List user's vehicles |
| POST | `/vehicles/` | Register a vehicle |
| GET | `/vehicles/{id}/` | Retrieve vehicle details |
| PATCH | `/vehicles/{id}/` | Update vehicle information |
| DELETE | `/vehicles/{id}/` | Remove a vehicle |
| GET | `/vehicle-models/` | Browse supported EV models |

## 5. Dashboard Scan and Reading Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/scans/` | Upload dashboard image and initiate scanning |
| GET | `/scans/{id}/` | Retrieve scan status and extracted data |
| POST | `/scans/{id}/confirm/` | Confirm reviewed values and save a reading |
| POST | `/readings/` | Save a manually entered reading |
| GET | `/vehicles/{id}/readings/` | Retrieve confirmed reading history |
| GET | `/vehicles/{id}/latest-reading/` | Retrieve latest confirmed reading |

Image uploads use `multipart/form-data`. Normal data requests use JSON.

AI-extracted values must be reviewed and confirmed by the user before becoming confirmed reading records.

## 6. Trip Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/trips/` | Save a trip |
| GET | `/trips/` | List user's trips |
| GET | `/trips/{id}/` | Retrieve trip details |

## 7. Future Charging Endpoints

- `GET /charging-stations/`
- `GET /charging-stations/{id}/`
- `POST /charging-sessions/`
- `GET /charging-sessions/`

## 8. Future Insights Endpoints

- `GET /insights/overview/`
- `GET /insights/efficiency/`
- `GET /insights/battery/`

## 9. Future Marketplace Endpoints

- `GET /marketplace/listings/`
- `GET /marketplace/listings/{id}/`
- `POST /marketplace/favourites/`

## 10. HTTP Status Codes

| Code | Meaning |
|---|---|
| 200 | Request successful |
| 201 | Resource created |
| 204 | Successful request with no response body |
| 400 | Invalid request data |
| 401 | Authentication required or invalid |
| 403 | Permission denied |
| 404 | Resource not found |
| 500 | Internal server error |

## 11. Example Vehicle Creation Request

```http
POST /api/v1/vehicles/
Authorization: Bearer <access_token>
Content-Type: application/json
```

```json
{
  "vehicle_model_id": "model-uuid",
  "registration_number": "ABC-1234",
  "is_primary": true
}
```

The backend must verify that the vehicle model exists and that the authenticated user is creating a vehicle under their own account.

## 12. Security Requirements

- Require authentication for private endpoints.
- Verify resource ownership.
- Validate incoming data.
- Use Django password hashing.
- Use HTTPS in production.
- Keep secret API keys on the backend.
- Restrict uploaded file types and sizes.

## 13. Implementation Note

This is the proposed API contract. Request fields, response structures and endpoint names may be refined during implementation.

Keep frontend and backend contracts synchronized.
