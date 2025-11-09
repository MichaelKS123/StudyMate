# StudyMate 📚 - Online Study Planner

**Author:** Michael Semera  
**Project Type:** Web Application (HTML/CSS/JavaScript)  
**Domain:** Education & Productivity

---

## 🎓 Project Overview

StudyMate is a comprehensive online study planner that helps students manage their study time effectively. With built-in timer functionality, subject tracking, statistics, and Google Calendar integration, StudyMate provides everything students need to stay organized and productive.

### Key Features

✅ **Subject Management** - Add and organize multiple subjects with color coding  
✅ **Study Timer** - Track study sessions with start/pause/stop functionality  
✅ **Time Tracking** - Automatic calculation of time spent per subject  
✅ **Progress Monitoring** - Visual progress bars for weekly targets  
✅ **Statistics Dashboard** - Comprehensive study analytics  
✅ **Session History** - Complete log of all study sessions  
✅ **Google Calendar Sync** - Export study sessions to iCalendar format  
✅ **Local Storage** - Data persists between sessions  
✅ **Responsive Design** - Works on desktop, tablet, and mobile  
✅ **Beautiful UI** - Modern, gradient-based interface  

---

## 🚀 Quick Start

### Installation

**Option 1: Direct Use**
1. Download `studymate.html`
2. Open in any modern web browser
3. Start adding subjects and tracking time!

**Option 2: Local Server (Recommended)**
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Then open: http://localhost:8000/studymate.html
```

**Option 3: GitHub Pages**
1. Fork this repository
2. Enable GitHub Pages in Settings
3. Access at: `https://yourusername.github.io/studymate`

### First Steps

1. **Add Your Subjects**
   - Click "Add Subject"
   - Enter subject name (e.g., "Mathematics")
   - Choose a color
   - Set weekly target hours
   - Click "Add Subject"

2. **Start Studying**
   - Select a subject from the timer dropdown
   - Click "▶️ Start" to begin timing
   - Focus on your studies
   - Click "⏹️ Stop & Save" when done

3. **Track Progress**
   - View statistics on the dashboard
   - Check recent sessions
   - Monitor weekly targets

4. **Sync with Calendar**
   - Click "📤 Export to Calendar"
   - Download the `.ics` file
   - Import to Google Calendar

---

## 💼 Core Functionality

### 1. Subject Management

**Add Subjects:**
- Subject name
- Custom color for visual identification
- Weekly target hours
- Automatic time tracking

**Features:**
- Color-coded organization
- Progress bars showing completion %
- Total time studied per subject
- Easy deletion with confirmation

**Example:**
```
Mathematics (Blue)
⏱️ 12h 30m studied
🎯 15h/week target
Progress: 83%
```

### 2. Study Timer

**Functionality:**
- Start/Pause/Resume/Stop controls
- Real-time display (HH:MM:SS)
- Subject selection
- Automatic session saving

**Usage Flow:**
1. Select subject
2. Start timer
3. Study (timer counts up)
4. Pause if needed (optional)
5. Stop and save (adds to history)

**Display:**
```
⏱️ Study Timer
[Mathematics]

01:45:32

▶️ Start  ⏸️ Pause  ⏹️ Stop & Save
```

### 3. Statistics Dashboard

**Metrics Tracked:**
- **Total Study Time** - All subjects combined
- **Active Subjects** - Number of subjects added
- **Sessions Today** - Study sessions completed today
- **Avg Session** - Average session duration

**Real-time Updates:**
- Updates after each session
- Persistent across browser sessions
- Visual stat cards with large numbers

### 4. Session History

**Information Stored:**
- Subject name and color
- Start date and time
- Duration
- Date display

**Features:**
- Most recent 10 sessions displayed
- Color-coded by subject
- Formatted timestamps
- Duration badges

**Example Entry:**
```
[Blue Bar] Mathematics        [1h 45m]
📅 11/09/2024 at 14:30:00
```

### 5. Google Calendar Integration

**Export Process:**
1. Click "📤 Export to Calendar"
2. Download `studymate-sessions.ics`
3. Open Google Calendar
4. Click "+" next to "Other calendars"
5. Select "Import"
6. Choose downloaded file
7. Study sessions appear in calendar!

**iCalendar Format:**
- Industry-standard `.ics` format
- Compatible with all major calendar apps
- Includes all session details
- Color-coded events
- Proper timezone handling

---

## 🎨 User Interface

### Design Philosophy

**Modern & Clean:**
- Gradient backgrounds
- Smooth animations
- Card-based layout
- Intuitive icons

**Color Scheme:**
```
Primary: #6366f1 (Indigo)
Success: #10b981 (Green)
Warning: #f59e0b (Amber)
Danger: #ef4444 (Red)
```

