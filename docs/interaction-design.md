# ZERO FEAR – Interaction Design and Navigation Flow

## 1. Purpose

This document defines how users interact with ZERO FEAR and navigate between its main application screens.

It describes the expected behaviour of interface elements, user actions, feedback states and interactions across the application's main modules.

## 2. Main Navigation

The application uses five primary bottom navigation tabs:

1. Home
2. Insights
3. Plan
4. Discover
5. Profile

Users should be able to switch between these sections while maintaining a consistent navigation experience.

My Garage can be accessed through Home and Profile.

## 3. Onboarding and Authentication Interactions

### New User Flow

Splash Screen → Welcome / Onboarding → Registration → Email Verification (if implemented) → Add Vehicle → Vehicle Confirmation → Dashboard Scanner → Review Readings → Confirm and Save → Home Dashboard.

### Returning User Flow

Splash Screen → Login → Authentication → Home Dashboard.

If a returning user has not registered a vehicle, the application should guide them to Add Vehicle.

### Interaction Behaviour

- Registration fields should validate user input.
- Password fields should support secure input.
- Authentication failures should display clear error messages.
- Users should be able to access password recovery.
- Users should not be forced to scan their dashboard every time they log in.

## 4. Home Dashboard Interactions

The Home Dashboard provides shortcuts to frequently used application features.

- Scan Dashboard opens the Dashboard Scanner.
- Plan Journey opens the Journey Setup screen.
- Find Chargers opens the Charging Station Map.
- View Insights opens the Insights Dashboard.
- My Garage opens vehicle management.
- Selecting the vehicle overview opens Vehicle Details.

The displayed battery percentage and remaining range should represent the latest available confirmed readings, with their reading time where appropriate.

## 5. Charging Discovery Interactions

### Map Interactions

- Search allows users to find charging stations by location.
- Filters allow users to narrow station results.
- Selecting a map marker displays information about the selected station.
- The station details panel can expand or collapse.
- Users can select another marker to view another station.

### Station Details Interactions

- View connector information.
- Review charging power and pricing.
- Review available facilities.
- Select Navigate to open the available directions experience.

Live station availability and reservation actions should only be provided when supported by external service integrations.

## 6. Trip Planning Interactions

### Journey Setup

- Users enter a starting location.
- Users enter a destination.
- Users select a registered vehicle.
- Users provide or confirm their current battery percentage.
- Plan Journey initiates route calculation.

### Route Analysis

- Display calculated route information.
- Display estimated distance and journey duration.
- Display estimated energy requirements.
- Display predicted arrival battery percentage.

### Route Alternatives

- Users can compare available route options.
- Users can select a preferred route.
- Recommended charging stops should be displayed when required.
- Users can review estimated charging information where available.

### Active Navigation

- Display the selected route.
- Provide navigation instructions.
- Display remaining distance and estimated arrival time.
- Display estimated battery information.
- Find Charger opens charging discovery.
- End Trip finishes the active journey.

Route and battery calculations should be presented as estimates rather than guaranteed outcomes.

## 7. Vehicle Management Interactions

### My Garage

- Display registered vehicles.
- Allow users to select a vehicle.
- Identify the primary vehicle.
- Add Vehicle opens the registration process.
- Selecting a vehicle opens Vehicle Details.

### Add Vehicle

The registration process consists of three stages:

1. Vehicle Selection.
2. Vehicle Confirmation.
3. Vehicle Added Success.

Users should be able to review the selected manufacturer, model, variant, year and available specifications before confirming registration.

### Vehicle Details

- Display registered vehicle information.
- Allow users to edit supported information.
- Allow users to change the primary vehicle.
- Important actions such as vehicle deletion should require confirmation.

## 8. Dashboard Scanner Interactions

The scanner follows three main stages.

### Stage 1 – Capture Dashboard Photograph

- Request camera permission when required.
- Display the camera preview.
- Provide dashboard alignment guidance.
- Allow users to capture a photograph.
- Provide an option to enter readings manually.

### Stage 2 – Review Extracted Readings

