# First Prompt for Google AI Studio

Copy and paste this prompt to start building your Namaazly app:

---

**You are an expert mobile app developer. Build a complete, functional React mobile app called "Namaazly" - an Islamic prayer times and Ramadan support app.**

## App Overview
**Purpose:** A lightweight, distraction-free app to help Muslims track daily prayer times and stay engaged during Ramadan.

**Target Users:** Muslims of all ages who want a simple, focused Islamic app that works offline.

## Core Features to Build

### 1. Daily Prayer Times Screen (Main/Home Screen)
- Display 5 daily prayers: Fajr, Zuhr, Asr, Maghrib, Isha
- Show current time and countdown to next prayer
- Highlight which prayer is current/upcoming with visual emphasis
- Each prayer should have:
  - Prayer name
  - Calculated time display
  - Adjustment controls: + and - buttons (adjust by ±1 minute, max ±15 minutes)
  - Visual badge/indicator if time was manually adjusted from default
  - Small reset icon to restore default time

### 2. Location Setup & Selection
- On first launch, show welcome screen then location setup
- Provide searchable dropdown/list of major global cities (at least 50 cities)
- Include cities from: USA, UK, Canada, Saudi Arabia, UAE, Pakistan, India, Egypt, Turkey, Malaysia, Indonesia, etc.
- Store selected city with its coordinates locally
- Display current city name at top of prayer times screen
- Allow changing city from settings anytime

### 3. Prayer Time Calculation
- Calculate accurate prayer times based on city coordinates
- Support multiple calculation methods:
  - Muslim World League (default)
  - Islamic Society of North America (ISNA)
  - Egyptian General Authority
  - Umm al-Qura (Makkah)
- User selects preferred method in settings
- Use standard prayer time calculation algorithms
- All calculations work offline (no API calls needed)

### 4. Ramadan Module

**Ramadan Dashboard Screen:**
- Accessible via bottom navigation or tab
- Shows:
  - Current Ramadan day: "Day 5 of 30"
  - Sehri (Suhoor) time with live countdown timer
  - Iftaar time with live countdown timer
  - Clear visual separation between Sehri and Iftaar sections
- Manual Ramadan start date picker (calendar input)
- Toggle to enable/disable Ramadan mode manually
- Auto-calculate which day of Ramadan it is based on start date

**30 Days Ramadan Challenge:**
- Separate screen/section accessible from Ramadan dashboard
- Display today's Islamic task based on current Ramadan day
- Pre-define 30 different daily tasks, examples:
  - Day 1: "Give charity to someone in need"
  - Day 2: "Call a family member you haven't spoken to recently"
  - Day 3: "Forgive someone who wronged you"
  - Day 4: "Read Surah Al-Mulk before sleep"
  - Day 5: "Share food with a neighbor"
  - (Continue with 25 more meaningful, simple tasks)
- Large, prominent checkbox to mark today's task complete
- Visual confirmation when checked (animation or color change)
- Progress section showing:
  - Completed days count: "12/30 days completed"
  - Progress bar (visual indicator)
  - Percentage: "40% complete"
- "View All Tasks" option showing all 30 days with completion status
- Persist completion data locally (don't lose progress on app close)

### 5. Settings Screen
Organized sections:
- **Location:** Current city with change button
- **Prayer Settings:**
  - Calculation method dropdown
  - Asr calculation: Standard or Hanafi
  - Individual prayer adjustments summary
  - Reset all adjustments button
- **Ramadan Settings:**
  - Set Ramadan start date
  - Enable/Disable Ramadan mode toggle
  - Reset challenge progress button (with confirmation)
- **Notifications:**
  - Enable/disable prayer reminders
  - Reminder timing: 5, 10, 15, or 30 minutes before
  - Individual toggles for each prayer
  - Ramadan Sehri/Iftaar reminder toggles
- **Display:**
  - Time format: 12-hour or 24-hour
  - Theme: Light, Dark, or Auto
- **About:** App version, credits

### 6. Navigation Structure
- Bottom navigation or tab bar with:
  - Home (Prayer Times) - default screen
  - Ramadan (only show during Ramadan mode)
  - Settings
- Simple, clear navigation icons
- Active tab highlighted

## Design Requirements
- **Mobile-first responsive design** (optimized for 375px to 428px width)
- **Color scheme:**
  - Primary: Deep teal or Islamic green (#0D7377 or #2E8B57)
  - Accent: Warm gold (#D4AF37)
  - Background: Soft white (#F8F9FA) for light mode, dark gray for dark mode
  - Text: High contrast for readability
- **Typography:**
  - Large, clear fonts (minimum 16px for body text)
  - Prayer names in bold, larger size
  - Times very prominent and easy to read
- **UI Elements:**
  - Rounded corners for cards and buttons
  - Subtle shadows for depth
  - Generous spacing and padding
  - Large touch targets (minimum 44px for buttons)
- **Subtle Islamic touches:**
  - Optional geometric pattern in header
  - Crescent moon icon for Ramadan
  - Clean, minimal aesthetic (not overly decorative)

## Technical Requirements
- Use React with TypeScript
- Use local storage for all data persistence
- Implement prayer time calculation logic (you can use standard formulas)
- Create reusable components
- Responsive design that works on mobile, tablet, desktop
- No external API calls - everything works offline
- Fast performance and smooth animations

## Data to Include
- Pre-populate at least 50 major cities with coordinates:
  - USA: New York, Los Angeles, Chicago, Houston, Miami, etc.
  - UK: London, Birmingham, Manchester
  - Canada: Toronto, Montreal, Vancouver
  - Middle East: Makkah, Madinah, Dubai, Riyadh, Cairo, Istanbul
  - South Asia: Karachi, Lahore, Delhi, Mumbai, Dhaka
  - Southeast Asia: Jakarta, Kuala Lumpur, Singapore
  - Add more as needed

- Pre-write all 30 Ramadan Challenge tasks (simple, universal, meaningful)

## Build Priority
**Phase 1 (Build This First):**
1. Prayer times home screen with all 5 prayers
2. Location selector with cities dropdown
3. Prayer time calculation (Muslim World League method)
4. Time adjustment feature with +/- buttons
5. Basic settings screen
6. Local storage for saving user preferences
