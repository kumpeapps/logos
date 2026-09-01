# Kumpe Home Logs --- Website Brand & UI Template

## 1. Brand Overview

**Product:** Kumpe Home Logs\
**Category:** Home management, documentation, care, maintenance, and
household recordkeeping\
**Primary audience:** Traditional households, foster families,
caregivers, and anyone responsible for maintaining organized home
records.

### Brand promise

> **Maintain. Track. Care. Protect.**

Kumpe Home Logs should feel like a **trusted digital home record**:
organized, protective, modern, calm, and dependable.

The interface should communicate:

-   Trust and safety
-   Organization without bureaucracy
-   Modern technology without looking clinical
-   Family/home warmth without becoming childish
-   Clear recordkeeping and accountability
-   Easy access to important information

The existing shield logo and distinctive **double-K monogram are the
primary brand identifiers. Do not redraw, simplify, mirror, distort, or
replace the double-K.**

------------------------------------------------------------------------

# 2. Visual Direction

## Overall aesthetic

**Modern technology + trusted household record + protective shield**

Think:

-   Dark premium dashboard
-   Cyan/teal technology accents
-   Crisp white typography
-   Subtle glass/metal surfaces
-   Shield and home motifs
-   Strong information hierarchy
-   Rounded but not overly playful components

Avoid:

-   Generic SaaS purple gradients
-   Excessive glassmorphism
-   Cartoon/family-app styling
-   Baby/pastel colors
-   Medical-only visual language
-   Excessive shadows
-   Overly decorative interfaces
-   Excessive animations

The product should look appropriate for both a **professional
foster-care environment** and a **normal family home**.

------------------------------------------------------------------------

# 3. Color System

The logo establishes a black + electric cyan/teal identity.

## Core colors

``` css
:root {
  /* Brand */
  --kh-primary: #10D9E8;
  --kh-primary-bright: #20F3FF;
  --kh-primary-dark: #0798A8;

  /* Background */
  --kh-black: #050708;
  --kh-bg: #080D10;
  --kh-surface: #0D1519;
  --kh-surface-2: #111D22;
  --kh-surface-3: #16262C;

  /* Text */
  --kh-text: #F4FAFB;
  --kh-text-secondary: #B7C8CC;
  --kh-text-muted: #71858A;

  /* Borders */
  --kh-border: #20343A;
  --kh-border-bright: #2C5961;

  /* Status */
  --kh-success: #32D583;
  --kh-warning: #F5B83D;
  --kh-danger: #F05D67;
  --kh-info: #55B8FF;

  /* Light-mode surfaces */
  --kh-light-bg: #F5F9FA;
  --kh-light-surface: #FFFFFF;
  --kh-light-surface-2: #EAF1F3;
  --kh-light-text: #0B171A;
  --kh-light-text-secondary: #50656A;
}
```

## Color usage

### Electric cyan / teal

Use for:

-   Primary buttons
-   Active navigation
-   Important links
-   Selected states
-   Icons
-   Progress indicators
-   Charts
-   Focus rings
-   Brand accents

Do not use cyan for large blocks of body text.

### Black

Use as the primary brand background and for high-contrast dashboard
environments.

### White

Use for:

-   Primary headings
-   Important values
-   Navigation labels
-   Card titles
-   High-priority information

### Status colors

Use status colors consistently:

-   **Green:** completed, healthy, current, verified
-   **Amber:** due soon, attention required
-   **Red:** overdue, critical, incident
-   **Blue:** informational

Status should never be communicated by color alone. Pair with an icon or
text label.

------------------------------------------------------------------------

# 4. Typography

Use a clean geometric sans-serif.

Preferred stack:

``` css
font-family:
  Inter,
  ui-sans-serif,
  system-ui,
  -apple-system,
  BlinkMacSystemFont,
  "Segoe UI",
  sans-serif;
```

## Type scale

``` css
--font-xs: 0.75rem;
--font-sm: 0.875rem;
--font-md: 1rem;
--font-lg: 1.125rem;
--font-xl: 1.375rem;
--font-2xl: 1.75rem;
--font-3xl: 2.25rem;
--font-4xl: 3rem;
```

### Weight

-   400 --- body
-   500 --- labels
-   600 --- navigation and card titles
-   700 --- headings
-   800 --- hero/brand emphasis

Use uppercase sparingly for labels and product branding.

------------------------------------------------------------------------

# 5. Logo Rules

The shield logo is the primary identity.

## Logo placement

Preferred:

-   Top-left of application navigation
-   Centered on login/authentication screens
-   Hero area of marketing pages
-   Footer at reduced size

