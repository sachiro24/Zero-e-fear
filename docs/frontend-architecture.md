# ZERO FEAR – Frontend Architecture

## 1. Overview

The ZERO FEAR mobile application will use React Native, Expo and TypeScript. The first release targets Android, with the architecture allowing iOS support later.

The frontend is responsible for presentation, navigation, camera interaction, user input, local interface state and communication with the Django backend.

## 2. Main Frontend Responsibilities

- Display onboarding, authentication and application screens.
- Provide five-tab navigation: Home, Insights, Plan, Discover and Profile.
- Support vehicle selection and garage management.
- Capture dashboard images using the device camera.
- Display AI-extracted values for user review and confirmation.
- Display reading history, insights and trip information.
- Communicate with backend APIs.
- Store authentication tokens securely.

## 3. Navigation Structure

### Authentication Flow

- Splash
- Welcome / onboarding
- Login
- Registration
- Forgot password

### Main Navigation

1. Home
2. Insights
3. Plan
4. Discover
5. Profile

My Garage is a supporting module accessible from Home and Profile rather than a separate bottom tab.

Discover contains charging discovery and the EV marketplace.

An AI Assistant floating shortcut is planned for a later stage.

## 4. Proposed Project Structure

```text
ev-navigator/
├── app/
│   ├── (auth)/
│   │   ├── login.tsx
│   │   ├── register.tsx
│   │   └── forgot-password.tsx
│   ├── (tabs)/
│   │   ├── index.tsx
│   │   ├── insights.tsx
│   │   ├── plan.tsx
│   │   ├── discover.tsx
│   │   └── profile.tsx
│   ├── garage/
│   ├── scanner/
│   └── _layout.tsx
├── src/
│   ├── components/
│   ├── features/
│   │   ├── auth/
│   │   ├── vehicles/
│   │   ├── scanner/
│   │   ├── insights/
│   │   ├── trips/
│   │   ├── charging/
│   │   └── marketplace/
│   ├── services/
│   │   ├── api.ts
│   │   └── ...
│   ├── hooks/
│   ├── context/
│   ├── types/
│   ├── constants/
│   └── utils/
├── assets/
└── package.json
```

This is a proposed structure and should be adapted to the existing Expo starter project rather than forcing unnecessary restructuring.

## 5. Frontend Layers

### Screens and Navigation

Expo Router can organize route files and navigation layouts.

### Reusable Components

Shared interface elements such as buttons, input fields, cards, loading indicators, error messages and vehicle summaries.

### Feature Modules

Feature-specific UI and logic grouped by domain, such as vehicles, scanner, trips and insights.

### API Services

A centralized API client should manage the backend base URL, request headers, authentication tokens, response handling and common errors.

### State Management

Use local component state for isolated UI state. Introduce shared context or a suitable state library only when state must be shared across screens.

### Types

Define TypeScript types for users, vehicles, scans, readings and trips. Keep them aligned with backend API contracts.

## 6. API Communication

- Communicate with Django through HTTPS REST APIs.
- Send JSON for normal requests.
- Use multipart form data for image uploads.
- Include access tokens for protected endpoints.
- Handle loading, success, empty and error states.
- Do not put private third-party API keys in frontend code.

## 7. Security

- Store authentication tokens using Expo SecureStore.
- Do not store passwords.
- Clear tokens on logout.
- Treat backend authorization as the source of truth.
- Validate user input on both frontend and backend.

## 8. Implementation Priority

Initial frontend priorities:

1. Navigation and application shell.
2. Authentication screens.
3. Home and vehicle management.
4. Manual readings and scanner UI.
5. Reading history and basic insights.
6. API integration and error states.

Other screens may be implemented as subsequent MVP features.