**Responsive Layout:**
- Desktop: Two-column grid
- Tablet: Adaptive layout
- Mobile: Single column, optimized touch

### Visual Components

**Subject Cards:**
- Color-coded left border
- Progress bars
- Hover effects
- Action buttons

**Timer Display:**
- Large digital clock
- High contrast
- Monospace font for clarity
- Gradient background

**Statistics:**
- Four-card grid
- Large numbers
- Descriptive labels
- Gradient backgrounds

---

## 🔧 Technical Details

### Architecture

**Single-Page Application (SPA):**
- No server required
- Pure client-side
- Instant interactions
- Offline capable

**Technology Stack:**
- **HTML5** - Structure
- **CSS3** - Styling (gradients, animations, responsive)
- **JavaScript (ES6+)** - Logic and interactivity
- **LocalStorage API** - Data persistence
- **iCalendar Format** - Calendar export

### Code Structure

```javascript
class StudyMate {
    // Core properties
    subjects: []      // Array of subject objects
    sessions: []      // Array of session objects
    timerInterval: null
    currentSession: null
    
    // Main methods
    initializeApp()           // Setup
    addSubject()              // Add new subject
    deleteSubject(id)         // Remove subject
    startTimer()              // Begin timing
    pauseTimer()              // Pause/resume
    stopTimer()               // Stop and save
    syncToCalendar()          // Export to .ics
    renderSubjects()          // Display subjects
    renderSessions()          // Display history
    updateStatistics()        // Calculate stats
}
```

### Data Models

**Subject Object:**
```javascript
{
    id: "1699123456789",        // Unique timestamp ID
    name: "Mathematics",        // Subject name
    color: "#6366f1",          // Hex color
    targetHours: 15,           // Weekly goal
    totalMinutes: 750,         // Time studied
    createdAt: "2024-11-09"    // ISO date
}
```

**Session Object:**
```javascript
{
    subjectId: "1699123456789",
    subjectName: "Mathematics",
    subjectColor: "#6366f1",
    startTime: "2024-11-09T14:30:00.000Z",
    endTime: "2024-11-09T16:15:00.000Z",
    duration: 6300              // Seconds
}
```

### LocalStorage Keys

```
studymate_subjects  // Array of subjects
studymate_sessions  // Array of sessions
```

**Storage Size:**
- Typical subject: ~200 bytes
- Typical session: ~150 bytes
- 100 sessions + 10 subjects: ~20KB
- LocalStorage limit: 5-10MB (plenty!)

---

## 📊 Features in Detail

### Progress Tracking

**Weekly Target System:**
```
Target: 15 hours/week
Studied: 12.5 hours
Progress: 83.3%

Visual: [█████████████░░░] 83%
```

**Calculations:**
- Minutes studied ÷ 60 = Hours
- (Hours / Target) × 100 = Progress %
- Capped at 100% for display

### Timer Mechanism

**Implementation:**
```javascript
// Start
setInterval(() => {
    if (!isPaused) {
        elapsedSeconds++;
        updateDisplay();
    }
}, 1000);

// Display format
const hours = Math.floor(seconds / 3600);
const minutes = Math.floor((seconds % 3600) / 60);
const secs = seconds % 60;

display = `${hours}:${minutes}:${secs}`;
```

**Features:**
- 1-second precision
- Pause/resume capability
- No drift (uses fixed interval)
- Updates subject totals on save

### Statistics Calculation

**Total Study Time:**
```javascript
totalMinutes = subjects.reduce((sum, s) => 
    sum + s.totalMinutes, 0
);
totalHours = Math.floor(totalMinutes / 60);
```

**Sessions Today:**
```javascript
sessionsToday = sessions.filter(s => {
    const sessionDate = new Date(s.startTime);
    const today = new Date();
    return sessionDate.toDateString() === today.toDateString();
}).length;
```

**Average Session:**
```javascript
avgDuration = sessions.reduce((sum, s) => 
    sum + s.duration, 0
) / sessions.length;
```

### Calendar Export Format

**iCalendar (.ics) Structure:**
```
BEGIN:VCALENDAR
VERSION:2.0
PRODID:-//StudyMate by Michael Semera//EN

BEGIN:VEVENT
UID:unique-id@studymate.com
DTSTART:20241109T143000Z
DTEND:20241109T161500Z
SUMMARY:Study Session: Mathematics
DESCRIPTION:Duration: 1h 45m
CATEGORIES:EDUCATION,STUDY
COLOR:#6366f1
END:VEVENT

END:VCALENDAR
```

**Benefits:**
- Standard format
- Universal compatibility
- Import to any calendar app
- Preserves all metadata

---

## 🎯 Use Cases

### For Students

