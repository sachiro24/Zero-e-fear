# ZERO FEAR – Application Structure

## 1. Overview

ZERO FEAR is a personal EV intelligence platform initially targeting electric vehicle owners in Sri Lanka.

The application aims to provide a connected experience for EV ownership through vehicle intelligence, battery reading management, charging discovery, battery-aware trip planning, driving insights and EV-related services.

The mobile application follows a five-tab bottom navigation structure to organise its main features and provide a consistent user experience.

The application is planned as an Android-first mobile application, with the possibility of supporting iOS in a later release.

## 2. Main Application Navigation

The application consists of five primary navigation modules:

1. Home
2. Insights
3. Plan
4. Discover
5. Profile

## 3. Main Application Modules

### 3.1 Home

**Purpose:** Provide a personalised overview of the user's electric vehicle and quick access to important features.

**Main functions:**
- Display the selected primary vehicle.
- Show the latest confirmed battery percentage.
- Display the displayed remaining driving range.
- Access the AI Dashboard Scanner.
- Provide a driving efficiency summary.
- Display recent journeys and vehicle activity.
- Access My Garage.
- Provide shortcuts to Trip Planning.
- Provide shortcuts to Charging Discovery.

**Main screens:**
- Home Dashboard.
- Dashboard Scanner.
- Review Extracted Readings.
- Scan Success.

### 3.2 Insights

**Purpose:** Help users understand their vehicle's real-world performance and historical activity.

**Main functions:**
- View battery reading history.
- Monitor battery percentage trends.
- Review recorded journey distances.
- View driving efficiency information.
- Review charging history.
- Access individual historical records.
- View consolidated vehicle activity.

**Main screens:**
- Insights Dashboard.
- Battery Reading History.
- Battery Reading Details.
- Journey History.
- Journey Details.
- Charging History.
- Charging Session Details.
- Full Vehicle Logbook.

### 3.3 Plan

**Purpose:** Help users plan journeys using EV-specific information and estimated battery requirements.

**Main functions:**
- Select starting location.
- Select destination.
- Select registered vehicle.
- Enter or confirm current battery percentage.
- Calculate estimated energy consumption.
- Predict arrival battery percentage.
- Recommend charging stops when necessary.
- Compare alternative routes.
- Display estimated journey costs where sufficient information is available.

**Main screens:**
- Journey Setup.
- Route Analysis.
- Route Alternatives.
- Active Navigation.

Charging stop recommendations are presented as part of the route planning experience rather than requiring a separate primary navigation module.

### 3.4 Discover

**Purpose:** Help users discover EV-related locations, charging infrastructure and marketplace services.

Discover contains two main areas.

#### A. Charging Discovery

**Main functions:**
- Interactive charging station map.
- Search for charging stations.
- Filter charging stations.
- View charging station details.
- Review connector compatibility.
- View charging power and pricing.
- Review available station facilities.
- Access navigation directions.

**Main screens:**
- Charging Station Map.
- Charging Station Details.

#### B. EV Marketplace

**Main functions:**
- Browse electric vehicle listings.
- Search and filter listings.
- View vehicle photographs.
- Review vehicle specifications.
- View vehicle prices and conditions.
- Access seller information.
- Contact sellers.
- Save favourite listings.

**Main screens:**
- Marketplace Home.
- Vehicle Listing Details.

Live charging availability, reservations and marketplace transactions depend on appropriate external integrations and backend functionality.

### 3.5 Profile

**Purpose:** Allow users to manage their accounts, registered vehicles and application preferences.

**Main functions:**
- View and manage personal information.
- Access My Garage.
- Manage account settings.
- Configure notification preferences.
- Change application theme.
- Manage privacy and security settings.
- Access Help and Support.
- Log out.

**Main screens:**
- Profile and Settings.

## 4. Additional Application Modules

The following modules support the main navigation sections.

### 4.1 My Garage

Allows users to register and manage their electric vehicles.

Main functions:
- Add a new vehicle.
- View registered vehicles.
- Select a primary vehicle.
- View vehicle details.
- Edit vehicle information.

### 4.2 Add Vehicle

Allows users to register an electric vehicle by selecting:
- Manufacturer.
- Model.
- Variant.
- Model year.

