# ZERO FEAR – AI Dashboard Scanner Workflow

## 1. Overview

The AI Dashboard Scanner allows users to capture an image of their EV dashboard and automatically extract important vehicle information.

The initial implementation focuses on:

- Battery percentage (State of Charge / SOC)
- Displayed remaining range (km)
- Odometer reading (km), when visible

The user must review and confirm extracted information before it is saved as a confirmed vehicle reading.

## 2. Technology

- Mobile application: React Native, Expo and TypeScript
- Backend: Python, Django and Django REST Framework
- Database: PostgreSQL
- Image analysis: Vision-capable API accessed through the Django backend
- Image storage: Private file storage

## 3. Scanner Workflow

### Step 1 – Open Scanner

The user opens the dashboard scanner from the Home screen.

### Step 2 – Capture Dashboard Image

The application opens the camera and allows the user to capture their EV dashboard.

The application should provide guidance for capturing a clear and readable image.

### Step 3 – Upload Image

The mobile application uploads the image to the Django backend using a secure API request.

The backend validates the file type and file size.

### Step 4 – AI Image Analysis

The Django backend sends the image to the configured Vision API.

The AI service attempts to extract:

- Battery percentage
- Displayed remaining range
- Odometer reading

### Step 5 – Process AI Response

The backend validates and normalizes the extracted information.

Values that are not visible or cannot be reliably identified should be returned as null rather than guessed.

An example structured extraction result:

```json
{
  "battery_percentage": 78,
  "displayed_range_km": 320,
  "odometer_km": 24560,
  "confidence": {
    "battery_percentage": "high",
    "displayed_range_km": "high",
    "odometer_km": "medium"
  }
}
```

This is a proposed application response format, not a guaranteed Vision API response.

### Step 6 – User Review

The application displays extracted values to the user.

The user can:

- Review extracted information.
- Correct incorrect values.
- Enter missing values manually.
- Cancel the scan.

### Step 7 – Confirm and Save

After confirmation, Django validates the submitted values and creates a confirmed Vehicle Reading record.

The Dashboard Scan record is updated to reflect its confirmed status.

### Step 8 – Update Application

The confirmed reading becomes available for:

- Home dashboard
- Battery reading history
- Insights
- Vehicle logbook

## 4. System Architecture

The workflow follows this sequence:

1. React Native captures the dashboard image.
2. React Native uploads the image to Django.
3. Django validates and stores the scan record.
4. Django sends the image to the Vision API.
5. The Vision API returns extracted information.
6. Django processes and stores the extraction result.
7. React Native displays the result for review.
8. The user confirms the information.
9. Django creates a confirmed Vehicle Reading record.
10. The mobile application refreshes relevant dashboard information.

## 5. Database Integration

### DashboardScans

Stores information about dashboard scanning attempts.

Proposed fields:

- id
- user_vehicle_id
- image_reference
- extracted_data
- status
- created_at
- confirmed_at

Possible statuses:

- pending
- pending_review
- confirmed
- failed

### VehicleReadings

Stores confirmed dashboard readings.

Proposed fields:

- id
- user_vehicle_id
- battery_percentage
- displayed_range_km
- odometer_km
- source
- recorded_at
- created_at

Possible reading sources:

- AI
- Manual

Only confirmed readings should be used in normal insights and reading history.

## 6. API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/v1/scans/` | Upload image and initiate scanning |
| GET | `/api/v1/scans/{id}/` | Retrieve scan status and extracted values |
| POST | `/api/v1/scans/{id}/confirm/` | Confirm reviewed values and save reading |
| POST | `/api/v1/readings/` | Save manually entered reading |
| GET | `/api/v1/vehicles/{id}/readings/` | Retrieve confirmed reading history |

## 7. Error Handling

The application should handle:

- Blurry or unreadable dashboard images.
- Missing dashboard values.
- Incorrect AI extraction.
- Vision API failures.
- Network interruptions.
- Invalid reading values.
- Image upload failures.
- Duplicate submissions.

A manual reading entry option should remain available if AI scanning fails.

## 8. Security and Privacy

- Validate image formats and file sizes.
- Use HTTPS for image uploads.
- Restrict access to private dashboard images.
- Protect Vision API credentials using backend environment variables.
- Apply user ownership checks.
- Avoid unnecessary retention of uploaded dashboard images.
- Do not treat unconfirmed AI results as verified vehicle readings.

## 9. Important Data Distinctions

The displayed remaining range is the estimate shown by the vehicle dashboard.

It should not be treated as the actual achievable driving range or actual energy efficiency.

Battery percentage represents the displayed State of Charge.

AI confidence information should be treated as an indicator, not a guarantee of correctness.

## 10. Implementation Priority

1. Camera capture.
2. Image upload.
3. Vision API integration.
4. Structured extraction.
5. Review and correction screen.
6. User confirmation.
7. Save confirmed reading.
8. Reading history integration.

## 11. Summary

The ZERO FEAR AI Dashboard Scanner connects mobile image capture, backend processing, AI-based extraction and user confirmation.

The user remains responsible for approving the extracted information before it becomes a confirmed vehicle reading.
