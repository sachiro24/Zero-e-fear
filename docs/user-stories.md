# EV Navigator – User Stories and Acceptance Criteria

## 1. Introduction

This document defines the user stories and acceptance criteria for EV Navigator.

User stories describe application functionality from the perspective of the people who will use the system.

Acceptance criteria define the conditions that must be satisfied before a feature can be considered successfully implemented.

## 2. User Roles

- **EV Owner:** A person who owns and uses an electric vehicle.
- **Potential EV Buyer:** A person researching and comparing electric vehicles.
- **Registered User:** An authenticated user of EV Navigator.
- **Seller:** A future marketplace user who manages vehicle listings.

# 3. User Stories and Acceptance Criteria

## US-01: User Registration

**User story:**

As a new user, I want to create an account so that I can access EV Navigator services.

**Acceptance criteria:**

1. The user can enter the required registration information.
2. The system validates the submitted information.
3. The system prevents registration with an already registered email address.
4. Passwords are securely stored.
5. The system provides confirmation when registration succeeds.
6. The system displays an appropriate error when registration fails.

**Priority:** Must Have

## US-02: User Login

**User story:**

As a registered user, I want to log in securely so that I can access my personal EV information.

**Acceptance criteria:**

1. The user can enter their registered email and password.
2. The system validates the credentials.
3. The system grants access when authentication succeeds.
4. Invalid credentials produce an appropriate error.
5. Protected application features require authentication.

**Priority:** Must Have

## US-03: Add an Electric Vehicle

**User story:**

As an EV owner, I want to add my vehicle to my account so that EV Navigator can provide vehicle-specific services.

**Acceptance criteria:**

1. The user can browse supported EV models.
2. The user can select a vehicle model.
3. The application displays available vehicle specifications.
4. The user can review and confirm the vehicle information.
5. The vehicle is associated with the user's account.
6. The user can update or remove the registered vehicle.

**Priority:** Must Have

## US-04: Discover Charging Stations

**User story:**

As an EV owner, I want to find nearby charging stations so that I can charge my vehicle when necessary.

**Acceptance criteria:**

1. The user can view charging station locations on a map.
2. The application can use the user's location after permission is granted.
3. The user can search for charging stations.
4. The user can filter stations by connector type.
5. The application displays available station details.
6. The application indicates when availability information is unknown or outdated.
7. The application displays the last verification time where available.

**Priority:** Must Have

## US-05: Plan an EV Journey

**User story:**

As an EV owner, I want to plan a journey using my vehicle information so that I can understand the expected battery consumption before travelling.

**Acceptance criteria:**

1. The user can select a registered EV.
2. The user can enter a starting point and destination.
3. The user can enter or confirm the current battery percentage.
4. The system calculates an estimated journey distance.
5. The system estimates battery consumption using available vehicle and route information.
6. The system displays the predicted arrival battery percentage.
7. The system explains when required information is unavailable.
8. The user can review the proposed journey.

**Priority:** Must Have

## US-06: Recommend Charging Stops

**User story:**

As an EV owner, I want to receive suitable charging-stop recommendations so that I can complete journeys that require additional charging.

**Acceptance criteria:**

1. The system identifies charging stations along or near the planned route.
2. The system checks connector compatibility against the selected vehicle.
3. The system considers estimated battery availability and a safety reserve.
4. The system displays relevant charging station information.
5. The system does not present unknown availability as confirmed availability.
6. The user can review the recommended charging stops.

**Priority:** Must Have

## US-07: Scan Vehicle Dashboard

**User story:**

As an EV owner, I want to scan my vehicle dashboard using my phone camera so that I can record important vehicle information easily.

**Acceptance criteria:**

1. The user can capture or upload a dashboard photograph.
2. The system processes the photograph.
3. The system extracts supported visible readings.
4. The system displays extracted values for review.
5. The user can correct incorrect readings.
6. The user must confirm the readings before they are saved as confirmed data.
7. The system informs the user when a reading cannot be reliably extracted.

**Priority:** Must Have

## US-08: View Vehicle Reading History

**User story:**

As an EV owner, I want to view my previous dashboard readings so that I can understand how my vehicle's battery information changes over time.

**Acceptance criteria:**

1. The system saves confirmed readings with timestamps.
2. The user can view historical readings.
3. The system displays battery percentage and other available readings.
4. The user can identify the date and time of each reading.
5. The system distinguishes confirmed readings from unconfirmed extraction results.

