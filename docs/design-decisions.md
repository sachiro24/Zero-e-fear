# ZERO FEAR – UI/UX Design Decisions

## 1. Product Design Direction

The application follows a futuristic EV technology design direction.

The Home screen focuses on personal vehicle intelligence rather than using a charging station map as the primary dashboard.

## 2. Navigation Structure

The application uses five primary navigation tabs:

- Home
- Insights
- Plan
- Discover
- Profile

## 3. Home Screen

The Home screen provides:
- Registered vehicle overview.
- Battery percentage.
- Estimated remaining range.
- AI Dashboard Scanner shortcut.
- Driving efficiency summary.
- Recent activity.

Detailed analytics are displayed in the Insights section instead of overcrowding Home.

## 4. Explore Screen

The Explore screen uses a map-first design.

Charging station details are displayed using a collapsible bottom sheet.

The collapsed state provides essential station information. The expanded state provides connectors, charging prices and amenities.

## 5. Trip Planner

The Trip Planner collects:
- Starting location.
- Destination.
- Registered vehicle.
- Current battery percentage.
- Journey preferences.

Route results display:
- Distance.
- Estimated travel time.
- Predicted arrival battery.
- Recommended charging stops.
- Alternative routes.

## 6. My Garage

My Garage uses simple vehicle cards.

Each card displays:
- Vehicle image.
- Manufacturer and model.
- Variant and year.
- Latest confirmed battery percentage.
- Estimated remaining range.

Users can select an active vehicle and add additional vehicles.

## 7. Add Vehicle

Vehicle registration follows a three-step process:

1. Select vehicle.
2. Confirm vehicle specifications.
3. Save vehicle.

Unnecessary engineering specifications should not be displayed during basic registration.

## 8. AI Dashboard Scanner

The scanning workflow contains three stages:

1. Scan Dashboard.
2. Review Extracted Readings.
3. Reading Saved.

The scanner extracts:
- Battery percentage.
- Displayed remaining range.
- Odometer reading, when visible.

All extracted values must be reviewed and confirmed by the user before being stored as confirmed readings.

Manual entry must be available.

## 9. Insights and Efficiency

The Insights screen will provide historical vehicle information using confirmed readings, recorded trips and charging records.

Estimated values must be distinguished from measured values.

Battery health or degradation must not be diagnosed from dashboard photographs alone.

## 10. General UI Decisions

- Avoid overcrowded screens.
- Prioritise important information.
- Use consistent spacing.
- Maintain a common visual identity.
- Keep advanced information expandable.
- Avoid unnecessary decorative elements.

## 11. Design Status

Designs are being iteratively reviewed using Google Stitch. A screen should only be marked approved after its layout and interactions have been reviewed.
