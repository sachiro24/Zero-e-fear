# ZERO FEAR – Functional Requirements

## 1. Introduction

This document defines the functional requirements of ZERO FEAR, a personal EV intelligence platform initially targeting electric vehicle owners in Sri Lanka.

Functional requirements describe the operations and behaviours that the application must provide to satisfy user needs.

Each requirement has a unique identifier and an implementation priority to support development planning, testing and future improvements.

## 2. Requirement Priorities

- **Must Have:** Essential functionality for the initial MVP.
- **Should Have:** Important functionality that can be implemented after the core MVP.
- **Future:** Functionality planned for later product releases.

UI design completion does not necessarily mean that the corresponding feature must be implemented in the initial MVP.

## 3. Functional Requirements

### FR-01: User Authentication and Account Management

| ID | Requirement | Priority |
|---|---|---|
| FR-01.1 | The system shall allow users to register an account. | Must Have |
| FR-01.2 | The system shall allow registered users to log in. | Must Have |
| FR-01.3 | The system shall allow users to log out. | Must Have |
| FR-01.4 | The system shall allow users to view and update their profile information. | Must Have |
| FR-01.5 | The system shall allow users to request password recovery. | Should Have |
| FR-01.6 | The system shall allow users to request account deletion. | Should Have |

### FR-02: Electric Vehicle Management

| ID | Requirement | Priority |
|---|---|---|
| FR-02.1 | The system shall allow users to add an electric vehicle to their account. | Must Have |
| FR-02.2 | The system shall provide a catalogue of supported EV manufacturers and models. | Must Have |
| FR-02.3 | The system shall display available vehicle specifications, including battery capacity and compatible charging connectors. | Must Have |
| FR-02.4 | The system shall allow users to update registered vehicle information. | Must Have |
| FR-02.5 | The system shall allow users to remove a registered vehicle. | Should Have |
| FR-02.6 | The system shall allow users to manage multiple registered vehicles. | Should Have |
| FR-02.7 | The system shall allow users to enter or update vehicle-specific information when catalogue information is unavailable. | Should Have |
| FR-02.8 | The system shall allow users to select a primary vehicle. | Must Have |

### FR-03: Charging Station Discovery

| ID | Requirement | Priority |
|---|---|---|
| FR-03.1 | The system shall display available charging station records on an interactive map. | Should Have |
| FR-03.2 | The system shall allow users to search for charging stations by location. | Should Have |
| FR-03.3 | The system shall allow users to filter stations by connector type and other supported criteria. | Should Have |
| FR-03.4 | The system shall display station information, including location, connector type and charging power where available. | Should Have |
| FR-03.5 | The system shall display charging prices where verified pricing information is available. | Should Have |
| FR-03.6 | The system shall display the last verification or update time of station information where available. | Should Have |
| FR-03.7 | The system shall allow users to submit reports about incorrect station information. | Future |
| FR-03.8 | The system shall distinguish confirmed availability information from unknown or outdated availability information. | Must Have |

### FR-04: Intelligent EV Trip Planning

| ID | Requirement | Priority |
|---|---|---|
| FR-04.1 | The system shall allow users to enter a starting location and destination. | Should Have |
| FR-04.2 | The system shall allow users to select a registered EV for trip planning. | Should Have |
| FR-04.3 | The system shall obtain the current battery percentage from a user-provided value or confirmed vehicle reading. | Should Have |
| FR-04.4 | The system shall calculate estimated energy consumption using available vehicle and route information. | Should Have |
| FR-04.5 | The system shall estimate the battery percentage at the destination. | Should Have |
| FR-04.6 | The system shall identify charging stations along or near a planned route. | Should Have |
| FR-04.7 | The system shall recommend compatible charging stations when charging is required. | Should Have |
| FR-04.8 | The system shall display estimated route distance and travel time. | Should Have |
| FR-04.9 | The system shall display the assumptions used for battery-consumption predictions. | Must Have |
| FR-04.10 | The system shall allow users to save planned journeys. | Future |

