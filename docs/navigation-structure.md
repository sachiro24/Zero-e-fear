# ZERO FEAR – Navigation Structure

## 1. Overview

ZERO FEAR uses a five-tab bottom navigation system designed to provide quick access to the application's main modules.

The five primary navigation tabs are:

1. Home
2. Insights
3. Plan
4. Discover
5. Profile

Each tab provides access to its respective features and related screens. Detailed screens are accessed through navigation within each module.

My Garage is accessible through Home and Profile rather than being a separate bottom navigation tab.

## 2. Primary Navigation

### 2.1 Home

The Home section provides a personalised overview of the user's electric vehicle and shortcuts to frequently used features.

Provides access to:
- Home Dashboard.
- Dashboard Scanner.
- Manual Reading Entry.
- My Garage.
- Add Vehicle.
- Vehicle Details.
- Trip Planner.
- Charging Station Discovery.
- Insights.

### 2.2 Insights

The Insights section provides access to vehicle performance information and historical activity.

Provides access to:
- Insights Dashboard.
- Battery Reading History.
- Battery Reading Details.
- Journey History.
- Journey Details.
- Charging History.
- Charging Session Details.
- Full Vehicle Logbook.

Users can access relevant historical information and review their vehicle activity.

### 2.3 Plan

The Plan section provides access to journey planning and route-related features.

Provides access to:
- Journey Setup.
- Route Analysis.
- Route Alternatives.
- Charging Stop Recommendations.
- Active Navigation.

### 2.4 Discover

The Discover section provides access to charging infrastructure discovery and the EV marketplace.

Provides access to:
- Charging Station Map.
- Charging Station Details.
- Charging Station Filters.
- EV Marketplace.
- Marketplace Search and Filters.
- Vehicle Listing Details.
- Favourites.

### 2.5 Profile

The Profile section provides access to user account information and application preferences.

Provides access to:
- Profile Information.
- My Garage.
- Account Settings.
- Notification Preferences.
- Theme Settings.
- Privacy and Security.
- Help and Support.

## 3. Onboarding and Authentication Navigation

### 3.1 New User Registration

New users follow this sequence:

Splash Screen  
→ Welcome / Onboarding  
→ Registration  
→ Email Verification (if implemented)  
→ Add Vehicle  
→ Vehicle Selection  
→ Vehicle Confirmation  
→ Vehicle Added Success  
→ Dashboard Scanner  
→ Review Extracted Readings  
→ Confirm and Save  
→ Home Dashboard

Users should have the option to skip the initial dashboard scan and enter readings manually or later.

### 3.2 Existing User Login

Returning users follow this sequence:

Splash Screen  
→ Login  
→ Authentication  
→ Check Registered Vehicles

If a vehicle is already registered:

→ Home Dashboard

If no vehicle is registered:

→ Add Vehicle  
→ Vehicle Confirmation  
→ Home Dashboard

Returning users should not be forced to scan their dashboard every time they log in.

## 4. Vehicle Management Navigation

My Garage can be accessed through Home or Profile.

### 4.1 View Existing Vehicles

Home / Profile  
→ My Garage  
→ Select Vehicle  
→ Vehicle Details  
→ Edit Vehicle (if required)

### 4.2 Add a New Vehicle

My Garage  
→ Add Vehicle  
→ Vehicle Selection  
→ Vehicle Confirmation  
→ Vehicle Added Success  
→ My Garage

Users can select a primary vehicle when multiple vehicles are registered.

## 5. Dashboard Scanner Navigation

The dashboard scanner can be accessed through the Home Dashboard.

Home  
→ Dashboard Scanner  
→ Capture Dashboard Photograph  
→ AI Reading Extraction  
→ Review Extracted Readings  
→ Edit Values (if necessary)  
→ Confirm and Save  
→ Scan Success  
→ Home

### Alternative Manual Entry Flow

