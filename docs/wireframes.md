# ZERO FEAR – Wireframe Documentation

## 1. Introduction

Wireframes define the structural layout, content hierarchy and primary components of application screens before detailed visual design and implementation.

For ZERO FEAR, wireframing establishes how users access the application's main features, interact with different modules and navigate between screens.

Google Stitch is used to develop high-fidelity UI concepts based on these structural decisions.

## 2. Main Navigation Structure

The application uses five primary bottom navigation tabs:

1. Home
2. Insights
3. Plan
4. Discover
5. Profile

My Garage is accessible through the Home and Profile sections rather than being a separate bottom navigation tab.

## 3. Home Dashboard Wireframe

### Main Sections

1. Application header.
2. Registered vehicle overview.
3. Battery percentage and displayed remaining range.
4. Quick action shortcuts.
5. Dashboard Scanner access.
6. Driving efficiency summary.
7. Recent journeys and activity.
8. Charging discovery shortcut.
9. My Garage access.
10. Bottom navigation.

### Main Purpose

Provide users with a personalised overview of their electric vehicle and quick access to important application features.

## 4. Discover – Charging Station Map Wireframe

### Main Sections

1. Search location field.
2. Charging station filters.
3. Interactive map.
4. Charging station markers.
5. Selected station indicator.
6. Collapsible station details panel.
7. Connector types and charging power.
8. Pricing and available facilities.
9. Navigation action.

### Main Purpose

Help users discover charging stations and review relevant station information.

### Station Details

The station details panel should provide relevant information about the selected charging station without requiring unnecessary separate screens for individual information categories.

Live availability and reservation information should only be displayed when supported by external service integrations.

## 5. Trip Planner Wireframe

The trip planning experience consists of four main screens.

### Screen 1 – Journey Setup

1. Starting location input.
2. Destination input.
3. Vehicle selection.
4. Current battery percentage.
5. Plan Journey action.

### Screen 2 – Route Analysis

1. Route map.
2. Estimated distance.
3. Estimated journey duration.
4. Estimated energy requirements.
5. Predicted arrival battery percentage.
6. Route overview.

### Screen 3 – Route Alternatives

1. Recommended route.
2. Alternative route options.
3. Estimated arrival battery percentage.
4. Recommended charging stops when required.
5. Estimated charging information.
6. Select Route action.

### Screen 4 – Active Navigation

1. Navigation map.
2. Next navigation instruction.
3. Remaining distance.
4. Estimated arrival time.
5. Predicted battery information.
6. Find Charger action.
7. End Trip action.

### Main Purpose

Allow users to plan journeys using EV-specific information and estimated battery requirements.

All route, energy and arrival battery calculations are estimates and should not be presented as guaranteed outcomes.

## 6. My Garage Wireframe

### Main Sections

1. Garage header.
2. Registered vehicle cards.
3. Primary vehicle indicator.
4. Vehicle information.
5. Vehicle management actions.
6. Add Vehicle action.
7. Bottom navigation.

### Vehicle Details

The individual vehicle details screen should provide:
- Vehicle manufacturer and model.
- Variant and model year.
- Available vehicle specifications.
- Primary vehicle status.
- Edit vehicle action.

### Main Purpose

Allow users to register, view and manage their electric vehicles.

## 7. Add Vehicle Wireframe

The vehicle registration process uses three steps.

### Step 1 – Vehicle Selection

- Manufacturer selection.
- Vehicle model.
- Powertrain variant.
- Model year.
- Continue action.

### Step 2 – Vehicle Confirmation

- Vehicle preview.
- Selected variant.
- Available vehicle specifications.
- Primary vehicle selection.
- Confirm and Add Vehicle action.

### Step 3 – Vehicle Added

- Registration success message.
- Registered vehicle summary.
- Go to My Garage action.
- Continue to Dashboard Scanner option.

### Main Purpose

Allow users to register an EV and establish the vehicle information used by other application modules.

## 8. Dashboard Scanner Wireframe

The dashboard scanning workflow consists of three main screens.

### Screen 1 – Dashboard Scanner

- Camera preview.
- Dashboard alignment guidance.
- Capture action.
- Manual entry option.

### Screen 2 – Review Readings

- Captured dashboard image.
- Extracted battery percentage.
- Displayed remaining range.
- Odometer reading, when visible.
- Editable values.
- Confirm and Save action.

### Screen 3 – Scan Success

