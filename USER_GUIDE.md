# StudyMate User Guide

**Complete Guide to Using StudyMate Effectively**  
**Author:** Michael Semera

---

## 📖 Table of Contents

1. [Getting Started](#getting-started)
2. [Adding Subjects](#adding-subjects)
3. [Using the Timer](#using-the-timer)
4. [Understanding Statistics](#understanding-statistics)
5. [Reviewing Sessions](#reviewing-sessions)
6. [Syncing with Google Calendar](#syncing-with-google-calendar)
7. [Tips & Best Practices](#tips--best-practices)
8. [Troubleshooting](#troubleshooting)

---

## Getting Started

### Opening StudyMate

**Method 1: Direct File**
1. Download `studymate.html`
2. Double-click to open in browser
3. Ready to use!

**Method 2: GitHub Pages**
Visit your hosted URL (if deployed)

**Method 3: Local Server**
```bash
python -m http.server 8000
# Open: http://localhost:8000/studymate.html
```

### First Impressions

When you open StudyMate, you'll see:
- 📚 Header with title and author credit
- ➕ Subject form on the left
- 📖 Subject list on the right
- ⏱️ Study timer in the center
- 📊 Statistics dashboard
- 📅 Recent sessions
- 🗓️ Calendar sync button

---

## Adding Subjects

### Step-by-Step

**1. Locate the "Add Subject" Card**
- Top-left section
- Purple/blue gradient form

**2. Fill in Subject Details:**

**Subject Name** (Required)
- Enter the course or topic name
- Examples: "Mathematics", "Spanish", "Chemistry"
- Be specific: "Calculus I" vs just "Math"

**Color** (Optional)
- Click the color picker
- Choose a unique color per subject
- Helps visual identification
- Default: Blue (#6366f1)

**Weekly Target** (Required)
- Set realistic hours per week
- Typical: 5-15 hours
- Adjust based on difficulty
- Default: 5 hours

**3. Click "Add Subject"**

### Subject Card Display

After adding, each subject shows:
```
[Color Dot] Mathematics

⏱️ 0h 0m studied
🎯 10h/week target

[Progress Bar: 0%]

[🗑️ Delete]
```

### Managing Subjects

**View All Subjects:**
- Displayed in "My Subjects" section
- Shows all active subjects
- Color-coded for easy identification

**Delete a Subject:**
1. Click 🗑️ button on subject card
2. Confirm deletion
3. All related sessions are also deleted
4. Cannot be undone!

**Edit a Subject:**
- Currently: Delete and recreate
- Future update: Edit button

---

## Using the Timer

### Starting a Study Session

**1. Select Subject**
- Open timer dropdown
- Choose from your subjects
- Can't start without selection

**2. Click ▶️ Start**
- Timer begins at 00:00:00
- Counts up continuously
- Start button becomes disabled

**3. Study!**
- Focus on your work
- Timer runs in background
- Tab can remain open

### Pausing the Timer

**When to Pause:**
- Quick bathroom break
- Answer phone call
- Brief interruption

**How to Pause:**
1. Click ⏸️ Pause
2. Timer stops counting
3. Button changes to ▶️ Resume
4. Click again to continue

**Note:** Pause/resume doesn't create separate sessions

### Stopping and Saving

**When to Stop:**
- Study session complete
- Switching subjects
- Taking extended break

**How to Stop:**
1. Click ⏹️ Stop & Save
2. Session saves automatically
3. Time added to subject total
4. Appears in recent sessions
5. Timer resets to 00:00:00

### Timer States

```
State 1: Ready
- Subject dropdown: Enabled
- Start: Enabled
- Pause: Disabled
- Stop: Disabled

State 2: Running
- Subject dropdown: Disabled
- Start: Disabled
- Pause: Enabled
- Stop: Enabled

State 3: Paused
- Pause button shows "Resume"
- Can resume or stop
```

---

## Understanding Statistics

### Statistics Dashboard

Four key metrics displayed:

**1. Total Study Time**
```
[12h]
Total Study Time
```
- Sum of all subjects
- All-time total
- Updates after each session

**2. Active Subjects**
```
[5]
Active Subjects
```
- Number of subjects added
- Includes subjects with 0 time
- Increases when adding subjects

**3. Sessions Today**
```
[3]
Sessions Today
```
- Completed sessions today
- Resets at midnight (local time)
- Counts individual timer stops

**4. Average Session**
```
[45m]
Avg Session
```
- Mean duration of all sessions
- Helps track focus periods
- Excludes very short sessions

### Progress Tracking

**Subject Progress Bars:**
```
Mathematics
⏱️ 8h 30m studied
🎯 10h/week target

[████████████░░░░] 85%
```

**How It Works:**
- (Time Studied ÷ Weekly Target) × 100
- Example: 8.5h ÷ 10h = 85%
- Caps at 100% for display
- Green color indicates progress

**Interpreting Progress:**
- 0-30%: Behind schedule
- 30-70%: On track
- 70-100%: Good progress
- 100%+: Target achieved!

---

## Reviewing Sessions

### Recent Sessions View

**Location:** Bottom-right card

**Display Format:**
```
[Blue Bar] Mathematics     [1h 30m]
📅 11/09/2024 at 14:30:00
```

**Information Shown:**
- Subject name (with color)
- Session duration
- Date and time started

### Session History

**Default View:**
- 10 most recent sessions
- Newest first (top)
- Color-coded by subject

**Reading Sessions:**
```
Subject: Mathematics
Duration: 1h 30m
Date: November 9, 2024
Time: 2:30 PM
```

### Using Session Data

**Weekly Review:**
1. Check sessions from past 7 days
2. Count sessions per subject
3. Verify targets being met
4. Adjust schedule as needed

**Monthly Analysis:**
1. Export to calendar (see below)
2. View monthly patterns
3. Identify peak productivity
4. Plan next month

---

## Syncing with Google Calendar

### Why Sync?

**Benefits:**
- Visualize study schedule
- Share with parents/teachers
- Set reminders
- Track long-term patterns
- Backup study data

### Export Process

**Step 1: Generate Calendar File**
1. Click "📤 Export to Calendar"
2. File downloads automatically
3. Filename: `studymate-sessions.ics`
4. Location: Default downloads folder

**Step 2: Import to Google Calendar**

**On Desktop:**
1. Open [Google Calendar](https://calendar.google.com)
2. Click "+" next to "Other calendars"
3. Select "Import"
4. Click "Select file from your computer"
5. Choose `studymate-sessions.ics`
6. Select calendar to import into
7. Click "Import"
8. Sessions appear instantly!

**On Mobile:**
1. Open email with .ics attachment
2. Or upload .ics to Google Drive
3. Open file
4. Tap "Add to Calendar"
5. Confirm import

### Viewing in Calendar

**What You'll See:**
```
Calendar Event:
Title: Study Session: Mathematics
Time: 2:30 PM - 4:00 PM
Description: StudyMate study session
             Duration: 1h 30m
Color: Subject's color
Category: EDUCATION, STUDY
```

**Features:**
- Color-coded by subject
- Exact start/end times
- Duration in description
- Searchable
- Can set reminders

### Re-importing

**Update Process:**
1. Export new .ics file
2. Import to same calendar
3. New sessions added
4. Duplicates possible if re-importing same sessions

**Best Practice:**
- Export weekly
- Create separate "StudyMate" calendar
- Review before importing

---

## Tips & Best Practices

### Effective Subject Setup

**Be Specific:**
- ❌ "Math"
- ✅ "Calculus I"
- ✅ "Algebra - Chapter 5"

**Use Colors Strategically:**
- Similar subjects: Similar colors
- Priority subjects: Bright colors
- Difficult subjects: Warm colors (red/orange)

**Set Realistic Targets:**
- Start conservative (5h/week)
- Adjust based on actual time
- Consider subject difficulty
- Account for other commitments

### Maximizing Study Sessions

**Before Starting:**
1. Prepare materials
2. Clear distractions
3. Set specific goal
4. Select subject in StudyMate
5. Start timer

**During Session:**
- Focus on single subject
- Use pause for brief breaks only
- Don't switch subjects mid-session
- Keep StudyMate tab open

**After Session:**
1. Stop and save timer
2. Note what you accomplished
3. Review progress bar
4. Plan next session

### Study Scheduling

**Daily Routine:**
```
Morning (9-11 AM):
- Mathematics: 2 hours

Afternoon (2-4 PM):
- Chemistry: 2 hours

Evening (7-8 PM):
- Review: 1 hour
```

**Weekly Planning:**
1. Monday: Check weekly targets
2. Daily: Track with timer
3. Wednesday: Mid-week progress check
4. Friday: Review week's sessions
5. Sunday: Export to calendar

### Maintaining Motivation

**Use Progress Bars:**
- Watch them fill up
- Satisfying visual feedback
- Clear goal achievement

**Track Streaks:**
- Study daily (note in sessions)
- Build consistency
- Create habits

**Review Statistics:**
- Celebrate milestones
- 10 hours total
- 50 sessions
- 100% target achieved

---

## Troubleshooting

### Timer Issues

**Problem: Timer won't start**

**Solutions:**
- Select a subject first
- Refresh page if frozen
- Check if another timer running

**Problem: Timer resets unexpectedly**

**Causes:**
- Browser refresh
- Closing tab
- Power loss

**Prevention:**
- Keep tab open
- Don't refresh during session
- Use pause instead of closing

### Data Issues

**Problem: Subjects disappeared**

**Likely Cause:** Browser data cleared

**Recovery:**
- No automatic backup
- Re-add subjects
- Use calendar export as backup

**Prevention:**
- Manual backup (see README)
- Don't clear browser data
- Export regularly

**Problem: Sessions not showing**

**Check:**
1. Scroll in sessions list
2. Only shows 10 most recent
3. Timer was stopped (not paused)
4. Browser hasn't cleared data

### Calendar Sync Issues

**Problem: .ics file won't download**

**Solutions:**
- Check browser downloads settings
- Try different browser
- Allow downloads from page

**Problem: Google Calendar won't import**

**Solutions:**
- Verify .ics file downloaded completely
- Try importing to different calendar
- Check file isn't corrupted
- Re-export from StudyMate

**Problem: Duplicate events**

**Cause:** Re-importing same sessions

**Solution:**
- Delete old StudyMate calendar
- Create new one
- Import fresh export

### Display Issues

**Problem: Layout looks broken**

**Solutions:**
- Use modern browser
- Update browser
- Clear browser cache
- Check screen size (responsive design)

**Problem: Colors not showing**

**Solutions:**
- Enable CSS
- Update browser
- Check color picker support

---

## Keyboard Shortcuts

Currently no keyboard shortcuts. Future feature!

---

## Mobile Usage

### Responsive Design

StudyMate works on mobile:
- Single column layout
- Touch-friendly buttons
- Larger tap targets
- Optimized forms

### Mobile Tips

**Timer on Mobile:**
- Keep screen on
- Use browser tab
- Don't switch apps frequently
- Battery considerations

**Best Practices:**
- Add to home screen
- Use in landscape for forms
- Portrait for timer/sessions

---

## Data Management

### Viewing Your Data

**Browser Console Method:**
```javascript
// Open Developer Tools (F12)
// Go to Console tab

// View subjects
console.log(localStorage.getItem('studymate_subjects'));

// View sessions
console.log(localStorage.getItem('studymate_sessions'));
```

### Backing Up Data

**Manual Backup:**
1. Open Developer Tools (F12)
2. Go to Console
3. Run backup script (see README)
4. Copy output
5. Save to text file

**Recommendation:**
- Backup weekly
- Before browser updates
- Before clearing cache

### Clearing Data

**To Start Fresh:**
1. Open Developer Tools
2. Go to Application tab
3. Storage → Local Storage
4. Delete `studymate_subjects`
5. Delete `studymate_sessions`
6. Refresh page

**Warning:** Cannot be undone!

---

## FAQ

**Q: Does StudyMate need internet?**  
A: No! Works completely offline after initial load.

**Q: Where is my data stored?**  
A: In your browser's LocalStorage (client-side only).

**Q: Can I use on multiple devices?**  
A: Currently no sync. Each device is independent.

**Q: How much data can I store?**  
A: LocalStorage limit is 5-10MB. Plenty for years of sessions!

**Q: Can I edit past sessions?**  
A: No, sessions are read-only once saved.

**Q: What if I close the browser during a session?**  
A: Session is lost. Always stop & save before closing.

**Q: Can teachers/parents see my data?**  
A: No, unless you share your device or export calendar.

**Q: Is there a mobile app?**  
A: Web app works on mobile. Native app: future plan.

**Q: Can I track multiple students?**  
A: Each browser profile is separate. Use different profiles.

**Q: How do I change a subject's target?**  
A: Currently: Delete and recreate. Edit feature coming.

---

## Getting Help

**Resources:**
- README.md - Full documentation
- GitHub Issues - Report bugs
- Portfolio contact - Direct support

**Before Asking:**
1. Check this user guide
2. Read troubleshooting section
3. Try refreshing browser
4. Check browser console for errors

---

**Guide Version:** 1.0.0  
**Last Updated:** November 2024  
**Author:** Michael Semera

**Happy studying with StudyMate! 📚**