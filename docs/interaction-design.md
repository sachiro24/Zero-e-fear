# ZERO FEAR – Interaction Design and Navigation Flow

## 1. Purpose

This document defines how users interact with ZERO FEAR and navigate between its main application screens.

## 2. Main Navigation

The application uses five primary bottom navigation tabs:

1. Home
2. Insights
3. Plan
4. Discover
5. Profile

## 3. Onboarding Flow

Splash Screen → Onboarding → Registration/Login → Add Vehicle → Dashboard Scanner → Review Readings → Confirm and Save → Home Dashboard.

Users must be able to enter readings manually if dashboard scanning is unsuccessful.

## 4. Home Interactions

- Scan Dashboard opens the scanner.
- Plan Journey opens the Trip Planner.
- Find Chargers opens Explore.
- View Insights opens Insights.
- My Garage opens vehicle management.

## 5. Explore Interactions

- Search allows users to find charging stations.
- Filters allow users to narrow station results.
- Selecting a marker displays station information.
- Station details can expand or collapse.
- Navigate opens the available directions experience.

## 6. Trip Planning Interactions

- Users enter starting location and destination.
- Users select a registered vehicle.
- Users provide or confirm current battery percentage.
- Plan Journey requests a route calculation.
- Route Results display estimated distance, duration and arrival battery.
- Users can compare alternative routes.
- Start Navigation opens the active trip experience.

## 7. Vehicle Management Interactions

- My Garage displays registered vehicles.
- Users can select an active vehicle.
- Add Vehicle opens the three-step registration process.
- Manage Vehicle opens vehicle details and editing options.

## 8. Dashboard Scanner Interactions

The scanner follows three stages:

1. Capture dashboard photograph.
2. Review extracted battery percentage, displayed range and odometer.
3. Confirm and save readings.

Extracted readings must remain pending until confirmed by the user.

Manual entry must be supported.

## 9. Insights Interactions

- Users can select a vehicle.
- Users can change the reporting period.
- Users can view battery reading trends.
- Users can access recent journeys.
- View Full Logbook opens detailed history.

## 10. Marketplace Interactions

- Search electric vehicle listings.
- Filter listings by category and condition.
- Save favourite listings.
- Open listing details.
- Contact the seller using the available contact method.

## 11. Profile Interactions

- Edit personal information.
- Manage account preferences.
- Change application theme.
- Manage notification preferences.
- Access privacy, security and support.
- Log out.

## 12. Interaction States

Important interactions should support:

- Loading state.
- Success state.
- Error state.
- Empty state.
- Validation feedback.
- Confirmation before important destructive actions.

## 13. General Interaction Principles

- Keep navigation predictable.
- Provide clear feedback after user actions.
- Avoid unnecessary navigation steps.
- Preserve user-entered information when appropriate.
- Clearly communicate failures.
- Never display estimated information as confirmed data.

## 14. Implementation Status

This document describes the planned interaction behaviour. Actual interactions will be implemented and tested during mobile application development.
