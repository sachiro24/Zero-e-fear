# ZERO FEAR – Technical Decisions

## 1. Project Overview

ZERO FEAR is an AI-assisted electric vehicle ecosystem application initially targeting Android users in Sri Lanka.

The platform aims to combine EV management, dashboard reading recognition, vehicle insights, charging discovery, trip planning and an EV marketplace.

This document records the main technical decisions for the initial development.

## 2. Technology Stack

### 2.1 Mobile Application

**Selected technologies:**

- React Native
- Expo
- TypeScript

**Reasons:**

- Supports Android and iOS development.
- Allows reuse of React knowledge.
- Expo simplifies development and testing.
- TypeScript improves code reliability and maintainability.

**Initial target:** Android.

### 2.2 Backend

**Selected technologies:**

- Python
- Django
- Django REST Framework

**Reasons:**

- Django provides a structured backend framework.
- Django REST Framework simplifies REST API development.
- Python supports AI and data-processing integrations.
- Django provides built-in authentication and database functionality.

### 2.3 Database

**Selected technologies:**

- PostgreSQL
- PostGIS

**Reasons:**

- PostgreSQL provides relational data management.
- Supports relationships between users, vehicles, readings and trips.
- PostGIS supports geographical queries.
- Suitable for future charging station discovery and location-based functionality.

### 2.4 AI Integration

**Selected approach:** Vision-capable AI API accessed through the Django backend.

**Purpose:**

- Recognize dashboard information.
- Extract battery percentage.
- Extract displayed remaining range.
- Extract odometer readings when visible.

AI-extracted information must be reviewed and confirmed by the user before being saved as a confirmed vehicle reading.

### 2.5 Development Tools

- Google Antigravity for AI-assisted development.
- Git for version control.
- GitHub for source code and documentation.
- Android Studio for emulator testing.
- Google Stitch for UI design.

## 3. Application Architecture

ZERO FEAR will follow a client-server architecture.

### Frontend

React Native application responsible for:

- User interface.
- Navigation.
- Camera access.
- User input.
- Displaying API responses.

### Backend

Django REST Framework responsible for:

- Authentication and authorization.
- Business logic.
- API endpoints.
- Database operations.
- AI and external service integrations.

### Database

PostgreSQL responsible for storing:

- User accounts.
- Vehicle models.
- Registered vehicles.
- Dashboard scans.
- Confirmed readings.
- Trips.
- Future charging and marketplace information.

## 4. Architecture Decisions

| ID | Decision |
|---|---|
| TD-01 | Use React Native with Expo for mobile development |
| TD-02 | Use TypeScript for frontend development |
| TD-03 | Use Django and Django REST Framework for the backend |
| TD-04 | Use PostgreSQL with PostGIS for data storage and geographical functionality |
| TD-05 | Use REST APIs for frontend-backend communication |
| TD-06 | Use JWT-based authentication |
| TD-07 | Access external AI services through the backend |
| TD-08 | Require user confirmation before saving AI-extracted readings |
| TD-09 | Support manual dashboard reading entry as an alternative |
| TD-10 | Prioritize Android for the initial release |

## 5. Application Navigation Decisions

The main bottom navigation will contain five tabs:

1. Home
2. Insights
3. Plan
4. Discover
5. Profile

My Garage will be accessible through Home and Profile rather than a separate bottom navigation tab.

Discover will contain charging station discovery and EV marketplace functionality.

The AI Assistant floating shortcut is planned for a later stage.

## 6. Security Decisions

- Use Django authentication and JWT.
- Use HTTPS in production.
- Store mobile authentication tokens using Expo SecureStore.
- Apply backend ownership and permission checks.
- Keep private API credentials on the backend.
- Validate incoming data and uploaded files.
- Protect private dashboard images.

## 7. External Integration Decisions

| Integration | Planned purpose |
|---|---|
| Vision API | Dashboard image recognition |
| Maps and routing API | Maps and trip planning |
| Charging data provider | Charging station information |
| Object storage | Dashboard and marketplace images |
| Email provider | Verification and password recovery |

Specific providers will be selected after evaluating pricing, availability and technical requirements.

## 8. Development Priorities

### Initial MVP

- Authentication.
- Vehicle management.
- Home dashboard.
- Manual dashboard readings.
- AI scanner prototype.
- Reading confirmation.
- Reading history.
- Basic insights.

### Subsequent Development

- Charging station discovery.
- Trip planning.
- Journey history.
- Marketplace browsing.

### Future Development

- AI EV Assistant.
- Advanced battery analytics.
- EV ownership cost comparisons.
- Rewards and eco-driving.
- Connected vehicle integrations.
- Marketplace seller functionality.

## 9. Technical Decision Review

These decisions provide the initial technical direction for ZERO FEAR.

Changes may be made when implementation reveals a genuine technical limitation, cost issue or better alternative. Significant changes should be documented with their reasoning.

## 10. Summary

ZERO FEAR will use React Native, Expo and TypeScript for its mobile application, Django REST Framework for its backend, and PostgreSQL with PostGIS for its database.

The architecture will prioritize modular development, secure communication, maintainability and future expansion of the EV ecosystem.
