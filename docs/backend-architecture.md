# ZERO FEAR – Backend Architecture

## 1. Overview

The ZERO FEAR backend will use Python, Django and Django REST Framework.

It exposes REST APIs to the React Native application, manages business logic, validates data, enforces permissions and communicates with PostgreSQL and external providers.

## 2. Backend Responsibilities

- User registration, login and authentication.
- Vehicle catalogue and registered vehicle management.
- Dashboard scan processing and confirmed readings.
- Trip records and future trip-planning services.
- Insights data aggregation.
- Future charging and marketplace functionality.
- External AI, maps, storage and email integrations.

## 3. Proposed Django Project Structure

```text
backend/
├── config/
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
├── apps/
│   ├── accounts/
│   ├── vehicles/
│   ├── readings/
│   ├── trips/
│   ├── insights/
│   ├── charging/
│   └── marketplace/
├── integrations/
│   ├── vision/
│   ├── maps/
│   ├── storage/
│   └── email/
├── common/
│   ├── permissions.py
│   ├── exceptions.py
│   └── utilities.py
├── manage.py
└── requirements.txt
```

## 4. Django App Responsibilities

| App | Responsibility |
|---|---|
| accounts | User model, registration, authentication and profile |
| vehicles | Vehicle catalogue and user's registered vehicles |
| readings | Dashboard scans, extraction results and confirmed readings |
| trips | Trip records and trip-related operations |
| insights | Aggregation of readings and trip information |
| charging | Charging station and session functionality in a later stage |
| marketplace | EV listings and favourites in a later stage |

## 5. Typical Django Request Flow

1. A request reaches a Django URL.
2. The URL routes it to the appropriate view.
3. Authentication and permission checks are applied.
4. A serializer validates incoming data.
5. The view calls application or domain logic.
6. Django ORM reads or writes database records.
7. A serializer formats the response.
8. Django returns a JSON response.

Complex business logic and external API calls should be kept out of large view functions and placed in suitable service modules.

## 6. Database Access

Use Django ORM with PostgreSQL.

Define foreign keys, constraints and indexes as appropriate. Use PostGIS for geographical functionality when required.

A custom Django user model should be selected at the beginning of the project, before creating the initial migrations.

## 7. Authentication and Permissions

- Use Django authentication with JWT support through Django REST Framework Simple JWT.
- Protect private endpoints.
- Check resource ownership for vehicles, readings and trips.
- Never rely on frontend checks alone.
- Store secrets in environment variables.

## 8. External Integrations

Create isolated backend service modules for:

- Vision API.
- Maps and routing.
- Private image storage.
- Email delivery.
- Charging station data providers.

The mobile app should communicate with Django rather than calling private third-party services directly.

## 9. Error Handling and Validation

- Use serializers to validate request data.
- Return consistent HTTP status codes and JSON errors.
- Handle external provider timeouts and failures.
- Log useful diagnostic information without exposing secrets or sensitive user data.
- Validate uploaded file types and sizes.

## 10. Implementation Priority

Initial backend priorities:

1. Project configuration and database connection.
2. Custom user model and authentication.
3. Vehicle catalogue and vehicle management.
4. Dashboard scan and reading APIs.
5. Trip records.
6. Permissions, validation and automated tests.

Charging and marketplace backend functionality can follow after the core MVP.