**Priority:** Must Have

## US-09: Track Completed Journeys

**User story:**

As an EV owner, I want to save completed journeys so that I can monitor my driving history and vehicle efficiency.

**Acceptance criteria:**

1. The user can save completed trip information.
2. The system records available trip distance.
3. The system records available starting and ending battery readings.
4. The system calculates efficiency when sufficient reliable data is available.
5. The user can view previous trips.
6. The system avoids calculating misleading efficiency values when essential data is missing.

**Priority:** Must Have

## US-10: Compare EV and Fuel Vehicle Costs

**User story:**

As a potential EV buyer, I want to compare the running costs of an electric vehicle and a petrol or diesel vehicle so that I can understand the potential financial savings.

**Acceptance criteria:**

1. The user can select an electric vehicle.
2. The user can select a petrol or diesel comparison vehicle.
3. The user can enter average daily or monthly driving distance.
4. The application uses identifiable electricity tariffs and fuel prices.
5. The user can adjust consumption and price assumptions.
6. The system calculates estimated electricity and fuel costs.
7. The system displays cost per kilometre.
8. The system displays daily, monthly and annual running costs.
9. The system calculates estimated running-cost savings.
10. The system displays the assumptions used in the comparison.

**Priority:** Must Have

## US-11: View Long-Term Ownership Cost

**User story:**

As a potential EV buyer, I want to compare long-term ownership costs so that I can make a better vehicle purchasing decision.

**Acceptance criteria:**

1. The user can enter or review vehicle purchase prices.
2. The system supports estimated maintenance costs.
3. The system considers running costs over a selected ownership period.
4. The system can include depreciation and resale-value assumptions when reliable data is available.
5. The system displays the estimated total ownership cost.
6. The system explains the assumptions used.

**Priority:** Future

## US-12: Use the AI EV Assistant

**User story:**

As an EV owner, I want to ask questions about my vehicle and journeys so that I can receive relevant assistance.

**Acceptance criteria:**

1. The user can submit questions through a conversational interface.
2. The assistant can retrieve relevant available vehicle information.
3. The assistant can use authorized trip and charging information.
4. The assistant provides answers based on available information.
5. The assistant distinguishes estimates from confirmed information.
6. The assistant indicates when it cannot verify an answer.

**Priority:** Should Have

## US-13: Earn Eco-Driving Rewards

**User story:**

As an EV owner, I want to earn rewards for efficient driving so that I am encouraged to improve my driving habits.

**Acceptance criteria:**

1. The system evaluates eligible journey information.
2. The system calculates an efficiency score using defined rules.
3. The system awards points for eligible achievements.
4. The user can view their points and badges.
5. The system displays historical progress.
6. Rewards must not encourage unsafe driving behaviour.

**Priority:** Future

## US-14: Browse the EV Marketplace

**User story:**

As a potential EV buyer, I want to browse electric vehicle listings so that I can discover vehicles available for purchase.

**Acceptance criteria:**

1. The user can browse available EV listings.
2. The user can search by brand and model.
3. The user can filter listings by price.
4. The application displays vehicle photographs and specifications.
5. The application displays listing and seller information according to privacy rules.
6. The user can save favourite listings.

**Priority:** Future

# 4. MVP User Story Prioritization

The first release will focus on the following user stories:

| User Story | Feature | Priority |
|---|---|---|
| US-01 | User Registration | Must Have |
| US-02 | User Login | Must Have |
| US-03 | Add an Electric Vehicle | Must Have |
| US-04 | Discover Charging Stations | Must Have |
| US-05 | Plan an EV Journey | Must Have |
| US-06 | Recommend Charging Stops | Must Have |
| US-07 | Scan Vehicle Dashboard | Must Have |
| US-08 | View Vehicle Reading History | Must Have |
| US-09 | Track Completed Journeys | Must Have |
| US-10 | Compare EV and Fuel Vehicle Costs | Must Have |
| US-12 | AI EV Assistant | Limited MVP |

US-11, US-13 and US-14 will be implemented in future releases.

# 5. Conclusion

These user stories and acceptance criteria provide a user-centred foundation for the development of EV Navigator.

They will guide feature implementation, testing and validation.

Each user story will be reviewed and refined as development progresses and feedback is collected from actual users.
