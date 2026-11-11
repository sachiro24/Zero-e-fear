# EV Navigator – Functional Requirements

## 1. Introduction

This document defines the functional requirements of EV Navigator.

Functional requirements describe the operations and behaviours that the application must provide to satisfy user needs.

Each requirement has a unique identifier and a priority to support implementation planning and testing.

## 2. Requirement Priorities

- **Must Have:** Essential for the initial MVP.
- **Should Have:** Important but can be implemented after the core MVP.
- **Future:** Planned for later product releases.

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
| FR-02.2 | The system shall provide a catalogue of supported EV models. | Must Have |
| FR-02.3 | The system shall display vehicle specifications, including battery capacity and compatible charging connectors where available. | Must Have |
| FR-02.4 | The system shall allow users to update their vehicle information. | Must Have |
| FR-02.5 | The system shall allow users to remove a registered vehicle. | Must Have |
| FR-02.6 | The system shall allow users to manage multiple registered vehicles. | Should Have |
| FR-02.7 | The system shall allow users to enter or update vehicle-specific information when supported catalogue information is unavailable. | Should Have |

### FR-03: Charging Station Discovery

| ID | Requirement | Priority |
|---|---|---|
| FR-03.1 | The system shall display available charging station records on a map. | Must Have |
| FR-03.2 | The system shall allow users to search for charging stations by location. | Must Have |
| FR-03.3 | The system shall allow users to filter stations by connector type. | Must Have |
| FR-03.4 | The system shall display station information, including location, connector type and charging power where available. | Must Have |
| FR-03.5 | The system shall display charging prices where verified pricing information is available. | Should Have |
| FR-03.6 | The system shall display the last verification or update time of station information where available. | Must Have |
| FR-03.7 | The system shall allow users to submit reports about incorrect station information. | Should Have |
| FR-03.8 | The system shall distinguish confirmed availability information from unknown or outdated availability information. | Must Have |

### FR-04: Intelligent EV Trip Planning

| ID | Requirement | Priority |
|---|---|---|
| FR-04.1 | The system shall allow users to enter a starting location and destination. | Must Have |
| FR-04.2 | The system shall allow users to select a registered EV for trip planning. | Must Have |
| FR-04.3 | The system shall obtain the current battery percentage from the user or confirmed vehicle reading. | Must Have |
| FR-04.4 | The system shall calculate estimated energy consumption for a planned journey using available vehicle and route information. | Must Have |
| FR-04.5 | The system shall estimate the battery percentage at the destination. | Must Have |
| FR-04.6 | The system shall identify charging stations along or near a planned route. | Must Have |
| FR-04.7 | The system shall recommend compatible charging stations when charging is required. | Must Have |
| FR-04.8 | The system shall display estimated route distance and travel time. | Must Have |
| FR-04.9 | The system shall display the assumptions used for battery-consumption predictions. | Must Have |
| FR-04.10 | The system shall allow users to save planned journeys. | Should Have |

### FR-05: EV Snapshot AI – Dashboard Scanning

| ID | Requirement | Priority |
|---|---|---|
| FR-05.1 | The system shall allow users to capture or upload a vehicle dashboard photograph. | Must Have |
| FR-05.2 | The system shall process the uploaded photograph to identify supported dashboard readings. | Must Have |
| FR-05.3 | The system shall extract battery percentage when clearly visible and readable. | Must Have |
| FR-05.4 | The system shall extract displayed driving range and odometer readings when supported and readable. | Should Have |
| FR-05.5 | The system shall display extracted values for user review before saving. | Must Have |
| FR-05.6 | The system shall allow users to correct extracted readings. | Must Have |
| FR-05.7 | The system shall save user-confirmed readings with timestamps. | Must Have |
| FR-05.8 | The system shall allow users to view historical dashboard readings. | Must Have |
| FR-05.9 | The system shall indicate when a reading cannot be reliably extracted. | Must Have |

### FR-06: Trip History and Vehicle Analytics

| ID | Requirement | Priority |
|---|---|---|
| FR-06.1 | The system shall allow users to save completed trip information. | Must Have |
| FR-06.2 | The system shall store trip distance and available starting and ending battery readings. | Must Have |
| FR-06.3 | The system shall calculate estimated real-world vehicle efficiency using suitable recorded data. | Must Have |
| FR-06.4 | The system shall allow users to view their previous trips. | Must Have |
| FR-06.5 | The system shall display historical vehicle-efficiency information. | Should Have |
| FR-06.6 | The system shall use sufficiently reliable historical vehicle information to improve future energy predictions. | Should Have |

### FR-07: EV Savings Intelligence

| ID | Requirement | Priority |
|---|---|---|
| FR-07.1 | The system shall allow users to select an electric vehicle for cost comparison. | Must Have |
| FR-07.2 | The system shall allow users to select a petrol or diesel comparison vehicle. | Must Have |
| FR-07.3 | The system shall allow users to enter their average daily or monthly driving distance. | Must Have |
| FR-07.4 | The system shall calculate estimated EV electricity costs. | Must Have |
| FR-07.5 | The system shall calculate estimated fuel costs for the selected comparison vehicle. | Must Have |
| FR-07.6 | The system shall display estimated cost per kilometre for both vehicles. | Must Have |
| FR-07.7 | The system shall display estimated daily, monthly and annual running costs. | Must Have |
| FR-07.8 | The system shall calculate estimated running-cost savings. | Must Have |
| FR-07.9 | The system shall allow users to adjust fuel prices, electricity tariffs and consumption assumptions. | Must Have |
| FR-07.10 | The system shall display the assumptions and price dates used in each comparison. | Must Have |
| FR-07.11 | The system shall support estimated maintenance and total ownership cost comparisons. | Future |
| FR-07.12 | The system shall estimate the break-even period based on purchase-price differences and projected savings. | Future |

### FR-08: AI EV Assistant

| ID | Requirement | Priority |
|---|---|---|
| FR-08.1 | The system shall provide a conversational interface for EV-related questions. | Should Have |
| FR-08.2 | The system shall retrieve relevant vehicle information when answering vehicle-specific questions. | Should Have |
| FR-08.3 | The system shall use available trip and charging information when answering relevant questions. | Should Have |
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
| FR-10.2 | The system shall allow users to search listings by brand and model. | Future |
| FR-10.3 | The system shall allow users to filter listings by price and other available specifications. | Future |
| FR-10.4 | The system shall display vehicle photographs, specifications and listed prices. | Future |
| FR-10.5 | The system shall display seller contact information according to platform privacy rules. | Future |
| FR-10.6 | The system shall allow users to save favourite listings. | Future |
| FR-10.7 | The system shall allow authorized sellers to create and manage listings. | Future |

## 4. Data Validation and Error Handling

1. The system shall validate user-provided information before processing it.
2. The system shall reject invalid battery percentages outside the range of 0–100%.
3. The system shall identify missing or invalid vehicle specifications before performing vehicle-dependent calculations.
4. The system shall notify users when a required external service is unavailable.
5. The system shall avoid presenting unavailable charging information as confirmed live availability.
6. The system shall avoid saving unconfirmed AI-extracted dashboard readings as confirmed vehicle data.

## 5. Requirement Scope

The initial MVP will prioritize FR-01 through FR-07, together with the essential safety and data-grounding requirements of FR-08.

FR-09 and FR-10 will be developed in future releases.

## 6. Conclusion

This document establishes the initial functional scope of EV Navigator.

The requirements will guide UI/UX design, architecture, database development, API implementation and software testing.

Requirements may be refined as the product is validated with EV owners and technical feasibility is investigated.