**Daily Study Routine:**
1. Morning: Review subjects for the day
2. Start timer for each study block
3. Take breaks between subjects
4. Review progress at end of day
5. Export to calendar weekly

**Exam Preparation:**
- Set higher weekly targets
- Track time per topic
- Monitor progress bars
- Ensure balanced coverage

**Project Management:**
- Create subjects for each project
- Track research/writing time
- Meet deadlines with targets
- Visualize time investment

### For Teachers/Parents

**Monitor Study Habits:**
- Review session history
- Check time distribution
- Verify weekly targets met
- Encourage consistency

**Goal Setting:**
- Set realistic weekly targets
- Adjust based on performance
- Track improvement over time

### For Self-Learners

**Skill Development:**
- Track online course time
- Monitor tutorial sessions
- Balance multiple learning paths
- Maintain consistency

---

## 🔐 Privacy & Data

### Data Storage

**Location:** Browser LocalStorage (client-side only)

**What's Stored:**
- Subject names and settings
- Study session records
- Timer preferences

**What's NOT Stored:**
- Personal information
- Login credentials
- Study content
- Location data

### Privacy Features

✅ **Completely Local** - No data sent to servers  
✅ **No Tracking** - No analytics or cookies  
✅ **No Account Required** - Works immediately  
✅ **Offline Capable** - Functions without internet  
✅ **Export Control** - You control calendar data  

### Data Management

**Backup:**
```javascript
// Manual backup (Developer Console)
const backup = {
    subjects: localStorage.getItem('studymate_subjects'),
    sessions: localStorage.getItem('studymate_sessions')
};
console.log(JSON.stringify(backup));
// Copy and save to file
```

**Restore:**
```javascript
// Restore from backup
localStorage.setItem('studymate_subjects', backup.subjects);
localStorage.setItem('studymate_sessions', backup.sessions);
location.reload();
```

**Clear Data:**
```javascript
// Clear all StudyMate data
localStorage.removeItem('studymate_subjects');
localStorage.removeItem('studymate_sessions');
location.reload();
```

---

## 🚀 Future Enhancements

### Planned Features

- [ ] **Cloud Sync** - Optional account for multi-device
- [ ] **Study Goals** - Long-term goal tracking
- [ ] **Pomodoro Timer** - 25/5 minute technique
- [ ] **Break Reminders** - Notifications for breaks
- [ ] **Study Streaks** - Daily streak counter
- [ ] **Dark Mode** - Eye-friendly theme
- [ ] **Graphs & Charts** - Visual analytics
- [ ] **Study Groups** - Collaborative features
- [ ] **Focus Music** - Built-in background music
- [ ] **Achievement Badges** - Gamification

### Technical Improvements

- [ ] PWA Support - Install as app
- [ ] IndexedDB - More storage capacity
- [ ] Service Worker - Offline enhancements
- [ ] Web Notifications - Study reminders
- [ ] Export Formats - PDF, CSV reports
- [ ] Import Data - From other apps

---

## 🤝 Contributing

This is a portfolio project by Michael Semera, but contributions are welcome!

**How to Contribute:**
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

**Areas for Contribution:**
- Bug fixes
- UI/UX improvements
- New features
- Documentation
- Translations

---

## 📄 License

**License:** MIT License  
**Copyright:** © 2024 Michael Semera

Free to use, modify, and distribute with attribution.

---

## 📧 Contact

**Michael Semera**  
Portfolio Project: StudyMate  
*Online Study Planner with Google Calendar Integration*

- 💼 LinkedIn: [Michael Semera](https://www.linkedin.com/in/michael-semera-586737295/)
- 🐙 GitHub: [@MichaelKS123](https://github.com/MichaelKS123)
- 📧 Email: michaelsemera15@gmail.com

---

## 🙏 Acknowledgments

- Inspired by productivity and time management principles
- Built with modern web technologies
- Designed for student success
- Created as a portfolio showcase

---

## 📚 Browser Compatibility

**Fully Supported:**
- ✅ Chrome/Edge 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Opera 76+

**Features Used:**
- ES6+ JavaScript (Classes, Arrow Functions, Template Literals)
- CSS Grid & Flexbox
- LocalStorage API
- Blob API (for downloads)
- Modern date/time handling

---

## 🎯 Project Goals Achieved

✅ Study time tracking  
✅ Subject organization  
✅ Timer functionality  
✅ Google Calendar integration  
✅ Statistics dashboard  
✅ Session history  
✅ Responsive design  
✅ Local data persistence  
✅ Clean, original code  
✅ Professional UI/UX  
✅ Portfolio-ready quality  

---

**Version:** 1.0.0  
**Status:** Production Ready  
**Last Updated:** November 2024

**Created with 📚 by Michael Semera for helping students succeed**