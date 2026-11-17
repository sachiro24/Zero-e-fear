# ZERO FEAR – Navigation Structure

## 1. Overview

ZERO FEAR uses a five-tab bottom navigation system.

The navigation structure is designed to provide quick access to the application's main modules while allowing users to navigate to detailed screens when required.

## 2. Primary Navigation

### Home
Provides access to:
- Home Dashboard.
- Dashboard Scanner.
- My Garage.
- Add Vehicle.
- Trip Planner.
- Explore Charging.
- Insights.

### Insights
Provides access to:
- Vehicle Insights.
- Battery Reading Trends.
- Recent Journeys.
- Full Vehicle Logbook.
- Historical Reading Details.

### Plan
Provides access to:
- Trip Planner.
- Route Results.
- Route Alternatives.
- Charging Stop Details.
- Active Trip.

### Discover
Provides access to:
- Charging Station Map.
- Station Details.
- Charging Station Filters.
- EV Marketplace.
- Marketplace Listing Details.

### Profile
Provides access to:
- User Profile.
- Account Settings.
- Notification Preferences.
- Theme Settings.
- Privacy and Security.
- Help and Support.

## 3. Onboarding Navigation

New users follow this sequence:

Splash Screen
→ Onboarding
→ Registration / Login
→ Add Vehicle
→ Vehicle Confirmation
→ Dashboard Scanner
→ Review Readings
→ Confirm and Save
→ Home Dashboard

Manual dashboard reading entry must be available if scanning is unsuccessful.

## 4. Vehicle Management Navigation

Home / Profile
→ My Garage
→ Select Vehicle
→ Vehicle Details
→ Edit Vehicle

My Garage
→ Add Vehicle
→ Vehicle Model Selection
→ Vehicle Confirmation
→ Vehicle Added
→ My Garage

## 5. Dashboard Scanner Navigation

Home
→ Dashboard Scanner
→ Capture Photograph
→ Review Readings
→ Confirm and Save
→ Scan Success
→ Home

Alternative flow:

Dashboard Scanner
→ Enter Readings Manually
→ Review Readings
→ Confirm and Save

## 6. Charging Discovery Navigation

Discover
→ Charging Station Map
→ Select Station
→ Station Details
→ Navigate

Users may also access Explore directly from Home using the Find Chargers shortcut.

## 7. Trip Planning Navigation

Home / Plan
→ Trip Planner
→ Enter Journey Details
→ Route Results
→ Select Route
→ Review Charging Stops
→ Start Navigation
→ Active Trip

## 8. Insights Navigation

Insights
→ Vehicle Insights
→ Select Reporting Period
→ View Battery Trends
→ Recent Journeys
→ Full Vehicle Logbook

## 9. Marketplace Navigation

Discover
→ Marketplace
→ Search / Filter Listings
→ Select Vehicle
→ Listing Details
→ Contact Seller

## 10. Profile Navigation

Profile
→ Account Information
→ Settings
→ Preferences
→ Privacy and Security
→ Help and Support

## 11. Navigation Behaviour

- The five primary tabs should remain consistently accessible.
- Detailed screens should provide an appropriate back-navigation action.
- Opening a feature from a shortcut should not create unnecessary duplicate screens.
- Users should be able to return to the relevant primary tab.
- Navigation should preserve relevant form information when appropriate.
- Authentication-protected screens should require a valid user session.

## 12. Future Navigation Considerations

The following navigation capabilities may be introduced in future releases:

- AI Assistant accessible throughout the application.
- Notifications and alerts.
- Advanced vehicle management.
- Marketplace seller dashboard.
- Rewards and achievements.

These features should be added without making the primary navigation overcrowded.

## 13. Implementation Status

This document defines the planned navigation structure.

Actual navigation behaviour will be implemented and tested during React Native development.
