# WorkWise

## Overview

WorkWise is a Progressive Web App (PWA) designed as a comprehensive gateway to BPO (Business Process Outsourcing) and VA (Virtual Assistant) careers. It serves as a platform connecting talented individuals with opportunities in the remote work industry, offering free training programs, job postings, recruitment events, and direct contact channels for career advancement.

The app is built as a single-page application with a mobile-first responsive design, featuring a bottom navigation bar for seamless section switching. It aims to bridge the gap between aspiring professionals and the growing demand for skilled virtual assistants and BPO workers.

## Features

### Core Sections
- **Home**: Welcome message introducing the platform and listing available free services including VA training, call center basics, interview coaching, and resume makeovers.
- **Classes**: Interactive training schedule table displaying available courses (Basic VA, English, BPO 101) with embedded Tally.so enrollment modals and time slots.
- **Events**: Showcase of upcoming recruitment events including on-site interviews and online webinars with detailed dates and locations.
- **Jobs**: Current job postings for positions like Customer Service Rep and General Virtual Assistant, complete with salary ranges and direct apply buttons.
- **Connect**: Comprehensive step-by-step application instructions including resume review, cover letter creation, email submission guidelines, and confirmation process.

### Technical Features
- **Splash Screen**: Full-screen animated company logo display with fade-out transition on app load, occupying entire viewport.
- **Responsive Design**: Optimized for mobile devices with adaptive layouts and touch-friendly navigation.
- **Progressive Web App**: Installable on mobile devices with offline capabilities and native app-like experience.
- **Smooth Animations**: CSS transitions, fade-in effects, and splash screen animations for enhanced user experience.
- **Custom Header**: Logo on left, dynamic title in center, chat icon placeholder on right.
- **Bottom Navigation**: Fixed navigation bar for easy access to all sections.

## Usage Instructions

1. **Accessing the App**: Open `index.html` in any modern web browser. The app will display a splash screen with the company logo for 5 seconds before loading the main interface.
2. **Navigation**: Use the bottom navigation bar to switch between sections (Home, Classes, Events, Jobs, Connect). The header displays the company icon on the left, current section title in the center, and a chat icon placeholder on the right.
3. **Enrollment**: Click "Enroll" buttons in the Classes section to open embedded Tally.so enrollment modals.
4. **Event Registration**: Click "Register" links in Events to open Tally.so registration modals.
5. **Job Applications**: Use "Apply Now" buttons to navigate to the Connect section with application instructions.
5. **PWA Installation**: On supported browsers, use the install prompt or browser menu to add WorkWise to your home screen.

## Technical Details

### Architecture
- **Frontend**: Pure HTML5, CSS3, and vanilla JavaScript implementation
- **Structure**: Single-page application with section-based navigation
- **Styling**: CSS custom properties (variables) for consistent theming and easy customization

### Progressive Web App Setup
- **Manifest**: `manifest.json` defines app metadata, icons, and display preferences
- **Service Worker**: Not implemented (can be added for offline functionality)
- **Installation**: Configured for standalone display mode with portrait orientation

### CSS Implementation
- **Variables**: Centralized color scheme using CSS custom properties
- **Responsive**: Mobile-first approach with flexible layouts
- **Animations**: Keyframe animations for smooth transitions and splash screen fade-out
- **Flexbox Layout**: Header uses flexbox for logo, title, and chat icon positioning
- **Image Scaling**: Splash logo uses object-fit for full-screen coverage
- **Components**: Reusable card layouts, navigation styling, and splash screen overlay

### JavaScript Functionality
- **Splash Screen Control**: Timed display and fade-out of splash screen with main content reveal
- **Section Management**: Dynamic showing/hiding of content sections
- **Navigation Highlighting**: Active state management for bottom nav items
- **Header Updates**: Dynamic header title changes based on active section ("WorkWise", "WorkWise Training", "WorkWise Events", "Job Openings", "Submission Instruction")
- **Email Copying**: Clipboard functionality for recruitment email address
- **Smooth Scrolling**: Automatic scroll to top on section changes

## Installation and Deployment

### Local Development
1. Clone or download the project files
2. Open `index.html` directly in a web browser
3. No build process or dependencies required

### Web Server Deployment
1. Upload all files to a web server
2. Ensure `manifest.json` is accessible at the specified path
3. Configure HTTPS for PWA installation capabilities
4. Test PWA installation on target devices

### Requirements
- Modern web browser with PWA support (Chrome, Firefox, Safari, Edge)
- HTTPS connection for full PWA functionality
- No server-side dependencies

## Screenshots and Diagrams

### App Structure Diagram
```
WorkWise PWA
├── Splash Screen
│   └── Company Logo (Logo.jpg)
├── Header
│   ├── Left: Icon (Icon.PNG)
│   ├── Center: Dynamic Title & Subtitle
│   └── Right: Chat Icon Placeholder
├── Home Section
│   ├── Welcome Card
│   └── Services List
├── Classes Section
│   ├── Schedule Table
│   └── Enrollment Modals
├── Events Section
│   ├── Event Cards
│   └── Registration Modals
├── Jobs Section
│   ├── Job Postings
│   └── Apply Buttons
├── Connect Section
│   ├── Application Steps
│   └── Email Contact
└── Bottom Navigation
    ├── Home
    ├── Classes
    ├── Events
    ├── Jobs
    └── Connect
```

### User Flow Diagram
```
User Opens App → Splash Screen (5s)
    ↓
Splash Fades → Home Section
    ↓
Navigation Click → Target Section
    ↓
Interaction (Enroll/Register/Apply) → Modals/Email
    ↓
Form Submission → Confirmation
```

*(Note: Actual screenshots would be added here showing the app interface on different devices)*

## Tally.so Integrations

### Overview
WorkWise integrates with Tally.so for form-based interactions, specifically for training enrollment. Tally.so provides embeddable forms and widgets for collecting user information without requiring custom backend development.

### Implementation Details
- **Widget Script**: Loaded asynchronously via `<script async src="https://tally.so/widgets/embed.js"></script>`
- **Modal Embeds**: Forms open as modals using `#tally-open=FORM_ID&tally-layout=modal` hash links
- **Form IDs**: Training enrollment uses `Zjjxez`, Webinar registration uses `lbbQ5k`
- **Modal Configuration**: Includes alignment, title hiding, emoji animations for enhanced UX

### API Usage
While Tally.so primarily uses embeddable widgets rather than traditional APIs, the integration follows these patterns:

1. **Form Embedding**: Widgets are embedded using JavaScript SDK
2. **Data Collection**: Forms collect enrollment data (name, email, course selection)
3. **Submission Handling**: Tally.so handles form validation and data storage
4. **Response Management**: Success/error states managed by Tally.so interface

### Configuration
- **Form URLs**: Currently using placeholder URLs (`https://tally.so/r/your-link-here`)
- **Customization**: Forms can be customized through Tally.so dashboard
- **Integration**: No API keys required; forms are publicly accessible

### Future Enhancements
- Webhook integrations for enrollment confirmations
- API-based form submissions for better user experience
- Analytics integration for tracking enrollment metrics

## Contributing

This is a static web application. Contributions can include:
- UI/UX improvements
- Additional features
- Bug fixes
- Documentation updates

## License

[Add appropriate license information]

## Contact

For recruitment inquiries: recruitmentph@workwise.com