The registration process includes vehicle selection, vehicle confirmation and registration success.

### 4.3 AI Dashboard Scanner

Uses image processing to extract useful information from EV dashboard photographs.

Main functions:
- Capture dashboard photographs.
- Extract battery percentage.
- Extract displayed remaining range when visible.
- Extract odometer information when visible.
- Allow users to review and correct extracted values.
- Save confirmed readings.

Manual reading entry is available as an alternative.

### 4.4 Vehicle Reading Management

Maintains historical dashboard readings.

Main functions:
- Store confirmed battery readings.
- Record reading date and time.
- Identify the reading source.
- Display historical readings.
- Provide access to individual reading details.

### 4.5 Vehicle Activity Management

Organises available vehicle activity records.

Main functions:
- Maintain journey records.
- Maintain charging session records.
- Provide historical activity information.
- Support the Full Vehicle Logbook.

## 5. User Onboarding Structure

### New User Journey

1. Splash Screen.
2. Welcome and Onboarding.
3. User Registration.
4. Email Verification, if implemented.
5. Add Electric Vehicle.
6. Vehicle Selection.
7. Vehicle Confirmation.
8. Dashboard Scanner.
9. Review Extracted Readings.
10. Confirm and Save.
11. Home Dashboard.

Users should have the option to skip the initial dashboard scan and enter readings manually or later.

### Returning User Journey

1. Splash Screen.
2. Login.
3. Authentication.
4. Home Dashboard.

Users without a registered vehicle should be directed to vehicle registration.

Returning users with an existing vehicle should not be forced to repeat vehicle registration or dashboard scanning.

## 6. Application Navigation Design

The five primary navigation tabs provide access to the main application modules.

| Navigation Tab | Main Module | Supporting Features |
|---|---|---|
| Home | Vehicle Overview | Dashboard Scanner, My Garage, Quick Actions |
| Insights | Vehicle Intelligence | Battery History, Journey History, Charging History, Logbook |
| Plan | Trip Planning | Route Analysis, Alternatives, Charging Stops, Navigation |
| Discover | EV Discovery | Charging Stations, Marketplace |
| Profile | Account Management | Settings, Preferences, My Garage, Support |

My Garage is accessible through Home and Profile rather than being a separate bottom navigation tab.

## 7. Future Application Modules

The following capabilities may be introduced in future releases:

### AI EV Assistant
Provides an AI-powered conversational assistant for EV-related questions and vehicle information.

### Rewards and Achievements
Encourages efficient driving through achievements and reward mechanisms.

### Advanced Vehicle Analytics
Provides more detailed analysis of driving patterns, vehicle efficiency and battery performance.

### Marketplace Seller Management
Allows users to create, manage and maintain EV marketplace listings.

These modules are part of the longer-term product direction and should not be treated as completed MVP functionality.

## 8. Application Design Principles

- Maintain consistent five-tab bottom navigation.
- Keep each screen focused on one primary purpose.
- Avoid unnecessary information and interface elements.
- Use progressive disclosure for advanced information.
- Maintain consistent UI components across modules.
- Prioritise simple and intuitive interactions.
- Clearly distinguish confirmed records from estimated information.
- Provide appropriate loading, error, empty and success states.
- Support different mobile screen sizes.

## 9. Technology Direction

The planned application technology stack is:

| Layer | Technology |
|---|---|
| Mobile Application | React Native |
| Mobile Framework | Expo |
| Programming Language | TypeScript |
| Backend | Python |
| Backend Framework | Django |
| API Development | Django REST Framework |
| Database | PostgreSQL |
| Geospatial Database Support | PostGIS |
| AI Image Processing | Vision API through the backend |

The mobile application communicates with the backend through REST APIs.

The backend manages application data, authentication, vehicle records, trip information and integrations with external services.

AI image-processing requests are handled through the backend rather than exposing API credentials directly in the mobile application.

## 10. Implementation Status

This document describes the planned logical application structure and module organisation of ZERO FEAR.

The UI/UX concepts are being developed using Google Stitch.

The mobile application, backend services, database and external integrations will be implemented during the subsequent development phases.

The presence of a module in this document does not indicate that its functionality has already been implemented or integrated.
