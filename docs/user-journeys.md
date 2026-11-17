# ZERO FEAR – User Journey Design

## 1. Introduction

This document defines the primary user journeys and interactions within ZERO FEAR, an electric vehicle ecosystem application designed initially for the Sri Lankan EV market.

The purpose is to understand how users navigate the application, complete important tasks and interact with its core features before implementation.

These journeys provide a foundation for UI/UX design, application architecture, database design and API development.

## 2. User Types

### 2.1 Existing EV Owner

An individual who owns an electric vehicle and wants to:
- Monitor vehicle information and battery readings.
- Record dashboard information.
- Plan journeys using battery-aware estimates.
- Discover suitable charging stations.
- Review driving history and vehicle efficiency.

### 2.2 Potential EV Buyer

An individual interested in purchasing an electric vehicle who wants to:
- Discover available electric vehicles.
- Compare vehicle specifications.
- Explore new and used EV listings.
- Understand potential running-cost differences between EVs and conventional vehicles.

### 2.3 EV Enthusiast

An individual interested in electric vehicle technology, vehicle efficiency, charging infrastructure, EV-related information and marketplace opportunities.

## 3. Main User Journeys

### Journey 1: User Registration and Vehicle Setup

**Goal:** Allow new users to create an account and register their electric vehicle before accessing personalized application features.

**Steps:**
1. User opens ZERO FEAR.
2. Application displays the welcome and onboarding screens.
3. User selects Register.
4. User enters the required account information.
5. Application creates the user account.
6. User proceeds to Add Vehicle.
7. User selects the vehicle manufacturer, model, variant and year.
8. Application displays the available vehicle information.
9. User reviews and confirms the vehicle details.
10. Application adds the vehicle to My Garage.
11. User may optionally proceed to the dashboard scanning feature.
12. User reaches the Home dashboard.

**Expected outcome:** The user creates an account, registers an EV and gains access to personalized vehicle features.

**Alternative flow:**
- Existing users can log in directly.
- If an existing user has already registered a vehicle, the application takes them to Home.
- If no vehicle is registered, the application prompts them to add one.
- Dashboard scanning is optional during initial setup.

### Journey 2: Plan an EV Trip

**Goal:** Allow an EV owner to plan a journey using estimated battery consumption and suitable charging stops.

**Steps:**
1. User opens the Plan section.
2. User selects their registered EV.
3. User enters the starting point and destination.
4. User confirms the current battery percentage.
5. Application retrieves available route and charging station information.
6. Application estimates energy consumption and arrival battery percentage.
7. Application checks whether the selected vehicle has sufficient estimated battery capacity for the journey.
8. If necessary, the application recommends suitable charging stops.
9. User reviews the recommended route and available alternatives.
10. User reviews distance, estimated travel time, predicted arrival battery and charging requirements.
11. User selects a suitable route.
12. Application displays the selected journey plan.
13. Where supported, the user can proceed to active navigation.
14. After completing the journey, the application can save the journey information to the user's history.

**Expected outcome:** The user receives a vehicle-aware journey plan with transparent battery and charging estimates.

**Alternative flow:**
- If the battery is insufficient, the application recommends suitable charging stops.
- If charging station information is unavailable, the application should communicate the limitation.
- Users should be able to modify their starting battery percentage or destination and recalculate the route.

### Journey 3: EV Snapshot AI – Dashboard Scanning

**Goal:** Allow users to record dashboard readings using AI-assisted image recognition and build a history of their vehicle's performance.

**Steps:**
1. User opens the Home dashboard.
2. User selects the EV Snapshot AI scanner.
3. User selects their registered vehicle if multiple vehicles are available.
4. User captures or uploads a dashboard photograph.
5. Application sends the image for AI processing.
6. AI extracts visible information such as:
   - Battery percentage.
   - Displayed remaining range.
   - Odometer reading, where visible.
7. Application displays the extracted values.
8. User reviews the extracted information.
9. User corrects any inaccurate values.
10. User confirms the readings.
11. Application stores the confirmed readings with a timestamp and vehicle reference.
12. The readings become available in the vehicle's reading history.
13. Historical readings can contribute to vehicle-efficiency analysis.

