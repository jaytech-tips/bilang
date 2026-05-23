# Client Clock — v2 Ideas

Backlog for next iteration. Prioritized roughly top-to-bottom.

## High Priority
- [ ] **Tab title timer** — show `25:00 - Client Clock` or `🔥 Break 5:00` in the browser tab while timer is running, so users on other tabs don't miss time
- [ ] **Notification API + beep** — when timer hits 0 and tab is backgrounded, use `Notification.requestPermission()` + `new Notification()` so users get a system alert. (Browser blocks this unless triggered by user gesture; do it on first timer start.)

## Medium
- [ ] **Earnings rate in Settings** — a default hourly rate that feeds into an "earnings today" stat in the summary. Currently shows hours but not ₱/day earned.
- [ ] **Dark mode toggle** — already mostly supported via CSS variables, just needs a persistent toggle somewhere visible
- [ ] **Keyboard shortcuts** — `P` for pomodoro/free toggle, `Space` for start/pause, `D` for done, `S` for skip break, `Esc` to cancel. Small QoL.

## Low / Polish
- [ ] **Break auto-finish → "Ready" state** — when break timer naturally reaches 0, auto-transition to a "Ready for next work?" state instead of just sitting there
- [ ] **Session duration warning** — if the timer's been running >8 hours without a done, show a toast suggesting to wrap up
- [ ] **GCash QR placeholder** — replace `gcash-qr.jpg` with actual QR when donation page is ready