## Clear space

Maintain at least the height of the inner double-K vertical stroke
around the logo.

## Never

-   Change the double-K geometry
-   Stretch the logo
-   Rotate the logo
-   Add unrelated effects
-   Place it on a visually noisy background
-   Change the brand cyan without a deliberate monochrome variant
-   Separate the double-K from the shield unless creating an approved
    favicon/app icon

------------------------------------------------------------------------

# 6. Design Tokens

``` css
:root {
  --radius-sm: 6px;
  --radius-md: 10px;
  --radius-lg: 16px;
  --radius-xl: 22px;
  --radius-pill: 999px;

  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-5: 20px;
  --space-6: 24px;
  --space-8: 32px;
  --space-10: 40px;
  --space-12: 48px;
  --space-16: 64px;

  --shadow-sm: 0 2px 8px rgba(0,0,0,.18);
  --shadow-md: 0 8px 24px rgba(0,0,0,.25);
  --shadow-lg: 0 16px 48px rgba(0,0,0,.35);

  --transition-fast: 120ms ease;
  --transition-normal: 200ms ease;
}
```

------------------------------------------------------------------------

# 7. Application Layout

Desktop application structure:

``` text
┌─────────────────────────────────────────────────────────────┐
│ Logo / Home Logs          Search       Alerts     Profile   │
├───────────────┬─────────────────────────────────────────────┤
│               │                                             │
│ Dashboard     │  Page title                                │
│ Home          │  Context / household selector              │
│ Maintenance   │                                             │
│ Medications   │  ┌────────┐ ┌────────┐ ┌────────┐           │
│ Health        │  │ Card   │ │ Card   │ │ Card   │           │
│ Discipline    │  └────────┘ └────────┘ └────────┘           │
│ Documents     │                                             │
│ Contacts      │  Main content                               │
│ Reports       │                                             │
│ Settings      │                                             │
│               │                                             │
└───────────────┴─────────────────────────────────────────────┘
```

### Sidebar

Dark, compact, and persistent on desktop.

Active item:

-   Cyan icon
-   Cyan left indicator
-   Slightly elevated surface
-   High-contrast text

Inactive items:

-   Muted white/gray
-   Cyan hover accent

On mobile, replace the sidebar with a bottom navigation or slide-out
drawer.

------------------------------------------------------------------------

# 8. Dashboard

The dashboard is the heart of the product.

### Hero section

Display:

**Good morning, \[Name\]**

Then:

> Here's what needs your attention today.

Include:

-   Household selector
-   Current date
-   Quick-add button

### Priority cards

Examples:

``` text
MEDICATIONS
2 doses due today

MAINTENANCE
1 item overdue

HEALTH
3 records updated this month

DOCUMENTS
2 items expiring soon
```

Use strong numbers and subtle iconography.

------------------------------------------------------------------------

# 9. Core Product Areas

## Home / Household

Represent each household as a protected environment.

Show:

-   Household name
-   Address (when appropriate)
-   Members
-   Important contacts
-   Current alerts
-   Recent activity

## Maintenance

Track:

-   HVAC
-   Filters
-   Plumbing
-   Electrical
-   Appliances
-   Roof
-   Pest control
-   Smoke/CO detectors
-   Vehicles
-   Yard
-   Other recurring tasks

Each maintenance record should support:

-   Task
-   Location
-   Date completed
-   Next due date
-   Cost
-   Vendor
-   Notes
-   Photos
-   Documents
-   Recurrence

## Medications

Designed around clarity and safety.

Display:

-   Medication name
-   Person
-   Dosage
-   Schedule
-   Next dose
-   Prescriber
-   Pharmacy
-   Refill status
-   Administration history

Use clear warning states and confirmation flows.

## Health

Track:

-   Appointments
-   Immunizations
-   Measurements
-   Allergies
-   Important notes
-   Providers
-   Health documents

The UI should feel organized and private rather than like a hospital
portal.

## Discipline / Behavior

Use neutral, respectful terminology and presentation.

Support:

-   Date/time
-   Person
-   Event type
-   Description
-   Action taken
-   Follow-up
-   Attachments
-   Notes

Avoid punitive visual language.

## Documents

Create a secure document library.

Categories:

-   Medical
-   School
-   Foster care
-   Insurance
-   Household
-   Legal
-   Maintenance
-   Other

Provide:

-   Search
-   Tags
-   Expiration reminders
-   Upload
-   Preview
-   Download
-   Audit/history

------------------------------------------------------------------------

