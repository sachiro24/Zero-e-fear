
# ZERO FEAR – UI/UX Design System

## 1. Design Vision

ZERO FEAR follows a futuristic EV technology design direction.

The interface should communicate:
- Intelligence.
- Confidence.
- Simplicity.
- Modern electric mobility.
- Reliability.

The design should create a premium technology experience without unnecessary visual complexity.

The primary focus is presenting vehicle information, battery readings and EV-related services in a clear and accessible way.

## 2. Colour Palette

The application uses a dark navy foundation with electric green and blue accents.

### 2.1 Primary Colour Palette

| Element | Colour | Hex |
|---|---|---|
| Primary Background | Dark Navy | #0B1220 |
| Secondary Surface | Dark Blue Grey | #151F30 |
| Primary Accent | Electric Green | #39E58C |
| Secondary Accent | Electric Blue | #38BDF8 |
| Primary Text | White | #F8FAFC |
| Secondary Text | Slate Grey | #94A3B8 |

### 2.2 Colour Usage Guidelines

**Dark Navy – #0B1220**
- Main application background.
- Primary screen backgrounds.

**Dark Blue Grey – #151F30**
- Cards and content surfaces.
- Input fields.
- Secondary containers.

**Electric Green – #39E58C**
- Primary action buttons.
- Important battery indicators.
- Selected states and positive status indicators.
- Important highlights.

**Electric Blue – #38BDF8**
- Secondary actions.
- Informational highlights.
- Map and navigation-related elements.

**White – #F8FAFC**
- Main headings.
- Important information.
- Primary numerical values.

**Slate Grey – #94A3B8**
- Secondary labels.
- Descriptions.
- Supporting information.

Colours should have consistent meanings throughout the application.

## 3. Typography

**Primary typeface:** Inter.

Typography should provide:
- Clear readability.
- Consistent heading hierarchy.
- Easy-to-read numerical values.
- Consistent labels and descriptions.
- Appropriate contrast between primary and secondary information.

### Typography Guidelines

- Use prominent headings for important screen titles.
- Use medium-weight text for section headings.
- Use readable body text for descriptions and instructions.
- Use clear numerical typography for battery percentages, distance, range and charging power.
- Keep supporting labels visually secondary.
- Avoid excessive font-weight and size variations.

Numerical values should be easy to identify because vehicle information is a major part of the application.

## 4. Themes

The application will support two visual themes.

### 4.1 Dark Theme

The primary design theme.

Characteristics:
- Dark navy backgrounds.
- Dark blue-grey surfaces.
- Electric green highlights.
- Electric blue informational accents.
- White primary text.
- Slate grey secondary text.

The dark theme should establish the futuristic EV technology identity.

### 4.2 Light Theme

A complementary light appearance.

Characteristics:
- Light neutral backgrounds.
- White or light-coloured content surfaces.
- Dark readable primary text.
- Suitable secondary text colours.
- Consistent green and blue accent colours.

The light theme must maintain sufficient contrast and preserve the same visual hierarchy as the dark theme.

Both themes should use consistent component layouts and interaction patterns.

## 5. Design Principles

The following principles apply across all application screens:

1. **Minimal and Premium Appearance:** Maintain a modern and clean visual identity.
2. **One Primary Purpose Per Screen:** Each screen should focus on one main user task.
3. **Generous Spacing:** Avoid tightly packed content.
4. **Clear Visual Hierarchy:** Important information should be immediately identifiable.
5. **Avoid Overcrowded Interfaces:** Display essential information first.
6. **Progressive Disclosure:** Keep advanced information expandable.
7. **Clear Actions:** Important actions should be visually distinguishable.
8. **Consistent Navigation:** Maintain common navigation patterns.
9. **Readable Data Visualisations:** Charts should communicate useful vehicle information without unnecessary complexity.
10. **Mobile Usability:** Design for different mobile screen sizes and touch interactions.
11. **Consistent Feedback:** Provide clear visual feedback for loading, success, errors and empty states.
12. **Information Accuracy:** Clearly distinguish confirmed readings from estimated or unverified information.

## 6. Component Guidelines

### 6.1 Cards

Cards should:
- Use rounded corners.
- Use secondary surface colours.
- Have subtle borders where appropriate.
- Maintain clear content hierarchy.
- Use consistent internal spacing.
- Avoid unnecessary decorative elements.

Cards should be used for vehicle summaries, activity records, marketplace listings and other grouped information.

### 6.2 Buttons

Buttons should have clearly defined visual hierarchy.

**Primary Buttons**
- Use electric green.
- Use readable contrasting text.
- Represent the main action on a screen.

**Secondary Buttons**
- Use neutral or secondary surface colours.
- Represent supporting actions.

