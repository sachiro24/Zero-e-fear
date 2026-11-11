# EV Navigator – User Journey Design

## 1. Introduction

This document defines the primary user journeys and interactions within EV Navigator.

The purpose is to understand how users navigate the application, complete important tasks and interact with its core features before beginning detailed UI/UX design and implementation.

## 2. User Types

### 2.1 Existing EV Owner
An individual who owns an electric vehicle and wants to plan journeys, locate charging stations and monitor vehicle performance.

### 2.2 Potential EV Buyer
An individual interested in purchasing an electric vehicle who wants to compare EVs with conventional fuel vehicles and understand potential savings.

### 2.3 EV Enthusiast
An individual interested in vehicle efficiency, EV technology, achievements and marketplace information.

## 3. Main User Journeys

### Journey 1: Plan an EV Trip

**Goal:** Allow an EV owner to plan a journey with estimated battery consumption and suitable charging stops.

**Steps:**
1. User opens EV Navigator.
2. User selects their registered EV.
3. User enters the starting point and destination.
4. User provides or confirms the current battery percentage.
5. Application retrieves available route and charging station information.
6. Application estimates battery consumption and arrival battery percentage.
7. If necessary, application recommends compatible charging stops.
8. User reviews the route, distance, estimated travel time and charging requirements.
9. User confirms the planned journey.
10. Application records trip information and allows the user to save the completed journey.

**Expected outcome:** The user receives a vehicle-aware journey plan with transparent battery and charging estimates.

### Journey 2: EV Snapshot AI

**Goal:** Allow users to record dashboard readings and build a history of their vehicle's performance.

**Steps:**
1. User opens EV Snapshot AI.
2. User selects their registered vehicle.
3. User takes or uploads a dashboard photograph.
4. AI extracts visible information such as battery percentage, displayed range and odometer reading.
5. Application displays the extracted values and confidence information where available.
6. User reviews and corrects the values.
7. User confirms the readings.
8. Application stores the confirmed readings with a timestamp.
9. Historical readings become available for vehicle-efficiency analysis.

**Expected outcome:** Users can maintain a reliable history of vehicle readings and improve personalized efficiency estimates.

### Journey 3: EV Savings Intelligence

**Goal:** Help users compare the running and ownership costs of electric and conventional fuel vehicles.

**Steps:**
1. User opens EV Savings Intelligence.
2. User selects an electric vehicle.
3. User selects a petrol or diesel comparison vehicle.
4. User enters average daily or monthly driving distance.
5. Application displays applicable fuel prices and electricity tariffs.
6. User reviews or adjusts vehicle consumption and energy-price assumptions.
7. Application calculates estimated running costs.
8. Application displays potential savings over daily, monthly and annual periods.
9. User optionally compares maintenance costs and total ownership costs.

**Expected outcome:** Users understand the estimated financial differences between EV and conventional vehicle ownership.

### Journey 4: Eco-Driving and Rewards

**Goal:** Encourage efficient and safe driving through achievements and rewards.

**Steps:**
1. User completes a journey.
2. Application evaluates available and validated efficiency information.
3. An efficiency score is calculated.
4. User receives eligible points or achievements.
5. Application updates the user's progress.
6. User views historical scores and milestones.

**Expected outcome:** Users are encouraged to improve energy efficiency without compromising driving safety.

### Journey 5: EV Marketplace

**Goal:** Allow users to discover and compare new and used electric vehicles.

**Steps:**
1. User opens the EV Marketplace.
2. User searches by brand, model or price.
3. User applies relevant filters.
4. Application displays matching vehicle listings.
5. User opens a listing.
6. Application displays photographs, specifications, price and seller information.
7. User saves the listing or contacts the seller.

**Expected outcome:** Users can research and compare EV listings through one platform.

### Journey 6: AI EV Assistant

**Goal:** Provide an intelligent conversational interface for EV-related assistance.

**Steps:**
1. User opens the AI EV Assistant.
2. User enters an EV-related question.
3. Application identifies the information needed.
4. Assistant retrieves relevant information through authorized application services.
5. Assistant generates a response based on available information.
6. User receives an explanation, recommendation or relevant estimate.

**Expected outcome:** Users can interact with EV Navigator using natural language.

## 4. Main Application Navigation

The initial mobile application will include four main navigation sections:

1. **Home:** Vehicle overview, battery information, shortcuts and important insights.
2. **Explore:** Charging stations, route planning and marketplace discovery.
3. **Insights:** Dashboard readings, trip history, vehicle efficiency and savings.
4. **Profile:** Account settings, registered vehicles, preferences and privacy settings.

The AI EV Assistant will be accessible from the home dashboard.

## 5. MVP User Journeys

The first release will prioritize:

- Account registration and authentication.
- Adding and managing a vehicle.
- Charging station discovery.
- EV trip planning.
- Dashboard photo scanning with user confirmation.
- Trip history and basic efficiency analytics.
- EV versus fuel vehicle running-cost comparison.
- Limited AI assistant functionality.

Eco-driving rewards and the complete marketplace experience will be developed in later releases.

## 6. Important User Experience Considerations

- Users must be able to correct AI-extracted dashboard readings before saving.
- The application must distinguish estimated values from confirmed values.
- Users should be able to edit their vehicle specifications.
- Charging station information should display its last verification time where available.
- Battery predictions should include clear assumptions and uncertainty.
- Cost comparisons should show the fuel prices, electricity tariffs and consumption assumptions used.
- Users should have control over their personal data and uploaded photographs.
- The application must not encourage unsafe driving to achieve rewards.

## 7. Conclusion

These user journeys establish the initial interaction model for EV Navigator.

They provide a foundation for subsequent UI/UX wireframes, system architecture, database design and API specification.

The journeys will be refined through user feedback and technical validation before implementation.