**Expected outcome:** Users can maintain a reliable history of confirmed dashboard readings and improve personalized vehicle insights.

**Alternative flow:**
- If the image is unclear, the application asks the user to capture another photograph.
- If AI extraction fails, users can enter the readings manually.
- AI-extracted values must not be treated as confirmed records until the user reviews and confirms them.

### Journey 4: EV Savings Intelligence

**Goal:** Help users compare the running costs of electric and conventional fuel vehicles.

**Steps:**
1. User opens EV Savings Intelligence.
2. User selects an electric vehicle.
3. User selects a petrol or diesel comparison vehicle.
4. User enters their average daily or monthly driving distance.
5. Application displays the applicable fuel prices and electricity tariffs, where reliable data is available.
6. User reviews or adjusts vehicle consumption and energy-price assumptions.
7. Application calculates estimated running costs.
8. Application displays estimated savings over daily, monthly and annual periods.
9. User optionally explores maintenance expenses and total ownership costs.

**Expected outcome:** Users understand the estimated financial differences between EV and conventional vehicle ownership.

**Note:** This feature is planned for a later release. Cost calculations must clearly display the assumptions, energy prices and consumption figures used.

### Journey 5: Eco-Driving and Rewards

**Goal:** Encourage efficient and responsible driving through achievements and rewards.

**Steps:**
1. User completes a journey.
2. Application evaluates available and validated journey information.
3. Application calculates an efficiency score using supported metrics.
4. User receives eligible points or achievements.
5. Application updates the user's progress.
6. User views historical scores, achievements and milestones.

**Expected outcome:** Users are encouraged to improve energy efficiency without compromising safe driving practices.

**Note:** Eco-driving rewards are planned for a later release. The application must not encourage unsafe driving behaviour to achieve higher scores.

### Journey 6: EV Marketplace

**Goal:** Allow users to discover and compare new and used electric vehicles.

**Steps:**
1. User opens the Discover section.
2. User selects EV Marketplace.
3. User searches by manufacturer, model or price.
4. User applies relevant filters, such as new or used vehicles.
5. Application displays matching vehicle listings.
6. User opens a listing.
7. Application displays vehicle photographs, specifications, price and seller information.
8. User reviews the available information.
9. User saves the listing or contacts the seller.

**Expected outcome:** Users can discover and compare EV listings through one platform.

**Note:** Marketplace discovery is included in the product direction. Advanced seller management and transaction workflows can be developed in later releases.

### Journey 7: AI EV Assistant

**Goal:** Provide an intelligent conversational interface for EV-related assistance.

**Steps:**
1. User opens the AI EV Assistant through its application shortcut.
2. User enters an EV-related question.
3. Application identifies the information required.
4. Assistant retrieves relevant information through authorized application services, where available.
5. Assistant generates a response based on available and relevant information.
6. User receives an explanation, recommendation or estimate.
7. Where appropriate, the assistant directs the user to relevant application features.

**Expected outcome:** Users can interact with ZERO FEAR using natural language to obtain EV-related assistance.

**Note:** The AI EV Assistant will be introduced progressively. Responses involving vehicle information, battery readings, charging prices or route estimates must be grounded in available data and clearly identify uncertainty.

## 4. Main Application Navigation

The mobile application will use five main bottom-navigation sections.

### 4.1 Home
Provides an overview of the user's registered vehicle and important information.

Main interactions:
- View selected vehicle.
- View latest confirmed battery percentage and displayed range.
- Open the dashboard scanner.
- Access My Garage.
- View recent activity.
- Access trip planning and charging discovery shortcuts.
- View a brief efficiency summary.

### 4.2 Insights
Provides historical information and vehicle-performance analytics.

Main interactions:
- View vehicle efficiency summaries.
- Explore journey history.
- View journey details.
- Review battery reading history.
- View individual reading details.
- Explore charging history.
- Access the full vehicle logbook.

