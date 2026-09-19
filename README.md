School Accounting Office Queue System
A simple, no-backend queueing demo for a school's accounting/cashier office. Students take a number for Enrollment, Tuition Payment, Uniform, or Logo Printing, and staff call the next number from a live queue.
Try it locally
No build step, no dependencies. Just open index.html in a browser.
# clone the repo, then:
open index.html        # macOS
start index.html        # Windows
xdg-open index.html     # Linux
Or run a tiny local server (recommended so localStorage behaves consistently across tabs):
python3 -m http.server 8000
# visit http://localhost:8000
How it works
Join queue tab — a student picks a service and taps "Take a number" to get a ticket, then sees their position and estimated wait.
Staff view tab — shows who's currently being served, a "Call next" button, and the full waiting list with a remove option.
State is stored in the browser's localStorage, so it currently syncs across tabs/windows on the same device, not across different devices. See "Roadmap" below for turning this into a real multi-device system.
Project structure
.
├── index.html   # entire app: markup, styles, and logic in one file
└── README.md
Roadmap / ideas for contributors
Real backend (Node/Express or similar) + database (Postgres or Redis) so the queue is shared across every device, not just one browser
Real-time sync via WebSockets instead of localStorage
Per-window "now serving" so multiple cashiers can each call their own line independently
Priority queuing (e.g. PWD, senior, pregnant applicants)
SMS/push notification when a student is near the front
Receipt/reference number tied to each ticket for reconciliation
Express lane for quick transactions (logo printing, uniform pickup) vs. full tuition payments
Contributing
Fork the repo
Create a branch (git checkout -b feature/your-idea)
Commit your changes
Open a pull request describing what you changed and why
License
Add a license of your choice (MIT is a common pick for small student projects).