### FR-05: AI Dashboard Scanner

| ID | Requirement | Priority |
|---|---|---|
| FR-05.1 | The system shall allow users to capture or upload a vehicle dashboard photograph. | Must Have |
| FR-05.2 | The system shall process the photograph to identify supported dashboard readings. | Must Have |
| FR-05.3 | The system shall extract battery percentage when clearly visible and readable. | Must Have |
| FR-05.4 | The system shall extract displayed driving range and odometer readings when supported and readable. | Should Have |
| FR-05.5 | The system shall display extracted values for user review before saving. | Must Have |
| FR-05.6 | The system shall allow users to correct extracted readings. | Must Have |
| FR-05.7 | The system shall save user-confirmed readings with timestamps. | Must Have |
| FR-05.8 | The system shall allow users to view historical dashboard readings. | Must Have |
| FR-05.9 | The system shall indicate when a reading cannot be reliably extracted. | Must Have |
| FR-05.10 | The system shall allow users to enter dashboard readings manually when image extraction is unavailable or unsuccessful. | Must Have |
| FR-05.11 | The system shall identify whether a saved reading originated from an AI dashboard scan or manual entry. | Must Have |

### FR-06: Trip History and Vehicle Analytics

| ID | Requirement | Priority |
|---|---|---|
| FR-06.1 | The system shall allow users to save completed trip information. | Should Have |
| FR-06.2 | The system shall store trip distance and available starting and ending battery readings. | Should Have |
| FR-06.3 | The system shall calculate estimated real-world vehicle efficiency using suitable recorded data. | Should Have |
| FR-06.4 | The system shall allow users to view their previous trips. | Should Have |
| FR-06.5 | The system shall display historical vehicle-efficiency information. | Should Have |
| FR-06.6 | The system shall use sufficiently reliable historical vehicle information to improve future energy predictions. | Future |
| FR-06.7 | The system shall allow users to view individual journey details. | Should Have |
| FR-06.8 | The system shall provide a consolidated vehicle logbook containing available vehicle activity records. | Should Have |

### FR-07: EV Savings Intelligence

| ID | Requirement | Priority |
|---|---|---|
| FR-07.1 | The system shall allow users to select an electric vehicle for cost comparison. | Future |
| FR-07.2 | The system shall allow users to select a petrol or diesel comparison vehicle. | Future |
| FR-07.3 | The system shall allow users to enter their average daily or monthly driving distance. | Future |
| FR-07.4 | The system shall calculate estimated EV electricity costs. | Future |
| FR-07.5 | The system shall calculate estimated fuel costs for the selected comparison vehicle. | Future |
| FR-07.6 | The system shall display estimated cost per kilometre for both vehicles. | Future |
| FR-07.7 | The system shall display estimated daily, monthly and annual running costs. | Future |
| FR-07.8 | The system shall calculate estimated running-cost savings. | Future |
| FR-07.9 | The system shall allow users to adjust fuel prices, electricity tariffs and consumption assumptions. | Future |
| FR-07.10 | The system shall display the assumptions and price dates used in each comparison. | Future |
| FR-07.11 | The system shall support estimated maintenance and total ownership cost comparisons. | Future |
| FR-07.12 | The system shall estimate the break-even period based on purchase-price differences and projected savings. | Future |

### FR-08: AI EV Assistant

| ID | Requirement | Priority |
|---|---|---|
| FR-08.1 | The system shall provide a conversational interface for EV-related questions. | Future |
| FR-08.2 | The system shall retrieve relevant vehicle information when answering vehicle-specific questions. | Future |
| FR-08.3 | The system shall use available trip and charging information when answering relevant questions. | Future |
| FR-08.4 | The system shall distinguish estimates from verified information. | Must Have |
| FR-08.5 | The system shall indicate when requested information is unavailable or cannot be verified. | Must Have |

### FR-09: Eco-Driving and Rewards