- Display the captured photograph.
- Extract battery percentage.
- Extract displayed remaining range when visible.
- Extract odometer reading when visible.
- Allow users to correct extracted values.
- Clearly identify information that could not be extracted.

### Stage 3 – Confirm and Save

- Users review all available values.
- Confirm and Save stores the reading.
- Successful saving displays a confirmation message.
- The saved reading becomes available in Battery Reading History.

Extracted readings must remain unconfirmed until the user reviews and confirms them.

Manual entry must follow the same review and confirmation process.

## 9. Insights and Vehicle History Interactions

### Insights Dashboard

- Users can select a registered vehicle.
- Users can change the reporting period.
- Users can view distance and efficiency summaries.
- Users can view battery reading trends.
- Users can access Journey History.
- Users can access Charging History.
- View Full Logbook opens consolidated vehicle records.

### Battery Reading History

- Display chronological confirmed readings.
- Allow users to filter readings by source where supported.
- Selecting a reading opens Battery Reading Details.

### Battery Reading Details

- Display the confirmed battery percentage.
- Display remaining range and odometer information when available.
- Display reading date and time.
- Display whether the reading came from AI Scan or Manual Entry.
- Display the original dashboard photograph when available.
- Allow supported editing and deletion actions.

### Journey History

- Display previously recorded journeys.
- Selecting a journey opens Journey Details.

### Charging History

- Display previously recorded charging sessions.
- Selecting a session opens Charging Session Details.

### Full Vehicle Logbook

- Display available vehicle records in a consolidated history.
- Allow users to review relevant readings, journeys and charging activity.

Historical information should distinguish between confirmed records and estimated values.

## 10. Marketplace Interactions

### Marketplace Home

- Search electric vehicle listings.
- Filter listings by category and condition.
- Browse available vehicle listings.
- Save and remove favourite listings.
- Open Vehicle Listing Details.

### Vehicle Listing Details

- Browse vehicle photographs.
- Review vehicle specifications.
- Review asking price and vehicle condition.
- View seller information.
- Contact the seller using the available contact method.
- Report a listing where supported.

Marketplace information should distinguish seller-provided details from independently verified information.

## 11. Profile and Settings Interactions

- Edit personal information.
- Access My Garage.
- Manage account preferences.
- Change application theme.
- Manage notification preferences.
- Access privacy and security settings.
- Access Help and Support.
- Log out of the application.

Users should receive confirmation where appropriate before important account-related actions.

## 12. Interaction States

Important interactions should support the following states:

### Loading State
Indicates that the application is processing a request or retrieving information.

### Success State
Confirms that an action has been completed successfully.

### Error State
Explains when an operation has failed and provides an appropriate recovery option.

### Empty State
Explains when no records or results are available and guides the user towards the next action.

### Validation State
Identifies missing or invalid information entered by the user.

### Confirmation State
Requests confirmation before important or destructive actions, such as deleting a vehicle or saved reading.

### Permission State
Explains when camera or location permissions are required for a feature.

## 13. General Interaction Principles

- Keep navigation predictable.
- Provide clear feedback after user actions.
- Avoid unnecessary navigation steps.
- Preserve user-entered information when appropriate.
- Clearly communicate failures.
- Never display estimated information as confirmed data.
- Use consistent buttons, forms and interaction patterns.
- Prevent accidental destructive actions.
- Provide suitable empty and loading states.
- Ensure important actions remain accessible and understandable.

## 14. Accessibility and Usability Considerations

- Use readable text sizes and sufficient colour contrast.
- Provide clear labels for interactive elements.
- Use appropriate touch target sizes.
- Avoid relying only on colour to communicate information.
- Provide understandable error messages.
- Keep important actions visually distinguishable.
- Ensure layouts remain usable on different mobile screen sizes.

## 15. Implementation Status

This document defines the intended interaction behaviour and navigation flow of ZERO FEAR.

Actual interactions will be implemented and tested during React Native and Expo development.

The implementation should be validated through functional testing, usability testing and integration testing to ensure that the intended user interactions work correctly.