Dashboard Scanner  
→ Manual Reading Entry  
→ Review Readings  
→ Confirm and Save  
→ Home

Only user-confirmed readings should be saved as confirmed vehicle records.

## 6. Charging Discovery Navigation

Discover  
→ Charging Station Map  
→ Search or Apply Filters  
→ Select Charging Station  
→ Charging Station Details  
→ Navigate to Station

Users can also access charging discovery through the Find Chargers shortcut on the Home Dashboard.

Station information may include:
- Charging connector types.
- Charging power.
- Charging prices.
- Available facilities.
- Station location.

Live availability and reservation options should only be provided when supported by the relevant charging network or service integration.

## 7. Trip Planning Navigation

Home / Plan  
→ Journey Setup  
→ Enter Origin and Destination  
→ Select Vehicle and Current Battery Level  
→ Route Analysis  
→ Route Alternatives  
→ Review Recommended Charging Stops (if required)  
→ Select Route  
→ Active Navigation  
→ End Trip

The trip planning process should consider the selected vehicle and available battery information when estimating energy requirements and arrival battery level.

Route and battery calculations are estimates and should not be presented as guaranteed outcomes.

## 8. Insights Navigation

Insights  
→ Insights Dashboard

From the dashboard, users can access the following sections:

### 8.1 Battery Reading History

Insights Dashboard  
→ Battery Reading History  
→ Select Reading  
→ Battery Reading Details

### 8.2 Journey History

Insights Dashboard  
→ Journey History  
→ Select Journey  
→ Journey Details

### 8.3 Charging History

Insights Dashboard  
→ Charging History  
→ Select Charging Session  
→ Charging Session Details

### 8.4 Full Vehicle Logbook

Insights Dashboard  
→ Full Vehicle Logbook  
→ Review Consolidated Vehicle Activity

The Insights section should allow users to review historical readings, journeys, charging activity and vehicle performance information.

## 9. Marketplace Navigation

Discover  
→ EV Marketplace  
→ Search / Apply Filters  
→ Browse Vehicle Listings  
→ Select Vehicle  
→ Vehicle Listing Details  
→ Contact Seller

Users may also save listings to Favourites and revisit them later.

Marketplace transactions and seller management may be introduced in future releases.

## 10. Profile and Settings Navigation

Profile  
→ Profile Information  
→ Account Settings  
→ Notification Preferences  
→ Theme Settings  
→ Privacy and Security  
→ Help and Support

Users should be able to manage their account information and application preferences through this section.

## 11. Navigation Behaviour

The application should follow these navigation principles:

- The five primary navigation tabs should remain consistently accessible within the main application.
- Detailed screens should provide appropriate back-navigation actions.
- Opening a feature through a Home shortcut should not create unnecessary duplicate screens.
- Users should be able to return to the relevant primary navigation section.
- Navigation should preserve relevant form information when appropriate.
- Authentication-protected screens should require a valid user session.
- Selecting a different vehicle should update vehicle-dependent information where applicable.
- Destructive actions, such as deleting a vehicle or saved reading, should require confirmation.
- Navigation should remain consistent across all application modules.

## 12. Future Navigation Considerations

The following capabilities may be introduced in future releases:

- AI Assistant accessible throughout the application.
- Notifications and alerts.
- Advanced vehicle management.
- Marketplace seller dashboard.
- Rewards and achievements.
- Advanced vehicle analytics.

These features should be introduced without overcrowding the primary navigation structure.

## 13. Implementation Status

This document defines the planned navigation structure and user flows for ZERO FEAR.

The navigation system will be implemented using React Native and Expo during mobile application development.

Actual navigation behaviour will be tested to ensure that:
- Navigation between primary tabs works correctly.
- Nested screens open and close appropriately.
- Authentication and onboarding flows work as expected.
- Vehicle information is preserved across relevant screens.
- Navigation remains consistent throughout the application.

This document describes the intended navigation design and does not imply that all navigation functionality has already been implemented.
