# Care Board

A single-file web app for keeping track of chemotherapy — where you are in the
cycle, how the days are going, questions for the next appointment, and the pile
of paperwork that comes with treatment.

Built for one person going through it. Shared in case it's useful to someone else.

## What it does

**Today** — opens with what day of which cycle it is, drawn as a strip of the
whole cycle with the low-count stretch shaded. Chemo is disorienting; knowing
"day 6 of 21" orients you fast.

**When to call** — a red button on every screen. Logging a temperature at or
above 100.4°F (38°C) triggers a prompt to call now rather than wait for morning.

**Log** — tap-level symptom tracking and a free-text note. No streaks, no scores,
no guilt for skipped days. Prints a one-page summary for an appointment.

**Questions** — a running list for the next visit, with room to write down the
answer afterward.

**Papers** — photos and PDFs, tagged and searchable, with zoom and a contrast
toggle for badly scanned documents.

**Plan** — treatment schedule, phone numbers, appointments, and an editable
medication list that surfaces the right items on the right cycle day.

## Privacy

There is no server, no account, and no analytics. Everything entered stays in
the browser's storage on that device and is never transmitted anywhere.

Because of that, **clearing browser data deletes everything**. Use the backup
button regularly and keep the file somewhere safe. Backup files contain
everything including stored documents — treat them like medical records,
because that's what they are.

## Setup

1. Put `index.html` and `sw.js` in a repo and enable GitHub Pages, or host them
   anywhere that serves static files over https.
2. Open the URL on a phone and use Add to Home Screen. It runs fullscreen with
   its own icon and works offline.
3. Open Plan and fill in the treatment details.

Storage is tied to the web address, so use one stable URL.

### Filing documents quickly

Files named like `2026-07-17 Pathology Consult Report [Pathology].pdf` sort and
categorize themselves on upload — leading ISO date sets the date, the bracketed
tag sets the category. Anything else lands in a "Needs filing" queue for naming
and tagging in place.

### Editing

After changing `index.html`, bump `CACHE_VERSION` in `sw.js` or devices will keep
serving the cached copy.

## Not medical advice

The cycle phases and symptom timing are general patterns, not predictions. The
care team's instructions always take priority over anything shown here.
