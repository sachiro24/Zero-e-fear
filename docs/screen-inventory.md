# ZERO FEAR – Screen Inventory

## 1. Authentication and Onboarding

| Screen | Description | Design Status |
|---|---|---|
| Splash Screen | Introduces the ZERO FEAR brand when the application launches | Designed direction |
| Welcome / Onboarding | Introduces the application's purpose and main capabilities | Designed direction |
| Login | Allows existing users to authenticate | Designed direction |
| Registration | Allows new users to create an account | Designed direction |
| Forgot Password | Allows users to recover access to their accounts | Planned |

## 2. Vehicle Management – My Garage

| Screen | Description | Design Status |
|---|---|---|
| My Garage | Displays the user's registered electric vehicles | Designed direction |
| Add Vehicle – Vehicle Selection | Allows users to select manufacturer, model, variant and year | Designed direction |
| Vehicle Confirmation | Allows users to review the selected vehicle and its specifications | Designed direction |
| Vehicle Added Success | Confirms successful vehicle registration | Designed direction |
| Vehicle Details | Displays information about an individual registered vehicle | Designed direction |
| Edit Vehicle | Allows users to update vehicle information | Planned |

## 3. Home Dashboard and Vehicle Intelligence

| Screen | Description | Design Status |
|---|---|---|
| Home Dashboard | Provides a personalised overview of the selected EV, battery reading, range and main features | Designed direction |
| Dashboard Camera Scanner | Allows users to capture photographs of their EV dashboard | Designed direction |
| Review Extracted Readings | Displays extracted battery percentage, remaining range and other available readings for user review and correction | Designed direction |
| Scan Success | Confirms that the reviewed dashboard reading has been saved | Designed direction |
| Manual Reading Entry | Allows users to enter battery readings manually when scanning is unavailable | Planned |

## 4. Insights and Vehicle History

| Screen | Description | Design Status |
|---|---|---|
| Insights Dashboard | Provides an overview of vehicle usage, efficiency, battery trends and activity | Designed direction |
| Journey History | Displays previously recorded journeys | Planned |
| Journey Details | Displays the details of an individual journey | Planned |
| Battery Reading History | Displays previously confirmed battery readings | Planned |
| Battery Reading Details | Displays the details of an individual battery reading, including its source and saved dashboard photo when available | Planned |
| Charging History | Displays recorded charging sessions | Planned |
| Charging Session Details | Displays the information associated with an individual charging session | Planned |
| Full Vehicle Logbook | Provides a consolidated history of vehicle activity, readings, journeys and charging records | Planned |

## 5. Charging Discovery

| Screen | Description | Design Status |
|---|---|---|
| Discover – Charging Station Map | Allows users to discover charging stations through a map interface | Designed direction |
| Charging Station Details | Displays station information, connector types, charging power, pricing and available facilities | Planned |
| Station Filters | Allows users to filter stations based on relevant criteria, such as fast charging and vehicle compatibility | Designed direction |
| Connector Information | Displays connector types and charging power information for a selected station | Included in Station Details |

## 6. Trip Planning

| Screen | Description | Design Status |
|---|---|---|
| Journey Setup | Allows users to enter the origin, destination, selected EV and current battery level | Designed direction |
| Route Analysis | Displays route information, distance, estimated duration and predicted arrival battery level | Designed direction |
| Route Alternatives | Allows users to compare available route options | Designed direction |
| Charging Stop Recommendations | Displays suggested charging stops when required for a journey | Planned |
| Active Navigation | Displays the selected route and ongoing journey information | Designed direction |

## 7. EV Marketplace

| Screen | Description | Design Status |
|---|---|---|
| Marketplace Home | Allows users to browse electric vehicle listings | Designed direction |
| Search and Filters | Allows users to search and filter EV listings | Planned |
| Vehicle Listing Details | Displays detailed information about a selected EV listing, including price, specifications and seller information | Designed direction |
| Favourites | Allows users to save and revisit interesting listings | Planned |

## 8. Account Management

| Screen | Description | Design Status |
|---|---|---|
| Profile and Settings | Displays user information and application settings | Designed direction |
| Notification Preferences | Allows users to manage notification preferences | Planned |
| Help and Support | Provides access to assistance and support information | Planned |

## 9. Future Features

The following screens and features may be introduced in future releases:

| Feature | Description | Design Status |
|---|---|---|
| AI EV Assistant | Provides an AI-powered conversational assistant for EV-related questions | Future |
| Rewards and Achievements | Encourages efficient driving through rewards and achievements | Future |
| Advanced Vehicle Analytics | Provides more detailed vehicle performance and battery analysis | Future |
| Seller Management | Allows users to create and manage marketplace listings | Future |

## 10. Main Application Navigation

The application uses a five-tab bottom navigation structure:

| Navigation Tab | Main Purpose |
|---|---|
| Home | Provides the main vehicle dashboard and shortcuts to important features |
| Insights | Provides vehicle performance information, battery history and usage records |
| Plan | Provides journey planning and route-related features |
| Discover | Provides charging station discovery and access to the EV marketplace |
| Profile | Provides account information, settings and access to My Garage |

My Garage is accessible through the Home and Profile sections rather than being a separate bottom navigation tab.

## 11. Design Status and Implementation Notes

The UI/UX designs are being developed using Google Stitch.

The design status values used in this inventory are:

- **Designed direction:** A screen concept has been created or its design direction has been established. It may still require refinement and review.
- **Planned:** The screen has been identified but its individual design has not yet been completed and reviewed.
- **Future:** The feature is intended for a later release and is not part of the immediate MVP design work.

This inventory documents the planned and designed application screens. It does not imply that all screens have been fully approved, implemented or connected to working backend services.

Certain capabilities, including live charging station availability, vehicle telemetry integration, real-time navigation and marketplace transactions, will require appropriate external services or backend integrations before they can be offered as operational features.