- Confirmation message.
- Saved vehicle reading summary.
- Return to Home action.
- View My Garage action.

### Main Purpose

Use AI-assisted image processing to extract useful information from EV dashboard photographs.

Extracted information must be reviewed and confirmed by the user before it becomes a saved vehicle record.

## 9. Insights and Vehicle History Wireframe

### Insights Dashboard

Main Sections:

1. Vehicle selector.
2. Reporting period selection.
3. Monthly distance summary.
4. Driving efficiency overview.
5. Battery reading trend chart.
6. Recent journeys.
7. Charging summary.
8. Full Vehicle Logbook action.

### Battery Reading History

- Latest confirmed battery percentage.
- Displayed remaining range.
- Chronological reading list.
- Reading date and time.
- Reading source: AI Scan or Manual Entry.
- Reading filters.

### Battery Reading Details

- Confirmed battery percentage.
- Displayed remaining range.
- Odometer reading, when available.
- Reading date and time.
- Reading source.
- Original dashboard photograph, when saved.
- Edit and delete actions.

### Journey History

- Chronological journey list.
- Journey origin and destination.
- Journey date.
- Distance travelled.
- Journey duration.
- Journey details access.

### Journey Details

- Journey route.
- Starting and ending information.
- Distance travelled.
- Duration.
- Available battery readings.
- Journey summary.

### Charging History

- Chronological charging session list.
- Charging date and time.
- Charging location, when available.
- Battery level before and after charging, when recorded.
- Energy added, when available.
- Charging session details access.

### Charging Session Details

- Charging location.
- Session date and time.
- Starting and ending battery percentages, when recorded.
- Energy added, when available.
- Charging duration.
- Recorded charging cost, when available.

### Full Vehicle Logbook

Provides a consolidated view of available vehicle records, including:

- Battery readings.
- Journey history.
- Charging sessions.
- Relevant vehicle activity.

### Main Purpose

Present historical vehicle information and help users understand their driving activity, charging records and battery trends.

## 10. Profile and Settings Wireframe

### Main Sections

1. User profile information.
2. Primary vehicle shortcut.
3. My Garage access.
4. Application preferences.
5. Theme selection.
6. Notification preferences.
7. Privacy and security.
8. Help and support.
9. About application.
10. Logout action.

### Main Purpose

Allow users to manage their account information, registered vehicles and application preferences.

## 11. EV Marketplace Wireframe

### Marketplace Home

1. Marketplace title.
2. Vehicle search.
3. Category filters.
4. Vehicle listing cards.
5. Vehicle photographs.
6. Model and year.
7. Asking price.
8. Favourite action.
9. View Details action.

### Vehicle Listing Details

1. Vehicle photo gallery.
2. Vehicle name and model year.
3. Asking price.
4. Essential vehicle specifications.
5. Full specifications section.
6. Vehicle condition.
7. Seller information.
8. Contact Seller action.
9. Report Listing action.

### Main Purpose

Allow users to browse electric vehicles and access relevant listing and seller information.

## 12. Future UI Concepts

The following features may be explored in future design iterations:

- AI EV Assistant.
- Rewards and Achievements.
- Advanced Vehicle Analytics.
- Marketplace Seller Management.

These features are not part of the current completed UI design scope.

## 13. Wireframe Design Principles

- Keep screens focused on their primary purpose.
- Prioritise important information.
- Avoid overcrowding and unnecessary interface elements.
- Maintain consistent navigation.
- Use a clear content hierarchy.
- Provide simple and predictable user interactions.
- Use progressive disclosure for advanced information.
- Maintain consistent components across application modules.

## 14. Relationship to High-Fidelity Designs

The structural wireframes establish the layout and content requirements for the ZERO FEAR application.

Google Stitch is used to develop high-fidelity UI concepts based on these requirements.

The high-fidelity designs introduce:
- ZERO FEAR visual identity.
- Colours and typography.
- Cards and reusable interface components.
- Icons and illustrations.
- Detailed spacing and layout.
- Interactive visual elements.

Google Stitch screenshots and approved visual references should be maintained separately from this document.

## 15. Documentation and Implementation Status

This document describes the intended wireframe structure of the ZERO FEAR application.

The structural concepts and high-fidelity UI designs are being developed before implementation.

Not every screen described in this document has an individually completed or approved design.

Actual application components and interactions will be implemented and tested during React Native development.