| ID | Requirement | Priority |
|---|---|---|
| FR-09.1 | The system shall calculate driving-efficiency scores using available validated journey information. | Future |
| FR-09.2 | The system shall award points for eligible eco-driving achievements. | Future |
| FR-09.3 | The system shall provide achievement badges and levels. | Future |
| FR-09.4 | The system shall allow users to view their rewards and progress. | Future |
| FR-09.5 | The system shall support efficiency challenges and leaderboards. | Future |

### FR-10: EV Marketplace

| ID | Requirement | Priority |
|---|---|---|
| FR-10.1 | The system shall display available EV listings. | Future |
| FR-10.2 | The system shall allow users to search listings by manufacturer and model. | Future |
| FR-10.3 | The system shall allow users to filter listings by price and other available specifications. | Future |
| FR-10.4 | The system shall display vehicle photographs, specifications and listed prices. | Future |
| FR-10.5 | The system shall display seller contact information according to platform privacy rules. | Future |
| FR-10.6 | The system shall allow users to save favourite listings. | Future |
| FR-10.7 | The system shall allow authorised sellers to create and manage listings. | Future |

### FR-11: Charging History Management

| ID | Requirement | Priority |
|---|---|---|
| FR-11.1 | The system should allow users to record charging sessions. | Should Have |
| FR-11.2 | The system should store charging date and time. | Should Have |
| FR-11.3 | The system should store starting and ending battery percentages when available. | Should Have |
| FR-11.4 | The system should store energy added and charging cost when available. | Should Have |
| FR-11.5 | The system should allow users to view historical charging sessions. | Should Have |
| FR-11.6 | The system should allow users to view individual charging session details. | Should Have |

## 4. Data Validation and Error Handling

The system shall:

1. Validate user-provided information before processing it.
2. Reject invalid battery percentages outside the range of 0–100%.
3. Identify missing or invalid vehicle specifications before performing vehicle-dependent calculations.
4. Notify users when a required external service is unavailable.
5. Avoid presenting unavailable charging information as confirmed live availability.
6. Avoid saving unconfirmed AI-extracted dashboard readings as confirmed vehicle data.
7. Distinguish displayed remaining range from battery capacity and actual driving efficiency.
8. Clearly identify estimated route, energy and arrival battery calculations.
9. Provide appropriate error messages when dashboard photographs cannot be processed.
10. Preserve user-entered information when an operation fails, where technically appropriate.

## 5. Initial MVP Scope

The initial MVP should prioritise a small set of connected and testable capabilities.

### Core MVP

- User registration and login.
- Vehicle registration and primary vehicle selection.
- Home Dashboard.
- Manual dashboard reading entry.
- AI-assisted dashboard scanning prototype.
- Review and confirmation of extracted readings.
- Saving and viewing battery reading history.
- Basic Insights Dashboard.

### Subsequent Development

- Charging station discovery and station details.
- Trip planning and route analysis.
- Journey history and efficiency analytics.
- Charging history and vehicle logbook.

### Future Releases

- Advanced EV savings intelligence.
- AI EV Assistant.
- Eco-driving rewards and achievements.
- EV Marketplace functionality.
- Advanced vehicle analytics and integrations.

The MVP scope may be refined based on development time, data availability, external service dependencies and testing results.

## 6. Requirement Scope and Dependencies

Some requirements depend on external services and reliable data sources.

Examples include:

- Charging station discovery requires an appropriate station dataset or service.
- Route planning requires a routing or mapping service.
- Battery predictions require vehicle specifications and suitable energy-consumption assumptions.
- AI dashboard scanning requires a vision-processing service.
- Marketplace functionality requires listing data and seller-management capabilities.

The application must communicate limitations when required information or external services are unavailable.

## 7. Conclusion

This document establishes the functional scope of ZERO FEAR.

These requirements will guide UI/UX design, system architecture, database development, API implementation and software testing.

Requirements may be refined as the product is developed and validated with EV owners.
