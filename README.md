<p align="center">
  <img src="./img.png" alt="Project Banner" width="100%">
</p>

# VitalLink 🎯

## Basic Details

### Team Name: Duo Nova

### Team Members
- Member 1: Aleena Leen - College of engineering Trivandrum
- Member 2: Arundhathi C - College of engineering Trivandrum 

### Hosted Project Link
[mention your project hosted link here]

### Project Description
VitalLink is a web based blood donor management sysytem that enables college students to register as donors with their blood type health informations, while the admin can access secure dashboard to search filter and manage donor records by blood type and eligibility status for coordinations during blood requirements.

### The Problem statement
college campus lack a centralized system to identify and mobilize eligible blood donors during medical requirements resulting in inadequte blood supply coordination.

### The Solution
VitalLink - a campus blood donor network.
VitalLink provides a centralized digital platform where students register as blood donors by providing their student and medical details with colllege id as identification.The system automatically assesses eligibility based on medical criteria and stores all data securely.When there is a blood requirement, administrators can instantly sort and filter donors by blood type and eligibility status, then send donation requests directly to eligible students via their registered mobile numbers. Students can respond to requests by accepting or declining with a reason provided, creating a transparent and efficient coordination system can enable efficient responses and ensures student consent before mobilization.

## Technical Details

### Technologies/Components Used

**For Software:**
- Languages used: HTML, CSS, Javascript
- Frameworks used: Firebase 
- Libraries used: Firebase SDK
- Tools used: VS Code, Git/Github



## Features

List the key features of your project:
- Feature 1: Student registration with real-time validation, automatic eligibility assessment (age 18-65, weight 50kg+, medical conditions) and duplicate detection (Student ID, email, phone).
- Feature 2: Admin dashboard with comprehensive donor  blood type and eligibility status plus real-time statistics (total donors, eligible count, ineligible count, stale records >30 days).
- Feature 3: Donation request system allowing admins to send blood requests to eligible donors via WhatsApp with pre-formatted messages including hospital details, donation date, reporting time, and address, with students able to accept or decline with reasons.
- Feature 4: Firebase Authentication for secure admin login and session-based admin tracking with real-time response updates.


## Implementation

### For Software:

#### Installation
Clone the repository, configure Firebase credentials in HTML files, create admin accounts in Firebase Authentication, enable Firestore with donor and donationRequests collections, and deploy to any static hosting (Firebase Hosting, GitHub Pages, or web server).


#### Run


### For Software:

#### Screenshots (Add at least 3)
<img width="1893" height="877" alt="image" src="https://github.com/user-attachments/assets/179df57e-5c70-459f-bd6a-a7c2f7f5ff42" />
Homepage shows hero section with "Every Drop Saves a Life" headline, key features overview, blood type badges, and CTAs for student registration and admin login.

<img width="1880" height="857" alt="image" src="https://github.com/user-attachments/assets/d5b4d702-0ef4-40a4-b592-9ef9189d19de" />
Registration page displays form fields for personal info and medical info with real-time validation feedback.
<img width="1892" height="852" alt="image" src="https://github.com/user-attachments/assets/3a3de80e-b286-4aa8-859c-3c36c5e87749" />
Admin dashboard shows donor statistics (total/eligible/ineligible/stale), search/filter toolbar, donor records table with blood type badges, eligibility status chips, request buttons, and donation requests tab with pending/accepted/declined statuses.
#### Diagrams

**System Architecture:**

┌─────────────────────────────────────────────────────────────┐
│                     VITALLINK SYSTEM                         │
└─────────────────────────────────────────────────────────────┘

┌──────────────────────┐          ┌──────────────────────┐
│   STUDENT USERS      │          │   ADMIN USERS        │
│ - Registration       │          │ - Dashboard Access   │
│ - Response Page      │          │ - Donor Management   │
└──────────────────────┘          └──────────────────────┘
         │                                  │
         │                                  │
    ┌────▼─────────────────────────────────▼────┐
    │      GITHUB PAGES (Static Hosting)        │
    │  (HTML/CSS/JavaScript - No Backend)       │
    └────┬─────────────────────────────────────┬┘
         │                                      │
         └──────────────────┬───────────────────┘
                            │
         ┌──────────────────▼──────────────────┐
         │      FIREBASE (Backend-as-Service) │
         ├──────────────────────────────────────┤
         │  • Authentication (Email/Password)   │
         │  • Firestore Database               │
         │    - donors collection              │
         │    - donationRequests collection    │
         └──────────────────────────────────────┘


