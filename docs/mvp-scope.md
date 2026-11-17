# ZERO FEAR – MVP Scope

## 1. MVP Objective

Develop an initial usable version of ZERO FEAR for Sri Lankan EV owners.

The MVP will demonstrate the core value of personal EV intelligence by allowing users to manage their electric vehicles, record dashboard readings, maintain vehicle history and access basic vehicle insights.

The initial release will establish the technical and functional foundation for expanding ZERO FEAR into a broader EV ecosystem.

## 2. Core MVP Modules

### 2.1 User Authentication

**Objective:** Allow users to create accounts and securely access their personal vehicle information.

Features:
- User registration.
- User login.
- Basic account management.
- Secure authentication.
- Protected access to personal information.

### 2.2 Vehicle Management

**Objective:** Allow users to register and manage their electric vehicles.

Features:
- Register an EV.
- Select manufacturer, model, variant and year.
- Display available vehicle specifications.
- Manage registered vehicles.
- Select a primary or active vehicle.
- Edit and remove registered vehicles.

### 2.3 AI Dashboard Scanner

**Objective:** Allow users to record vehicle dashboard information using AI-assisted image recognition.

Features:
- Capture dashboard photographs using the mobile camera.
- Upload dashboard photographs.
- Extract battery percentage.
- Extract displayed remaining range.
- Extract odometer reading where visible.
- Display extracted values for review.
- Allow users to correct extracted values.
- Confirm and save readings.
- Provide manual reading entry when image processing fails.

### 2.4 Vehicle Insights

**Objective:** Provide users with a history of recorded vehicle information and basic performance observations.

Features:
- Dashboard reading history.
- Timestamped vehicle readings.
- Battery percentage history.
- Displayed range history.
- Recorded trip information where available.
- Basic battery and efficiency observations.
- Basic efficiency calculations when sufficient reliable data is available.

## 3. Subsequent Release Modules

The following modules are part of the product direction but will be developed after the initial MVP foundation.

### 3.1 Charging Discovery

**Objective:** Help EV owners discover charging stations and review relevant station information.

Features:
- Charging station map.
- Search for charging stations.
- Station details.
- Connector information.
- Charging power.
- Station filters.
- Pricing and availability where reliable data is available.
- Last verification time where available.

### 3.2 EV Trip Planning

**Objective:** Help EV owners plan journeys using vehicle information and estimated battery consumption.

Features:
- Starting location and destination.
- Registered vehicle selection.
- Current battery input.
- Route alternatives.
- Estimated journey distance and duration.
- Estimated battery consumption.
- Predicted arrival battery percentage.
- Recommended charging stops where necessary.
- Charging connector compatibility checks.

### 3.3 EV Marketplace

**Objective:** Allow users to discover and compare available electric vehicles.

Features:
- Browse EV listings.
- Search by manufacturer and model.
- Filters for price and vehicle condition.
- View vehicle photographs.
- View listing details.
- Review vehicle specifications and seller information.

The initial marketplace experience will focus on browsing and discovering listings. Advanced seller management and transaction workflows will be developed later.

## 4. Future Capabilities

The following features represent the longer-term ZERO FEAR product vision.

- Advanced battery analytics.
- Personalised energy consumption prediction.
- EV versus petrol and diesel running-cost comparison.
- Long-term vehicle ownership cost analysis.
- Eco-driving rewards and challenges.
- Community charging assistance.
- Advanced AI EV Assistant.
- Marketplace seller management.
- Emergency charging support.
- Connected-vehicle integrations where technically supported.

These features will be evaluated and prioritized based on user feedback, available data and development resources.

## 5. MVP Priorities

Development will follow a staged approach.

### 5.1 Initial MVP – Core Foundation

The first implementation will prioritize:

1. Authentication and account management.
2. Vehicle registration and management.
3. Home dashboard.
4. Manual dashboard reading entry.
5. AI dashboard scanning prototype.
6. Reading review, correction and confirmation.
7. Vehicle reading history.
8. Basic vehicle insights.

### 5.2 Subsequent Development

After the initial foundation is stable:

1. Charging station discovery.
2. Basic vehicle-aware trip planning.
3. Route alternatives and battery estimates.
4. Charging-stop recommendations.
5. Journey history and detailed trip records.
6. EV Marketplace browsing.

### 5.3 Future Development

Advanced capabilities will be introduced incrementally:

- Advanced AI assistance.
- Battery analytics and personalized predictions.
- EV running-cost comparisons.
- Rewards and achievements.
- Marketplace seller functionality.
- Connected-vehicle services.

## 6. Important Data Principles

### 6.1 Dashboard Reading Accuracy
- AI-extracted readings must remain pending until confirmed by the user.
- Users must be able to correct extracted values before saving.
- Confirmed readings must include timestamps and vehicle references.
- Manual entry must be available as a fallback.

### 6.2 Battery and Range Information
- Displayed range must not be treated as actual battery capacity.
- Battery percentage, displayed range and odometer readings must be treated as separate values.
- Estimated predictions must be clearly labelled.
- Battery predictions must communicate their assumptions and limitations.

### 6.3 Vehicle Specifications
- Vehicle specifications should come from verified or identifiable sources.
- The application should distinguish manufacturer-provided specifications from user-entered information.
- Users should be able to review and correct vehicle details where appropriate.

### 6.4 Charging Station Information
- Charging availability should only be displayed as live when supported by reliable data.
- Unknown or outdated information must be clearly identified.
- Connector compatibility should be checked against the selected vehicle where sufficient information is available.
- Pricing information should identify its source and verification status where possible.

### 6.5 Vehicle Insights
- Efficiency calculations should only be performed when sufficient reliable data is available.
- The application must avoid presenting misleading performance conclusions.
- Historical readings should be associated with the correct vehicle.

## 7. MVP Limitations

The MVP is an initial product release intended to validate the core application concept.

The initial release will have the following limitations:

1. Direct integration with every EV manufacturer's vehicle systems will not be available.
2. Dashboard image recognition may not accurately recognize every vehicle dashboard.
3. AI-extracted readings will require user verification.
4. Real-time charging availability will not be guaranteed across all charging stations.
5. Battery consumption and journey predictions will depend on available vehicle and route information.
6. Advanced battery health analysis will not initially be provided.
7. Full AI assistant functionality will not be available in the initial release.
8. Marketplace transactions and seller management will not initially be supported.
9. Advanced rewards and community features will not be included.

## 8. MVP Success Criteria

The initial MVP will be considered functionally successful when:

1. A user can register and log in.
2. A user can add and manage an electric vehicle.
3. A user can access the Home dashboard.
4. A user can manually enter vehicle readings.
5. A user can capture or upload a dashboard photograph for AI-assisted extraction.
6. A user can review, correct and confirm extracted readings.
7. Confirmed readings are saved with timestamps and associated with the correct vehicle.
8. A user can view historical vehicle readings.
9. Basic vehicle insights can be displayed using available confirmed data.
10. The application can be tested on an Android device.

## 9. Conclusion

The ZERO FEAR MVP will establish the foundation of a personal EV intelligence platform.

The initial focus is on vehicle management, dashboard reading collection, historical records and basic vehicle insights.

Charging discovery, EV trip planning and marketplace functionality will expand the platform through subsequent releases.

Advanced AI capabilities, rewards, financial comparisons and connected-vehicle services will form part of the longer-term product vision.

This staged approach allows ZERO FEAR to develop into a comprehensive EV ecosystem while keeping the initial implementation achievable and technically manageable.