# 10. Cards

Default card:

``` css
.card {
  background: var(--kh-surface);
  border: 1px solid var(--kh-border);
  border-radius: var(--radius-lg);
  padding: var(--space-6);
  box-shadow: var(--shadow-sm);
}
```

Hoverable cards:

``` css
.card-interactive:hover {
  border-color: var(--kh-border-bright);
  transform: translateY(-1px);
  box-shadow: var(--shadow-md);
}
```

Do not make every card glow.

Use cyan glow only for important interactive/selected elements.

------------------------------------------------------------------------

# 11. Buttons

## Primary

Cyan background with dark text.

``` text
+-------------------------+
|       + ADD RECORD      |
+-------------------------+
```

## Secondary

Dark surface with cyan/gray border.

## Ghost

Transparent with muted text; cyan on hover.

## Danger

Reserved for destructive operations.

Buttons should use verbs:

-   Add record
-   Save changes
-   Complete task
-   Upload document
-   Schedule
-   View history
-   Export report

Avoid vague labels such as "Submit" whenever possible.

------------------------------------------------------------------------

# 12. Forms

Forms should be extremely clear because this product stores important
records.

Input:

``` css
input,
textarea,
select {
  background: var(--kh-surface-2);
  border: 1px solid var(--kh-border);
  color: var(--kh-text);
  border-radius: var(--radius-md);
  min-height: 44px;
}

input:focus,
textarea:focus,
select:focus {
  outline: 2px solid var(--kh-primary);
  outline-offset: 1px;
}
```

Always display:

-   Field label
-   Helpful description when needed
-   Validation state
-   Error explanation

Never rely exclusively on placeholder text.

------------------------------------------------------------------------

# 13. Tables & Logs

Logs are a major part of the product.

Use:

-   Strong date hierarchy
-   Compact rows
-   Status badges
-   Person/category icons
-   Expandable details

Example:

``` text
DATE        TYPE          PERSON       STATUS       ACTION
Aug 31      Medication    John         Completed    View
Aug 30      Maintenance   Household    Completed    View
Aug 29      Appointment   Jane         Upcoming     View
```

Desktop should support dense tables.

Mobile should convert rows into cards.

------------------------------------------------------------------------

# 14. Timeline Component

For activity/history:

``` text
● Aug 31 · 8:00 AM
  Medication administered
  Jane Doe
  Completed

│
● Aug 30 · 4:30 PM
  HVAC filter replaced
  Living room
  Completed

│
● Aug 29 · 10:00 AM
  Doctor appointment scheduled
  John Doe
  Upcoming
```

Use a subtle vertical cyan line and small status markers.

------------------------------------------------------------------------

# 15. Status Badges

Examples:

``` text
✓ COMPLETED
● UPCOMING
! DUE SOON
× OVERDUE
i INFORMATION
```

Style:

-   Small
-   Rounded
-   Uppercase only for short labels
-   Icon + text

Do not use giant colored pills.

------------------------------------------------------------------------

# 16. Empty States

Empty states should feel helpful, not broken.

Example:

**No maintenance records yet**

> Start building your home's maintenance history so important tasks
> never get forgotten.

Primary action:

**+ Add maintenance record**

Use a simple line icon, preferably a home/shield/tool motif.

------------------------------------------------------------------------

# 17. Alerts

Alerts should be prioritized.

### Critical

Used sparingly.

### Warning

For upcoming deadlines or expiring records.

### Information

For normal system messages.

Example:

``` text
⚠  HVAC filter is due in 5 days
   Last replaced 3 months ago

   [View maintenance]
```

------------------------------------------------------------------------

# 18. Navigation Labels

Recommended primary navigation:

``` text
Dashboard
Household
Members
Maintenance
Medications
Health
Behavior & Discipline
Documents
Appointments
Contacts
Reports
Activity
Settings
```

Depending on the application structure, some areas can be grouped under:

**CARE** - Members - Medications - Health - Appointments - Behavior

**HOME** - Household - Maintenance - Documents - Contacts

**RECORDS** - Activity - Reports

------------------------------------------------------------------------

# 19. Landing Page

Suggested structure:

## Hero

**Your home. Your records. One secure place.**

Subheading:

> Kumpe Home Logs helps families and caregivers maintain organized
> records for the people, property, medications, maintenance,
> appointments, and important events that make up everyday home life.

Buttons:

**Get Started**\
**See How It Works**

Hero visual:

-   Dark background
-   Large shield/logo
-   Subtle cyan radial glow
-   Dashboard preview
-   No stock family photography required