### 4.3 Plan
Provides vehicle-aware journey planning.

Main interactions:
- Enter starting point and destination.
- Select a registered vehicle.
- Confirm current battery percentage.
- Review route analysis.
- Compare alternative routes.
- Identify recommended charging stops.
- Access active navigation where supported.

### 4.4 Discover
Provides access to EV-related locations and marketplace information.

Main interactions:
- Explore charging stations on a map.
- Search and filter charging stations.
- View station details.
- Review connector types and charging power.
- Explore the EV Marketplace.
- View vehicle listings and seller information.

### 4.5 Profile
Provides account settings and personal application management.

Main interactions:
- View and update profile information.
- Access My Garage.
- Manage application preferences.
- Configure notifications.
- Review privacy and security settings.
- Access support and application information.
- Log out.

### Additional Application Access

**My Garage:** A supporting module accessible through Home and Profile. It allows users to add, edit, remove and select their registered vehicles.

**EV Snapshot AI:** Accessible through a prominent scanner shortcut on Home.

**AI EV Assistant:** Intended to be accessible through a floating shortcut across relevant application screens.

## 5. MVP User Journeys and Release Priorities

The first release will focus on delivering a functional foundation for vehicle management, dashboard reading records and basic vehicle insights.

### 5.1 Initial MVP

Priority journeys:
- Account registration and authentication.
- Adding and managing a registered EV.
- Viewing the Home dashboard.
- Manually entering dashboard readings.
- AI-assisted dashboard scanning prototype.
- Reviewing, correcting and confirming extracted readings.
- Viewing battery reading history.
- Basic vehicle insights.

### 5.2 Subsequent Development

Features to introduce after the initial foundation:
- Charging station discovery.
- Vehicle-aware trip planning.
- Journey history and journey details.
- Charging history.
- More detailed vehicle-efficiency analytics.
- EV versus fuel vehicle running-cost comparison.

### 5.3 Future Features

Features intended for later development:
- Advanced active navigation.
- Complete AI EV Assistant.
- Eco-driving rewards and achievements.
- Advanced EV Marketplace functionality.
- Seller management and transaction workflows.
- Additional connected-vehicle and telemetry capabilities, subject to technical availability.

## 6. Important User Experience Considerations

### 6.1 Data Accuracy
- Users must be able to correct AI-extracted dashboard readings before saving.
- AI-extracted values must remain unconfirmed until the user approves them.
- The application must distinguish estimated values from confirmed values.
- Vehicle specifications should be editable where appropriate.

### 6.2 Battery and Range Information
- Displayed remaining range must be distinguished from actual driving efficiency.
- Battery predictions should include clear assumptions and uncertainty.
- The application must not present estimated arrival battery percentages as guaranteed results.

### 6.3 Charging Station Information
- Charging station information should display its last verification time where available.
- Connector compatibility and charging power should be clearly presented.
- Live availability must only be displayed when reliable live data is available.

### 6.4 Cost and Efficiency Calculations
- Cost comparisons should show the fuel prices, electricity tariffs and consumption assumptions used.
- Users should be able to adjust relevant assumptions.
- Efficiency insights should be based on available and sufficiently reliable records.

### 6.5 Privacy and Security
- Users should have control over their personal information and uploaded dashboard photographs.
- Vehicle and reading records should be associated with the appropriate user account.
- Access to personal data must be appropriately protected.

### 6.6 Safe and Clear Interactions
- The application must not encourage unsafe driving to achieve rewards.
- Important actions should provide clear feedback.
- Users should be able to recover from errors and correct information.
- The interface should avoid displaying too much information at once.
- Each screen should have a clear primary purpose.

## 7. Conclusion

These user journeys establish the initial interaction model for ZERO FEAR.

They describe how users register vehicles, record dashboard readings, plan journeys, discover charging stations, review vehicle insights and access other EV-related services.

The journeys will guide the application's screen design, navigation structure, technical architecture, database design and API development.

They will be refined through user feedback and technical validation before and during implementation.
