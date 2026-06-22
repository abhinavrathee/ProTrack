# ProTrack — Full Project Documentation

> **"Plan. Track. Deliver."**
> A web-based Learning Management System (LMS) designed to help students manage academic activities, track progress, set goals, and gain insights through real-time analytics.

---

## Table of Contents

1. [Project Overview](#1-project-overview)
2. [Tech Stack Used](#2-tech-stack-used)
3. [Skills for Resume](#3-skills-for-resume)
4. [Project Structure](#4-project-structure)
5. [Pages and Features Breakdown](#5-pages-and-features-breakdown)
6. [JavaScript Modules Logic](#6-javascript-modules-logic)
7. [CSS Architecture](#7-css-architecture)
8. [Assets and Media](#8-assets-and-media)
9. [Data Storage and State Management](#9-data-storage-and-state-management)
10. [Key Algorithms and Implementations](#10-key-algorithms-and-implementations)
11. [External Libraries and CDNs Used](#11-external-libraries-and-cdns-used)
12. [Academic and Project Context](#12-academic-and-project-context)

---

## 1. Project Overview

**ProTrack** is a front-end-only Learning Management System (LMS) built entirely with vanilla HTML, CSS, and JavaScript. It is designed for students to track their academic journey including:

- College lecture attendance
- Self-study hours
- Extracurricular activities
- Goal setting and event scheduling
- Performance analytics and visual reports
- Task management via a to-do list
- Subscription/billing plan simulation

The app does **not use any backend or server**. All data is stored and persisted using the browser's **`localStorage`** API. This makes ProTrack a fully client-side, zero-dependency static web application.

### Live Demo
Available at: [abhinavrathee.github.io/ProTrack](https://abhinavrathee.github.io/ProTrack/)

### Target Audience
Students at all levels who want to manage, track, and improve their academic performance.

---

## 2. Tech Stack Used

### Frontend (Core)

| Technology | Usage |
|---|---|
| **HTML5** | Structure of all 9 web pages; semantic tags like `<header>`, `<aside>`, `<main>`, `<footer>`, `<section>`, `<nav>` |
| **CSS3** | Styling all pages; each page has its own dedicated CSS file |
| **Vanilla JavaScript (ES6+)** | All interactivity, DOM manipulation, form handling, localStorage logic |

### UI Libraries (via CDN)

| Library | Version | Purpose |
|---|---|---|
| **Font Awesome** | 5.15.4 & 6.1.1 & 6.2.0 & 6.4.0 | Icons across all pages (fa-bars, fa-moon, fa-chart-line, fa-lock, etc.) |
| **Google Material Icons Sharp** | Latest | Dashboard sidebar icons and action buttons |
| **Google Material Symbols Outlined** | Latest | Todo list icon set |
| **Google Fonts — Poppins** | All weights 100-900 | Primary font family used across the entire project |
| **Chart.js** | CDN (jsdelivr) | Line, Bar, and Doughnut charts on the Reports page |
| **jQuery** | 3.6.0 | DOM utility used in landing page and login page |
| **Payment Icons** | 1.1.0 (jsdelivr) | Card icons (Visa, Mastercard, Amex, Discover) on billing page |

### Data and Storage

| Technology | Usage |
|---|---|
| **`localStorage` API** | Persisting user accounts, session state, todos, activities, calendar events |
| **JSON** | Data format for serializing/deserializing objects stored in `localStorage` |
| **Browser Session** | Maintaining signed-in user state via `localStorage.getItem('signedInUser')` |

### Development Tools

| Tool | Usage |
|---|---|
| **VS Code** | Primary code editor |
| **Git / GitHub** | Version control and project hosting |
| **Chrome DevTools** | Debugging and responsive design testing |
| **Live Server** | Local development server |

---

## 3. Skills for Resume

> This section lists all the skills demonstrated through building this project. These are directly extractable from the project code and features.

---

### Programming Languages
- **HTML5** — Semantic markup, forms, tables, SVG, accessibility attributes
- **CSS3** — Custom properties, flexbox, grid, animations, responsive design, dark mode, media queries
- **JavaScript (ES6+)** — DOM manipulation, event listeners, arrow functions, template literals, destructuring, `localStorage`, JSON parsing

### Frontend Development
- **Responsive Web Design** — Mobile-first approach, CSS media queries, viewport management
- **UI/UX Design** — Consistent design system across 9 pages with reusable sidebar and header components
- **Dark/Light Mode Toggle** — Implemented via CSS class toggling (`dark-theme-variables`) with preference persisted in `localStorage`
- **CSS Flexbox and Grid** — Used extensively for layouts across all pages
- **CSS Animations and Transitions** — Hover effects, sidebar open/close transitions, popup modals
- **SVG Circular Progress Indicators** — Custom `<svg>` elements used for the Dashboard insight rings
- **Modern UI Patterns** — Applied in billing and settings page card designs

### Data Visualization
- **Chart.js** — Integrated and configured three distinct chart types:
  - **Line Chart** — Performance Score trend over months
  - **Bar Chart** — Task Completion Rate by category
  - **Doughnut Chart** — Time Distribution across activities
- **Dynamic Chart Theming** — Chart colors and legends update based on dark/light mode
- **Data-driven Rendering** — Charts are rendered from programmatic data arrays

### Authentication and State Management
- **Client-Side Authentication System** — User registration, login, and session management built from scratch using `localStorage`
- **Gender-based Profile Personalization** — Profile photo changes dynamically (male.png / female.png) based on user's registered gender
- **Session Persistence** — Login state maintained across page navigations using `localStorage`
- **Logout and State Cleanup** — Proper session removal on logout with redirect

### Calendar and Event Scheduling
- **Interactive Calendar** — Fully custom-built calendar in JavaScript with month navigation
- **Event CRUD Operations** — Add, display, and delete calendar events per day
- **Date Validation** — Custom date/time input validation with formatting auto-complete
- **LocalStorage Event Persistence** — Events survive page refresh via `localStorage`

### Task Management
- **To-Do List Application** — Create, read, update, delete (CRUD) tasks
- **Category System** — Tasks categorized into: Self-Study, College Lectures, Extra-Curricular, Self-Improvement
- **Deadline Tracking** — Each task includes a deadline date
- **Task Completion Toggle** — Checkbox-based completion marking with visual strikethrough
- **Inline Editing** — Edit task content directly in the list view via contenteditable-style input toggling
- **LocalStorage Persistence** — All tasks are saved and restored across sessions

### Software Architecture and Best Practices
- **Multi-Page Application (MPA)** — 9 HTML pages with a consistent shared sidebar navigation
- **Separation of Concerns** — HTML for structure, CSS for styling, JS for behavior — all kept in separate files
- **Modular JavaScript** — Each page has its own dedicated JS file (`login.js`, `dashboard.js`, `todo.js`, `charts.js`, `goalSetting.js`, `billing.js`, `settings.js`, `script.js`)
- **Reusable Components** — Sidebar navigation and the "Activity Analytics" panel are shared across Dashboard, Analytics, Goal Setting, Todo, and Reports pages
- **DOM Manipulation** — Elements created, appended, and removed programmatically using JavaScript

### Payment Flow Simulation
- **Billing Gateway UI** — A complete payment form with card number, expiry date, CVV, and cardholder name
- **Plan Switching** — Toggle between Monthly (Rs.599) and Annual (Rs.5999) plans with dynamic price updates
- **Order Summary Modal** — A success confirmation modal with order receipt details
- **Card Icon Detection** — Real payment card brand icons (Visa, Mastercard, Amex, Discover)

### Web Performance and SEO
- **Preloader** — A loading GIF shown before page content appears
- **Scroll-to-Top Button** — Smooth navigation UX enhancement
- **Favicon** — Custom favicon applied to all pages
- **Meta Viewport** — Proper responsive viewport configured on every page
- **Semantic HTML** — Use of `<header>`, `<footer>`, `<main>`, `<aside>`, `<section>`, `<nav>` etc.

---

## 4. Project Structure

```
ProTrack/
|
|-- index.html               <- Public landing page (hero, features, testimonials, download CTA)
|-- login.html               <- Login + Register page with animated panel flip
|-- dashboard.html           <- Main admin dashboard (insights, courses, activity analytics)
|-- goalSetting.html         <- Interactive calendar with event scheduling
|-- analytics.html           <- Timeline of learning milestones
|-- todo.html                <- Categorized to-do list with deadlines
|-- reports.html             <- Chart.js-powered visual reports
|-- settings.html            <- Profile, authentication, privacy, subscription settings
|-- billing-getaway.html     <- Payment simulation with plan selection and success modal
|
|-- README.md                <- GitHub project README
|-- PROJECT_DOCUMENTATION.md <- This file: full project documentation
|-- .gitIgnore               <- Git ignore configuration
|-- Landing-Page-React.zip   <- Archived React version of the landing page
|
|-- contents/
    |-- css/
    |   |-- style.css           <- Landing page styles
    |   |-- queries.css         <- Responsive breakpoints for landing page
    |   |-- login.css           <- Login/register animated panel styles
    |   |-- dashboard.css       <- Shared dashboard layout + sidebar styles
    |   |-- goalSetting.css     <- Calendar component styles
    |   |-- analytics.css       <- Timeline section styles
    |   |-- todo.css            <- Todo list styles
    |   |-- reports.css         <- Report card and chart container styles
    |   |-- setting.css         <- Settings page and shared card styles
    |   `-- billing.css         <- Billing gateway form and modal styles
    |
    |-- js/
    |   |-- script.js           <- Landing page: hamburger menu, scroll-to-top logic
    |   |-- login.js            <- Auth system: sign-up, sign-in, gender-based profile
    |   |-- dashboard.js        <- Core dashboard: sidebar toggle, dark mode, activity CRUD, session check
    |   |-- goalSetting.js      <- Full calendar implementation with event management
    |   |-- todo.js             <- Todo CRUD with categories, deadlines, and localStorage
    |   |-- charts.js           <- Chart.js configuration for Line, Bar, and Doughnut charts
    |   |-- settings.js         <- Settings page interactivity (Pro popup, subscription)
    |   `-- billing.js          <- Payment form handling, plan switching, success modal
    |
    `-- images/
        |-- logo.png            <- ProTrack logo
        |-- favicon.png         <- Browser tab icon
        |-- hero-image.svg      <- Landing page hero illustration
        |-- login_img.svg       <- Login panel illustration
        |-- register_img.svg    <- Register panel illustration
        |-- header-shape.svg    <- Decorative header shape
        |-- banner.png          <- README banner image
        |-- dashboard.png       <- Dashboard screenshot
        |-- analytics.png/.jpg  <- Analytics screenshots
        |-- goals.png           <- Goals screenshot
        |-- tracking.jpg        <- Activity tracking section image
        |-- calender.jpg        <- Calendar section image
        |-- download-app.png    <- App download section image
        |-- preloader.gif       <- Loading animation
        |-- student-1.jpg       <- Testimonial photo - Emily Johnson
        |-- student-2.jpg       <- Testimonial photo - Daniel Martinez
        |-- testimonial-bg.jpg  <- Testimonial section background
        |-- male.png            <- Male avatar (profile photo)
        |-- female.png          <- Female avatar (profile photo)
        |-- user.png            <- Default/fallback user avatar
        |-- google-play.png     <- Google Play Store badge
        |-- app-store.png       <- Apple App Store badge
        `-- IndianFlag.jpg      <- Indian flag for country selector in footer
```

---

## 5. Pages and Features Breakdown

### 5.1 Landing Page (index.html)

**Purpose:** Public-facing marketing page that introduces ProTrack to new visitors.

**Sections:**

| Section | Description |
|---|---|
| **Navigation** | Logo + site name + hamburger menu (mobile) + Register/Logout button |
| **Hero** | Headline "Empower Your Academic Journey", description, Login + Explore More buttons, hero SVG illustration |
| **Features** | 3-column grid: Comprehensive Tracking, Interactive Analytics, Customizable Experience |
| **Testimonials** | 2 student reviews with photos (Emily Johnson, Daniel Martinez) |
| **Courses/Modules** | Activity Tracking, Interactive Calendar, Activity Analytics — each with image and description |
| **Download App** | App promo with mobile features (Set Reminders, Access Anywhere, Real-Time Analytics) + Store badges |
| **Footer** | Multi-column links (About, Features, Student Portal, Learn More, Follow Us), country + language selectors, social media icons, copyright disclaimer |

**Key UX Features:**
- Preloader GIF shown while the page loads
- Scroll-to-top button appears on scroll
- Dark mode toggle (moon icon) — preference saved in `localStorage`
- Dynamic Nav: If a user is already signed in, "Register" button changes to "Welcome, Username!" + Logout, and hero buttons change to "Open Dashboard"
- Hamburger menu for mobile navigation

---

### 5.2 Login / Register Page (login.html)

**Purpose:** Combined login and registration page with animated panel transitions.

**Layout:**
- Split-screen with two panels: Left (sign-in form) and Right (sign-up panel art)
- Clicking "Sign Up" slides the panels to reveal the registration form

**Sign-Up Form Fields:** Username, Email, Password, Gender (radio: Male / Female), Social login buttons (UI only)

**Sign-In Form Fields:** Username, Password, Social login buttons (UI only)

**Authentication Logic (login.js):**
1. **Registration:** Validates unique username, stores `{ username, password, gender }` as JSON array in `localStorage['users']`
2. **Login:** Looks up stored users array, matches username+password, sets `localStorage['signedInUser']` and `localStorage['userGender']` on success
3. **Redirect:** On successful login → redirects to `index.html`
4. **Profile Photo:** Gender stored at login is later used in the dashboard to show male.png or female.png
5. **Session Check:** If already signed in, auto-configures dashboard navigation

---

### 5.3 Dashboard (dashboard.html)

**Purpose:** Main hub of the application after login. Provides an overview of academic performance.

**Layout:** 3-column layout — Left Sidebar | Main Content | Right Panel

**Left Sidebar Navigation Links:** Dashboard (active), Goal Setting, Analytics, Todo, Reports, Settings, Logout

**Main Content:**
- Date Picker — Inline HTML date input for filtering
- Insights Cards (3 circular SVG progress rings):
  - College Lectures: 81% (18 Lectures)
  - Self Study: 62% (10 Skills)
  - Extra-curricular: 44% (8 Activities)
- My Courses Table with columns: Course Name, Start Date, Rate, Level, Status
  - Sample data: Web Design (Jul 30, 4.9, Intermediate, Pending), OOPS (Aug 15, 4.8, Intermediate, Pending), DBMS (Sep 3, 4.4, Elementary, Pending)
- Add Activity Popup Form — modal with Title and Duration fields

**Right Panel:**
- Profile section with username and dynamic gender-based avatar
- Dark/Light mode toggle button
- Recent Updates — Activity feed showing latest user actions
- Activity Analytics — List of logged activities loaded from `localStorage`
- "+ Add Activity" button — Opens popup to add new activities

**Dashboard JS Logic (dashboard.js):**
- Checks `localStorage['signedInUser']` on load — if not found, redirects to `login.html` (route protection)
- Sets dynamic username in all `#username-placeholder` elements
- Sets gender-based profile photo in all `#profile-photo-placeholder` elements
- Handles sidebar open/close on mobile via menu button
- Dark mode toggle stores preference in CSS class `dark-theme-variables`
- Activity CRUD: loads activities from `localStorage['activities']`, renders them dynamically
- `logout()` function clears `signedInUser` from `localStorage` and redirects to `login.html`

---

### 5.4 Goal Setting (goalSetting.html)

**Purpose:** An interactive calendar for scheduling and managing academic events and deadlines.

**Features:**
- Full Monthly Calendar View with day cells
- Navigation: Previous month and Next month arrows
- Today Button — Jumps back to the current month
- Go-To Date — Input field (mm/yyyy format) + Go button to jump to a specific month
- Day Selection — Click any day to view and manage events for that day
- Event Display Panel — Shows selected day name, full date, and list of events scheduled
- Add Event Modal — Triggered by the floating + button (Event Name, Time From, Time To)
- Event Deletion — Click an event in the panel to get a delete confirmation dialog
- Days with Events — Visually marked with an event dot indicator

**Calendar JS Logic (goalSetting.js):**
- Fully custom-built calendar without any third-party calendar library
- Uses native `Date()` object to calculate first day, last day, and surrounding month days
- Events stored as a structured array in `localStorage['events']`:
  ```
  [{ "day": 15, "month": 6, "year": 2026, "events": [{ "title": "Math Exam", "time": "10:00 AM - 12:00 PM" }] }]
  ```
- Time is validated against 24-hour format and converted to 12-hour AM/PM display
- Duplicate event detection (same title on same day is rejected)

---

### 5.5 Analytics (analytics.html)

**Purpose:** A chronological timeline showcasing academic/learning milestones.

**Content — Timeline of Learning Achievements:**

| Month | Achievement |
|---|---|
| September 2023 | Advanced Excel and Data Analysis (Jobaaj Learning Platform) |
| October 2023 | Python Programming Excellence — 5-star HackerRank, 850+ points, top 10% |
| November 2023 | C++ and Object-Oriented Programming — Student Management System |
| December 2023 | Data Structures Fundamentals — Hospital Management System |
| January 2024 | Advanced Python — FastAPI, SQLAlchemy, REST API |
| February 2024 | Frontend Development — HTML5, CSS3, JS ES6+, Tailwind, animations |
| March 2024 | Database Design and SQL — Inventory Management System, MySQL |
| April 2024 | React and Modern Web Dev — Redux, Firebase, Task Management System |
| May 2024 | Backend Development with Node.js — Express.js, MongoDB, Social Media Backend |
| July 2024 | Full Stack Deployment — AWS, GitHub Actions CI/CD, nginx, SSL |
| August 2024 | Cloud Architecture and DevOps — AWS EC2/S3/Lambda, Docker, Kubernetes |
| September 2024 | Machine Learning and AI — TensorFlow, scikit-learn, recommendation systems |

---

### 5.6 Todo List (todo.html)

**Purpose:** A task management system for tracking academic goals with categories and deadlines.

**Create Task Section:**
- Goal text input
- Category selector (radio buttons): Self-Study (blue), College Lectures (purple), Extra-Curricular (orange), Self-Improvement (green)
- Deadline date picker
- "Add Goal" submit button

**Todo List Section:**
Each todo item displays: Colored category bubble, Goal text (editable), Deadline date, Checkbox to mark complete, Edit button, Delete button.
Completed tasks get a visual `done` class (strikethrough/dimmed style).

**Todo JS Logic (todo.js):**
- On load: reads `localStorage['todos']` array and renders all todos
- On submit: creates new todo object `{ content, category, deadline, done: false, createdAt }` and pushes to array
- Checkbox: toggles `todo.done`, updates `localStorage`, re-renders
- Edit: removes `readonly` from input on Edit click, saves on blur
- Delete: filters out the todo object and saves updated array

---

### 5.7 Reports (reports.html)

**Purpose:** Visual reports showing academic performance using Chart.js data visualizations.

**Charts:**

| Chart | Type | Data |
|---|---|---|
| **Performance Score** | Line Chart | Current vs Previous period scores (Jan-Jun): 88 vs 79 max |
| **Task Completion Rate** | Bar Chart | Projects (85%), Meetings (90%), Tasks (78%), Goals (92%) vs targets |
| **Time Distribution** | Doughnut Chart | Development (40%), Meetings (20%), Planning (25%), Learning (15%) |

**Stats Cards:**

| Card | Value | Change |
|---|---|---|
| Focus Time | 5.2h | +15% increase |
| Goals Progress | 78% | -3% decrease |

**Charts JS Logic (charts.js):**
- Waits for DOM to load then initializes each chart only if its canvas element exists
- All charts are responsive: true and maintainAspectRatio: false
- Chart theme color: Purple `#8a70D6` as primary accent
- `updateChartsTheme()` function updates chart legend/axis colors for dark/light mode
- Window resize handler triggers chart `.resize()` on all charts

---

### 5.8 Settings (settings.html)

**Purpose:** Account and preference management page.

**Sections:**

**1. Upgrade to Pro Banner**
- Prominent card at top urging upgrade
- "Learn More" button opens the Pro Plan popup modal

**2. Profile Settings**
- Fields: Username, First Name, Last Name, Email, Phone
- Save / Cancel buttons

**3. Authentication Settings**
- Change Password (Current, New, Confirm New)
- Two-Factor Authentication (Enable 2FA button — UI only)
- Login History (View Login History button — UI only)

**4. Pro Settings — Plan Comparison**
- Free Plan: Basic activity tracking, limited goal setting, basic analytics
- Pro Plan: Advanced tracking, unlimited goals, comprehensive analytics + reports, ad-free, priority support
- "Subscribe Now" links to `billing-getaway.html`

**5. Privacy Settings**
- Checkbox: Allow usage data collection
- Checkbox: Allow personalized recommendations
- View Privacy Policy button
- Data Export: "Request Data Export" (processing takes 48 hours)
- Data Deletion: Danger zone with warning, confirmation checkbox, and "Delete My Account" button (disabled until checkbox checked)

---

### 5.9 Billing Gateway (billing-getaway.html)

**Purpose:** A simulated payment flow for upgrading to ProTrack Pro.

**Plan Selection:**
- Monthly Plan: Rs.599/month
- Annual Plan: Rs.5,999/year (saves 17%)
- Clicking a plan updates the order summary dynamically

**Order Details Table:** Plan Name, Order ID, Total Before Tax, Tax (10%), Order Total

**Payment Form:**
- Card Number (with Visa, Mastercard, Amex, Discover icons)
- Expiry Date (MM/YY format)
- CVV
- Name on Card
- "Pay Rs.599.00" submit button
- SSL Security Badge: "Secure SSL Encrypted Payment"

**Success Modal:** Shown after payment submission. Displays: Order ID, Plan, Amount, Tax, Total Paid. "Back to Homepage" button.

**Billing JS Logic (billing.js):**
- Plan toggle updates displayed price and order summary values
- Form submission triggers the success modal with calculated totals
- Card number auto-formatted with spaces every 4 digits
- Expiry date auto-formatted as MM/YY

---

## 6. JavaScript Modules Logic

| File | Responsibility |
|---|---|
| `script.js` | Landing page: hamburger menu toggle, scroll-to-top button show/hide |
| `login.js` | User registration (unique username check), sign-in (credential match), session management, gender-based profile photo setup |
| `dashboard.js` | Route protection (redirect to login if not signed in), dynamic username/avatar rendering, sidebar open/close, dark mode toggle, activity CRUD (localStorage), logout |
| `goalSetting.js` | Full custom calendar: date calculation, month navigation, event add/delete/display, localStorage persistence, 12/24 hour time conversion, event validation |
| `todo.js` | Todo CRUD: add with category/deadline, checkbox completion, inline edit on blur, delete, localStorage persistence |
| `charts.js` | Chart.js initialization for 3 chart types, theme-aware color updating, resize handler, hover cursor |
| `settings.js` | Pro upgrade popup modal control, delete account button enable/disable based on confirmation checkbox |
| `billing.js` | Plan switching (monthly/annual), order summary calculation, card number formatting, success modal trigger |

---

## 7. CSS Architecture

Each page has a **dedicated CSS file** to prevent style conflicts:

| CSS File | Covers |
|---|---|
| `style.css` | Full landing page: navbar, hero, features, testimonials, courses, download section, footer, dark mode, scroll button |
| `queries.css` | Responsive breakpoints for the landing page (tablet and mobile layouts) |
| `login.css` | Animated panel flip transition, input field styling, social media icons |
| `dashboard.css` | Shared base for all inner pages: sidebar, top-right panel, insights cards with SVG rings, course table, activity analytics widget, dark theme variables |
| `goalSetting.css` | Calendar grid, day cells, event display panel, add event form popup |
| `analytics.css` | Vertical timeline component with dots, connectors, and content cards |
| `todo.css` | Todo item cards, category color bubbles, completion strikethrough, edit/delete button styles |
| `reports.css` | Chart card containers, stats grid, stat cards with icons and change indicators |
| `setting.css` | Settings card layout, Pro banner, plan comparison cards, privacy toggle styles |
| `billing.css` | Billing form layout, plan option cards, success modal overlay |

### Design System Highlights
- **Primary Color:** Purple (`#8a70D6` and variations)
- **Font:** Poppins (all weights 100-900)
- **Dark Mode:** Toggled via `dark-theme-variables` CSS class on `<body>`, with CSS custom properties
- **CSS Custom Properties (Variables):** Used for consistent color, spacing, and border-radius values
- **Card-based UI:** Settings, reports, and billing use a consistent `.card` component

---

## 8. Assets and Media

| File | Usage |
|---|---|
| `logo.png` | Landing page nav logo |
| `favicon.png` | Browser tab icon (all pages) |
| `hero-image.svg` | Landing page hero illustration (~1.6MB) |
| `login_img.svg` | Login panel illustration |
| `register_img.svg` | Register panel illustration |
| `header-shape.svg` | Decorative SVG shape behind hero section |
| `banner.png` | README.md banner (~590KB) |
| `dashboard.png` | Dashboard screenshot for README |
| `analytics.png / analytics.jpg` | Analytics screenshots |
| `goals.png` | Goal Setting screenshot for README |
| `tracking.jpg` | Activity Tracking section image |
| `calender.jpg` | Calendar section image |
| `download-app.png` | App download section image |
| `preloader.gif` | Page loading animation (~516KB) |
| `student-1.jpg` | Testimonial photo — Emily Johnson |
| `student-2.jpg` | Testimonial photo — Daniel Martinez |
| `testimonial-bg.jpg` | Background for testimonial section |
| `male.png` | Male user avatar (shown when gender = male) |
| `female.png` | Female user avatar (shown when gender = female) |
| `user.png` | Default avatar (fallback) |
| `google-play.png` | Google Play Store badge |
| `app-store.png` | Apple App Store badge |
| `IndianFlag.jpg` | Flag shown in footer country selector |
| `log-ProTrack.png` | High-res ProTrack logo (~1.8MB) |

---

## 9. Data Storage and State Management

ProTrack uses **browser localStorage** as its sole data store. No backend, no database.

### localStorage Keys Used

| Key | Type | Set By | Used By | Description |
|---|---|---|---|---|
| `users` | JSON Array | `login.js` sign-up | `login.js` sign-in | Array of `{ username, password, gender }` objects |
| `signedInUser` | String | `login.js` sign-in | All dashboard pages | The username of the currently logged-in user |
| `userGender` | String | `login.js` sign-in | `dashboard.js` | 'male' or 'female' for profile photo |
| `dark-mode` | String | `index.html` script | `index.html` | 'enabled' or 'disabled' for landing page dark mode |
| `activities` | JSON Array | `dashboard.js` | `dashboard.js` | Array of `{ title, duration, createdAt }` activity objects |
| `todos` | JSON Array | `todo.js` | `todo.js` | Array of `{ content, category, deadline, done, createdAt }` |
| `events` | JSON Array | `goalSetting.js` | `goalSetting.js` | Array of `{ day, month, year, events: [{title, time}] }` |

### Data Flow Example (Login to Dashboard)

```
User fills login form
  |
  v
handleSignIn() called in login.js
  |
  v
Looks up localStorage['users'] array
  |
  v
Finds matching { username, password }
  |
  v
Sets localStorage['signedInUser'] = username
     localStorage['userGender'] = gender
  |
  v
Redirects to index.html -> user clicks "Open Dashboard"
  |
  v
dashboard.html loads -> dashboard.js runs DOMContentLoaded listener
  |
  v
Reads localStorage['signedInUser'] -- if null -> redirect to login.html
  |
  v
Sets all #username-placeholder elements to the username
Sets all #profile-photo-placeholder src to male.png or female.png
```

---

## 10. Key Algorithms and Implementations

### 10.1 Custom Calendar Algorithm
The calendar in `goalSetting.js` dynamically generates each month's day grid:
1. Get the first day of the month — determines offset for empty cells before day 1
2. Get the last day of the month — determines total days to render
3. Fill remaining cells at end with next month's days
4. Mark today's date with `today active` CSS classes
5. Mark days with saved events with an `event` CSS class
6. On day click: switch months if prev/next date cell was clicked, update active state

### 10.2 Authentication System
Uses a simple array-based credential store in localStorage:
- Register: Check for username collision, push new user, save
- Login: `Array.find()` to match both username AND password, set session

### 10.3 Activity Rendering (Dashboard)
Activities from localStorage are rendered dynamically:
- Odd/even `createdAt` timestamp determines "online" (green) vs "offline" (blue) activity type
- Icons, time labels, and completion percentages are set based on this classification

### 10.4 Todo Edit (Inline Editing)
The edit button removes the `readonly` attribute from the input, gives it focus. On `blur` (when user clicks away), it re-applies `readonly` and saves the updated content to localStorage.

### 10.5 Billing Plan Toggle
Clicking Monthly/Annual plan cards:
1. Toggles `active` CSS class
2. Updates order summary table values (`#plan-name`, `#total-before-tax`, `#tax-amount`, `#order-total`)
3. Updates the Pay button text dynamically

---

## 11. External Libraries and CDNs Used

```
Font Awesome (Icons):
  https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css
  https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css
  https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.2.0/css/all.min.css
  https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css

Google Fonts — Poppins:
  https://fonts.googleapis.com/css2?family=Poppins:wght@...

Google Material Icons Sharp:
  https://fonts.googleapis.com/icon?family=Material+Icons+Sharp

Google Material Symbols Outlined:
  https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined...

jQuery:
  https://code.jquery.com/jquery-3.6.0.min.js

Chart.js:
  https://cdn.jsdelivr.net/npm/chart.js

Payment Icons (Visa, Mastercard, etc.):
  https://cdn.jsdelivr.net/npm/payment-icons@1.1.0/min/flat/visa.svg
  https://cdn.jsdelivr.net/npm/payment-icons@1.1.0/min/flat/mastercard.svg
  https://cdn.jsdelivr.net/npm/payment-icons@1.1.0/min/flat/amex.svg
  https://cdn.jsdelivr.net/npm/payment-icons@1.1.0/min/flat/discover.svg
```

---

## 12. Academic and Project Context

| Detail | Info |
|---|---|
| **Project Type** | Academic / Educational Web Development Project |
| **Institution** | Chitkara University Institute of Engineering and Technology, Punjab, India |
| **Supervised By** | Ms. Parul Gahelot |
| **Year** | 2024 |
| **License** | Personal and Educational Use — Free. Commercial use requires author permission. |
| **GitHub** | github.com/abhinavrathee/ProTrack |
| **Live URL** | abhinavrathee.github.io/ProTrack/ |

---

> This documentation was generated from a full code analysis of the ProTrack project.
> Every section is based on what actually exists in the codebase — no fabricated features.
>
> (c) 2024 ProTrack. All rights reserved.
