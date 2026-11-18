# ZERO FEAR – Authentication and Security Plan

## 1. Overview

ZERO FEAR requires authentication and authorization to protect user accounts, vehicle information, dashboard readings and trip history.

Planned technologies:

- Django authentication
- Django REST Framework
- JWT authentication using Simple JWT
- HTTPS
- Expo SecureStore for mobile token storage
- Django permissions and resource ownership checks

## 2. User Registration

1. User enters their name, email and password.
2. React Native submits the registration form to Django over HTTPS.
3. Django validates the submitted information.
4. Django securely hashes the password.
5. The account is created.
6. The user receives registration confirmation.
7. Email verification can be included in the production registration flow.

## 3. User Login

1. User enters email and password.
2. The mobile app sends credentials to Django over HTTPS.
3. Django verifies the credentials.
4. Django issues access and refresh tokens.
5. The mobile app stores tokens securely.
6. The access token is included in protected API requests.

## 4. JWT Token Management

### Access Token

- Authorizes API requests.
- Has a relatively short lifetime.
- Sent in the Authorization header as a Bearer token.

### Refresh Token

- Used to obtain a new access token.
- Has a longer lifetime.
- Must be stored securely.
- Should support rotation and revocation policies.

Proposed initial configuration:

- Access token lifetime: 10 minutes.
- Refresh token lifetime: 7 days.

These are initial configuration proposals and should be reviewed during implementation.

## 5. Authorization and Permissions

Users must only access resources they own.

Examples:

- A user can view their own vehicles.
- A user can update their own vehicle information.
- A user can view their own dashboard readings.
- A user can view their own trip history.
- A user cannot access another user's private information.

Django must enforce ownership checks. Hiding information in the mobile interface is not sufficient.

## 6. Password Security

- Never store plain-text passwords.
- Use Django's password hashing.
- Validate password requirements.
- Provide a secure password-reset process.
- Avoid revealing whether an email address is registered during password recovery.

## 7. Mobile Application Security

- Store tokens using Expo SecureStore.
- Do not store passwords.
- Avoid storing sensitive authentication tokens in ordinary AsyncStorage.
- Use HTTPS in production.
- Clear authentication tokens on logout.
- Handle expired and invalid tokens appropriately.

## 8. Backend Security

- Validate input using Django REST Framework serializers.
- Protect private endpoints with authentication and permission checks.
- Verify resource ownership before accessing or modifying records.
- Keep secret keys in environment variables.
- Restrict database access to the backend.
- Validate uploaded file types and sizes.
- Configure production CORS and security settings appropriately.
- Apply rate limiting to sensitive endpoints where appropriate.

## 9. AI Scanner Security

Dashboard images may contain personal vehicle information.

The backend should:

- Validate uploaded images.
- Restrict image size and accepted formats.
- Control access to stored images.
- Avoid unnecessary image retention.
- Protect Vision API credentials.
- Require user confirmation before extracted values become confirmed readings.

## 10. Future Security Improvements

- Email verification.
- Refresh token rotation and revocation.
- Login rate limiting.
- Account and data deletion workflows.
- Audit logging for important security events.
- Additional protection for sensitive account operations.

## 11. Summary

ZERO FEAR will use JWT authentication, Django authorization, secure mobile token storage and HTTPS to protect user accounts and application data.

Security controls must be enforced by the backend rather than relying only on the mobile application interface.