## Feature section

Six feature cards:

1.  Home Maintenance
2.  Medications
3.  Health Records
4.  Household & Family
5.  Documents
6.  Activity & Reports

## Trust section

Emphasize:

-   Organized
-   Private
-   Accountable
-   Accessible
-   Built for real homes

------------------------------------------------------------------------

# 20. Foster Home Positioning

The brand must work for foster families without making the entire
product look like a government/medical application.

Recommended language:

> **Built for everyday homes and the people who care for them.**

Secondary message:

> Whether you're managing a busy family household or keeping detailed
> foster-care records, Kumpe Home Logs gives you one organized place to
> document what matters.

Avoid:

-   "case management" as the primary brand language
-   Institutional imagery
-   Excessive medical symbols
-   Fear-based messaging

------------------------------------------------------------------------

# 21. Iconography

Use a consistent outline icon set.

Recommended style:

-   1.75--2px stroke
-   Rounded line caps
-   Simple geometric construction
-   Minimal detail

Icon themes:

-   Home
-   Shield
-   Wrench
-   Pill
-   Heart/ECG
-   Clipboard
-   Family
-   Calendar
-   File
-   Bell
-   User
-   Lock
-   Check
-   Alert

The shield and home should be recurring secondary motifs.

------------------------------------------------------------------------

# 22. Motion

Motion should communicate state, not decorate the interface.

Recommended:

-   120--200ms transitions
-   Subtle card lift
-   Fade/slide for panels
-   Smooth modal entry
-   Progress animation

Avoid:

-   Constant glowing animations
-   Excessive parallax
-   Bouncing buttons
-   Long page transitions

Respect:

``` css
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

------------------------------------------------------------------------

# 23. Responsive Design

Breakpoints:

``` css
--bp-sm: 640px;
--bp-md: 768px;
--bp-lg: 1024px;
--bp-xl: 1280px;
--bp-2xl: 1536px;
```

### Mobile

Prioritize:

1.  Dashboard
2.  Add record
3.  Alerts
4.  Today's tasks
5.  Activity

Use large touch targets.

Minimum interactive target:

**44 × 44px**

------------------------------------------------------------------------

# 24. Accessibility

Target WCAG 2.2 AA.

Requirements:

-   Keyboard navigation
-   Visible focus states
-   Semantic HTML
-   Proper labels
-   Screen-reader-friendly icons
-   Minimum contrast requirements
-   Do not communicate status by color alone
-   Accessible dialogs
-   Accessible tables
-   Reduced-motion support

------------------------------------------------------------------------

# 25. Dark Mode

Dark mode is the primary brand experience.

Example:

``` text
Page background     #050708
Surface             #0D1519
Elevated surface    #111D22
Border              #20343A
Primary cyan        #10D9E8
Primary text        #F4FAFB
Secondary text      #B7C8CC
Muted text          #71858A
```

Light mode should preserve the same cyan brand accent while using soft
blue-gray backgrounds rather than pure white everywhere.

------------------------------------------------------------------------

# 26. Security / Privacy Visual Language

Because Home Logs can contain sensitive household information, privacy
should be visible without being intimidating.

Use:

-   Shield iconography
-   Lock indicators
-   "Private" labels
-   Clear session/account controls
-   Audit/history indicators

Avoid claiming specific certifications or regulatory compliance unless
the product actually has them.

Preferred messaging:

> **Your household records belong in a place you trust.**

------------------------------------------------------------------------

# 27. Data Visualization

Use restrained charts.

Good examples:

-   Maintenance completion over time
-   Medication adherence history
-   Upcoming deadlines
-   Household activity
-   Expense history

Use cyan as the primary data accent and status colors only when
meaningful.

Never create rainbow charts.

------------------------------------------------------------------------

# 28. Brand Voice

## Voice

-   Calm
-   Clear
-   Protective
-   Respectful
-   Practical
-   Modern
-   Human

## Writing style

Prefer:

> "Your HVAC filter is due in 5 days."

Over:

> "ATTENTION! Your maintenance task requires immediate action!"

Prefer:

> "3 records need your attention."

Over:

> "You have 3 outstanding tasks!!!"

The product should feel like a capable assistant, not an alarm system.

------------------------------------------------------------------------

# 29. Recommended Component Library

Create reusable components:

``` text
AppShell
Sidebar
TopBar
MobileNav
HouseholdSelector
PageHeader
StatCard
RecordCard
RecordTable
Timeline
StatusBadge
AlertBanner
EmptyState
SearchBar
FilterBar
DatePicker
PersonSelector
FileUploader
DocumentCard
QuickAdd
Modal
Drawer
ConfirmDialog
Toast
ProgressIndicator
ActivityFeed
```

Build components from the design tokens rather than hard-coding
individual page styles.

------------------------------------------------------------------------

# 30. Cursor Implementation Brief

Paste the following into Cursor as the high-level design instruction:

> Redesign the Kumpe Home Logs frontend using the provided brand
> guidelines.
>
> The existing shield logo and distinctive double-K monogram are the
> authoritative brand assets. Preserve the double-K exactly; do not
> redraw or reinterpret it.
>
> Build a polished, modern, security-conscious home management
> application using a dark black/blue-black foundation with electric
> cyan/teal accents and white typography.
>
> The visual identity should feel like a combination of a premium
> technology dashboard, a trusted household record system, and a
> protective shield. It must work equally well for traditional family
> homes and foster homes.
>
> Use reusable components, CSS variables/design tokens, responsive
> layouts, accessible controls, consistent status states, and strong
> information hierarchy.
>
> Do not introduce purple SaaS gradients, cartoon styling, pastel
> family-app aesthetics, excessive glassmorphism, or excessive
> animations.
>
> Primary UX principles:
>
> 1.  Important information should be visible immediately.
> 2.  Adding a record should require minimal friction.
> 3.  Logs should be easy to scan and audit.
> 4.  Upcoming/overdue items should be obvious.
> 5.  Privacy and security should be visually apparent without becoming
>     intimidating.
> 6.  Mobile must be a first-class experience.
> 7.  Use icons and text together rather than relying on color alone.
>
> The primary product navigation should include Dashboard, Household,
> Members, Maintenance, Medications, Health, Behavior & Discipline,
> Documents, Appointments, Contacts, Reports, Activity, and Settings.
>
> The dashboard should emphasize today's activity, alerts, upcoming
> tasks, recent records, and quick actions.
>
> Use the supplied logo asset wherever the brand identity is displayed.
> Keep sufficient clear space around it.
>
> Implement the brand tokens supplied in the Kumpe Home Logs brand guide
> and avoid introducing arbitrary colors unless required for
> accessibility or semantic status states.

------------------------------------------------------------------------

# 31. CSS Starter

``` css
:root {
  --brand: #10D9E8;
  --brand-bright: #20F3FF;
  --brand-dark: #0798A8;

  --bg: #050708;
  --surface: #0D1519;
  --surface-2: #111D22;
  --surface-3: #16262C;

  --text: #F4FAFB;
  --text-secondary: #B7C8CC;
  --text-muted: #71858A;

  --border: #20343A;
  --border-hover: #2C5961;

  --success: #32D583;
  --warning: #F5B83D;
  --danger: #F05D67;
  --info: #55B8FF;

  --radius-sm: 6px;
  --radius-md: 10px;
  --radius-lg: 16px;
  --radius-xl: 22px;
  --radius-pill: 999px;

  --shadow-sm: 0 2px 8px rgba(0,0,0,.18);
  --shadow-md: 0 8px 24px rgba(0,0,0,.25);
  --shadow-lg: 0 16px 48px rgba(0,0,0,.35);

  --focus: 0 0 0 3px rgba(16,217,232,.28);
}

body {
  margin: 0;
  background: var(--bg);
  color: var(--text);
  font-family:
    Inter,
    ui-sans-serif,
    system-ui,
    -apple-system,
    BlinkMacSystemFont,
    "Segoe UI",
    sans-serif;
}

.card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-sm);
}

.button-primary {
  background: var(--brand);
  color: #031013;
  border: 0;
  border-radius: var(--radius-md);
  min-height: 44px;
  padding: 0 18px;
  font-weight: 700;
  cursor: pointer;
  transition: 160ms ease;
}

.button-primary:hover {
  background: var(--brand-bright);
  transform: translateY(-1px);
}

.button-secondary {
  background: var(--surface-2);
  color: var(--text);
  border: 1px solid var(--border-hover);
  border-radius: var(--radius-md);
  min-height: 44px;
  padding: 0 18px;
  font-weight: 600;
}

:focus-visible {
  outline: none;
  box-shadow: var(--focus);
}
```

------------------------------------------------------------------------

# 32. Final Design Principle

Kumpe Home Logs should look like a **digital shield around the home**.

The shield represents protection.

The double-K represents Kumpe.

The house represents home.

The records represent accountability.

The cyan technology language represents the modern system connecting
everything together.

Every screen should reinforce that idea without becoming visually
repetitive.