**Destructive Actions**
- Use a visually distinct warning or destructive treatment.
- Require appropriate confirmation for important irreversible actions.

Buttons should have clear pressed, disabled and loading states where applicable.

### 6.3 Forms and Input Fields

Forms should:
- Use clear labels.
- Provide helpful input instructions.
- Display validation messages.
- Maintain consistent spacing.
- Use appropriate keyboard types.
- Avoid requesting unnecessary information.

Complex registration processes should be divided into smaller steps.

### 6.4 Navigation

The application should maintain consistent navigation across all major sections.

The five primary navigation tabs are:
1. Home.
2. Insights.
3. Plan.
4. Discover.
5. Profile.

The selected tab should have a clear visual state.

Supporting modules such as My Garage should remain accessible without unnecessarily increasing the number of bottom-navigation tabs.

### 6.5 Maps

Map interfaces should:
- Prioritize geographical clarity.
- Use distinguishable map markers.
- Avoid unnecessary visual clutter.
- Provide clear selected-location indicators.
- Use collapsible bottom sheets for additional information.

Charging station details should be progressively displayed rather than placing every detail directly on the map.

### 6.6 Charts and Data Visualisations

Charts should:
- Be simple and readable.
- Use consistent visual indicators.
- Clearly identify units and time periods.
- Avoid unnecessary decoration.
- Display useful historical information.
- Distinguish estimated values from confirmed or recorded values.

### 6.7 Vehicle Cards

Vehicle cards should display relevant information such as:
- Vehicle image.
- Manufacturer and model.
- Variant and year.
- Latest confirmed battery percentage, when available.
- Displayed remaining range, when available.

The selected or primary vehicle should be clearly identifiable.

### 6.8 Bottom Sheets

Bottom sheets should be used for contextual information that does not require a separate screen.

Examples include:
- Charging station details.
- Map location information.
- Additional route information.
- Contextual actions.

Collapsed and expanded states should have clearly differentiated information levels.

### 6.9 Status Indicators

Status indicators should communicate information consistently.

Examples:
- Confirmed readings.
- Estimated values.
- Pending confirmation.
- Unavailable information.
- Successful operations.
- Errors and warnings.

Colour should not be the only method of communicating status. Text labels or other visual indicators should also be used.

## 7. Navigation Structure

The application uses five primary bottom-navigation sections.

| Section | Main Purpose |
|---|---|
| Home | Vehicle overview and important shortcuts |
| Insights | Historical information and efficiency analytics |
| Plan | EV journey planning |
| Discover | Charging station discovery and EV Marketplace |
| Profile | Account settings and preferences |

Additional modules:
- My Garage – accessible through Home and Profile.
- AI Dashboard Scanner – accessible through Home.
- AI EV Assistant – intended to be accessible through a floating shortcut.

## 8. Design Tools and Implementation

### 8.1 UI/UX Design Tool

Google Stitch is being used for:
- Screen exploration.
- Initial UI generation.
- Layout refinement.
- Visual design iteration.
- Reviewing individual screen concepts.

### 8.2 Mobile Application Implementation

The final designs will serve as references during React Native implementation.

The planned mobile technology stack is:
- React Native.
- Expo.
- TypeScript.

The implementation should maintain consistency with the approved design system.

### 8.3 Design Consistency

During implementation:
- Reusable components should be created for common UI elements.
- Colour values should be maintained centrally.
- Typography styles should be reusable.
- Spacing and layout conventions should remain consistent.
- Dark and light themes should use shared semantic design tokens.
- Individual screens should not introduce unrelated visual styles.

## 9. Accessibility and Usability

The interface should consider:
- Sufficient text and background contrast.
- Readable text sizes.
- Clear button labels.
- Appropriate touch-target sizes.
- Visible interaction states.
- Accessible descriptions for meaningful icons.
- Clear error and validation messages.
- Consistent interaction patterns.

Important information should remain understandable without relying exclusively on colour.

## 10. Design Status

Google Stitch is being used for iterative UI exploration and screen design.

The design workflow follows these stages:

1. Initial screen generation.
2. Layout and visual review.
3. Refinement and correction.
4. Interaction review.
5. Design approval.
6. Documentation for implementation.

A screen should only be marked **Approved** after its layout and interactions have been reviewed.

Screens that have been generated but not fully reviewed should remain **In Progress** or **Pending Review**.

The design system itself may also evolve as implementation reveals usability or technical requirements.

## 11. Conclusion

This design system establishes the visual identity, colour palette, typography, themes, component guidelines and usability principles of ZERO FEAR.

It provides a common reference for maintaining consistency across the application's screens and features.

The design system will guide Google Stitch design work and subsequent React Native implementation.