Architecture Explanation:

Frontend: Pure HTML/CSS/JavaScript hosted on GitHub Pages (no backend server)
Authentication: Firebase handles admin login/logout with email-password method
Database: Firestore stores all donor records and donation requests with real-time updates
Communication: WhatsApp integration via direct wa.me links (no API calls needed)
Data Flow: Student registers → Data saved to Firestore → Admin views dashboard → Admin sends WhatsApp request → Student responds via link → Status updates in Firestore

**Application Workflow:**

STUDENT FLOW:
Register → Validation → Eligibility Check → Save to Firestore → Success Screen

ADMIN FLOW:
Login (Firebase Auth) → View Dashboard → Search/Filter Donors → Select Eligible Donor
→ Fill Request Form (Date, Hospital, Address) → Send Request
→ WhatsApp Link Generated → Student Receives Message

STUDENT RESPONSE FLOW:
Click WhatsApp Link → Open donor-response.html → View Request Details
→ Accept (Confirm) OR Decline (Select Reason) → Update Firestore
→ Admin Sees Status Change → Process Complete
Workflow Explanation:
Registration Phase: Student fills form with personal & medical data; system validates and assesses eligibility automatically
Admin Phase: Admin logs in securely via Firebase, searches donors by blood type/eligibility, selects candidate
Request Phase: Admin creates donation request with hospital details; system auto-generates WhatsApp message with response link
Response Phase: Student receives WhatsApp message, clicks link, views request details, accepts or declines with reason
Tracking Phase: All responses recorded in Firestore; admin can view status in real-time on dashboard

---


### For Mobile Apps:

#### App Flow Diagram

VitalLink is a web-only application 
Student → Register → Success 
Admin → Login (admin-login.html) → Dashboard → 
Admin → Select donor → Send request → 
Student → Receive WhatsApp link → Click link → 
Student → Respond → Accept/Decline → 
Admin → See status update in dashboard

Installation Guide
VitalLink is web-only 
Access the application:
After deployment to GitHub Pages
Open browser and visit: https://USERNAME.github.io/vitallink

Supported on all devices:
Desktop 
Mobile 
Tablet (responsive design)

## Project Demo

### Video
https://drive.google.com/file/d/1eJy9sa2lGn-0mpG-VzUHxdEaLZZkzJz9/view?usp=drivesdk
https://drive.google.com/file/d/1YOERVI_MVD-maBIU9nPiJQD4tg3S4MhI/view?usp=sharing

Project Demo
Live Website
https://USERNAME.github.io/vitallink
VitalLink is fully functional on GitHub Pages with Firebase backend - Student registration, Admin dashboard, and WhatsApp donation requests work seamlessly.
Key Features Demonstrated:

 Student registration with real-time validation
 Admin login with Firebase Authentication
 Donor search & filter by blood type and eligibility
 Donation request system with WhatsApp integration
 Student accept/decline responses with reasons
 Real-time status updates in admin dashboard

Demo Account Credentials:
Email: admin@vitallink.com
Password: [Contact project maintainer]



## AI Tools Used (Optional - For Transparency Bonus)

If you used AI tools during development, document them here for transparency:

**Tool Used:** e.g. Gemini, ChatGPT, Claude

**Purpose:** [What you used it for]
- Development assistance
- "Debugging assistance for async functions"
- "Code review and optimization suggestions"

**Key Prompts Used:**
-Implement WhatsApp message generation for donation requests with formatted hospital details
-Debugging and optimization of form validation

**Percentage of AI-generated code:** 90%

**Human Contributions:**
- Architecture design and planning
- Custom business logic implementation
- Integration and testing
- UI/UX design decisions
- 
Transparency Note: AI was used extensively for development but all logic, architecture, and testing were human-directed and verified.

## Team Contributions

- Arundhathi C and Aleena leen: Idea Generation,Firebase Configuration,Frontend development,API integration


Made with ❤️ at TinkerHub
