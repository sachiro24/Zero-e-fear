# ZERO FEAR – External Integrations

## 1. Overview

ZERO FEAR will use selected third-party services to provide AI image recognition, maps, route planning, charging station information, file storage and email notifications.

External services will primarily be accessed through the Django backend to protect API credentials and centralize business logic.

## 2. Planned Integrations

### 2.1 AI Vision API

**Purpose:** Dashboard image recognition.

Responsibilities:

- Analyze uploaded EV dashboard photos.
- Extract battery percentage.
- Extract displayed remaining range.
- Extract odometer readings when visible.
- Return structured information for backend validation.

**Priority:** Core MVP integration.

Possible provider: OpenAI vision-capable API or another suitable vision provider. Final selection requires evaluation.

### 2.2 Maps and Routing API

**Possible providers:** Google Maps Platform or Mapbox.

Responsibilities:

- Display interactive maps.
- Search locations.
- Calculate routes.
- Estimate travel distance and duration.
- Support future EV trip planning and charging-stop suggestions.

**Priority:** Subsequent MVP stage.

### 2.3 Charging Station Data

Possible sources:

- Charging network provider APIs.
- Public charging station datasets.
- Manually curated station information.

Responsibilities:

- Store charging station locations.
- Display connector types.
- Display charging power.
- Display prices where available.
- Display live availability only when supported by a reliable data provider.

**Priority:** Subsequent MVP stage.

### 2.4 Image and File Storage

**Possible provider:** Amazon S3 or compatible object storage.

Responsibilities:

- Store dashboard images.
- Provide controlled access to uploaded files.
- Support future marketplace listing images.

Requirements:

- Private storage for personal dashboard images.
- Access control.
- File type and size validation.
- Appropriate retention and deletion policies.

**Priority:** Needed for scanner workflow.

### 2.5 Email Service

**Possible providers:** Brevo or Amazon SES.

Responsibilities:

- Email verification.
- Password-reset emails.
- Important account notifications.

**Priority:** Optional for initial prototype.

## 3. Integration Architecture

The general integration flow:

1. React Native sends a request to Django.
2. Django validates the request.
3. Django communicates with the relevant external provider.
4. The external provider returns a response.
5. Django processes and validates the response.
6. Django returns the required information to React Native.

Private API credentials must remain on the backend.

## 4. Integration Priorities

| Integration | Priority | Development stage |
|---|---|---|
| Vision API | High | Initial MVP |
| Image storage | High | Initial MVP |
| Maps and routing | Medium | Subsequent MVP |
| Charging station data | Medium | Subsequent MVP |
| Email service | Optional | Later implementation |

## 5. Important Technical Considerations

- Review provider pricing and usage limits before selection.
- Protect API keys using backend environment variables.
- Handle external API failures and network interruptions.
- Avoid unnecessary requests to paid services.
- Cache suitable data where appropriate.
- Check service availability and regional coverage.
- Do not promise live charging availability without a reliable data source.
- Keep integrations replaceable where practical.

## 6. Decisions Still Required

The following provider choices must be confirmed before implementation:

- Vision API provider.
- Maps and routing provider.
- Image storage provider.
- Charging station data source.
- Email service provider.

## 7. Summary

ZERO FEAR will initially prioritize AI dashboard scanning and secure image storage.

Maps, routing and charging station integrations will be introduced as the trip-planning and charging-discovery modules are implemented.

Provider selection will consider cost, reliability, API capabilities and availability in Sri Lanka.
