# Bilang — Changelog

All notable changes to Bilang (formerly Client Clock), tracked from initial build.

---

## v2.3.0 — May 23, 2026

### Added
- **📄 Invoice Generator** — new "📄" button in header opens an invoice modal. Choose client, date range, and template (Professional). Generates a print-ready invoice in a new tab with: business name, client info, session breakdown, hours, rate, and total amount due. Auto-opens print dialog for Save as PDF
- **🧾 Invoice settings** — Settings modal now has fields for Business Name and Email, used on invoices
- **`fmtDec()` helper** — formats duration as decimal hours (e.g. 2.50h) for invoices

### Changed
- Settings modal layout: Invoice Details section added above presets

---

## v2.2.0 — May 23, 2026

### Fixed
- **Resume duration bug** — `doneTimer()` and `stopTimer()` now add back `ts.elapsed` when timer is running, fixing the bug where resumed sessions only recorded time since resume
- **GCash QR 404** — committed the actual QR image. Support modal now loads it properly

### Changed
- **Edit modal** — Duration and Hourly Rate are now read-only. Only Client, Date, Status, and Notes can be edited. Prevents time cheating
- **Suggestions button** — now shows "💬 Suggestions" text instead of just the icon
- **Tutorial** — after closing, shows a toast: "Got feedback? Click the 💬 Suggestions button!"

---

## v2.1.0 — May 23, 2026

### Changed
- **Rebranded to Bilang** — "bilang" means "count" in Tagalog. Clean, short, speaks to the PH audience
- Page title: `Bilang – Track Your Billable Hours`
- Header: `Bilang — Track your billable hours`
- Tab title now shows `00:00:00 - Bilang` when timer is active
- Export filenames changed to `bilang-export.csv` and `bilang-backup.json`
- All modals and docs updated to reflect new name
- localStorage keys preserved so existing users keep their data

---

## v2.0.0 — May 23, 2026

### Removed
- **Pomodoro timer removed** — app is now Free Timer only. Laser-focused on time tracking for PH freelancers. Archived copy saved at `archive/client-clock-v1.2.0-with-pomodoro.html` for future reference
- Removed mode toggle, pomodoro progress bar, pomodoro info text, skip/extend break buttons
- Removed all pomodoro settings (work duration, break duration, long break, cycles, auto-stop)
- Removed `setMode()`, `skipBreak()`, `extendBreak()`, `getPomodoroDuration()` functions
- Removed ~25% of JS logic and CSS. File size down from 63KB → 47KB

### Changed
- Timer UI simplified: no mode toggle, just client input + rate + start/pause/done/cancel
- Tutorial updated to reflect Free Timer only

---

## v1.2.0 — May 23, 2026

### Added
- **Tab title timer** — browser tab now shows remaining time so you know time left even when minimized
- **Desktop notifications** — requested on first Start click. Fires system `Notification` popups for timer events. Works even when tab is in the background
- **Unfinished session recovery** — if you close the tab mid-session, a yellow banner appears on reload with resume/cancel options
- **Live notes input** — text field appears under the timer for real-time note-taking. Notes are saved on Done/Cancel

### Changed
- `stopTimer()` now reads live notes
- `doneTimer()` now captures notes from live input
- `clearTimer()` hides the notes field

---

## v1.1.0 — May 23, 2026

### Added
- **Status tracking** — sessions have `completed` or `cancelled` status
- **Cancel saves data** — pressing Cancel saves the session as "cancelled" instead of discarding
- **Edit session status** — dropdown in edit modal to toggle between Completed/Cancelled
- **Skip +5m buttons** during breaks

### Changed
- Stats/summary exclude cancelled sessions
- Cancelled sessions appear faded with ✕ badge
- CSV export includes Status column

---

## v1.0.0 — May 23, 2026

### Initial Release (as Client Clock)
- Free Timer and Pomodoro modes
- Client presets with rate, live earnings display
- Timer controls: Start, Pause, Done, Cancel
- Session history with client filter
- Edit/Delete sessions
- Weekly/monthly earnings summary
- Dark mode, CSV/JSON export/import
- GCash donation, feedback form
- Sound alerts, localStorage persistence
- Responsive design
