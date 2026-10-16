 College Event Management System

A lightweight front-end web application for managing college events. Students can browse and register for events, and organisers can create events and review registrations.

Built with plain HTML, CSS and JavaScript. There is no build step and no dependencies.

Features

Student portal (user.html)

Browse upcoming events as ticket-style cards
Search by title or venue and filter by category
Register with name, roll number and college email
Live seat counts, duplicate-registration check and full-event handling

Admin dashboard (admin.html)

Summary stats: events, registrations and open seats
Add new events (title, date, venue, category, seats, description)
View the registrant list for each event
Delete events together with their registrations

Home page (index.html)

Highlights the next upcoming event with a day countdown
Lists upcoming events and links to both portals
Project structure
college-event-management/
├── index.html   # Landing page
├── user.html    # Student portal
├── admin.html   # Admin dashboard
└── README.md
Getting started
Clone the repository:
bash
   git clone https://github.com/<your-username>/college-event-management.git
   cd college-event-management
Open index.html in any modern browser. Alternatively, serve the folder locally:
bash
   python3 -m http.server 8000
   # then visit http://localhost:8000
How data is stored

Data is kept in the browser's localStorage under the cems. prefix (cems.events, cems.regs). The three pages share it, so an event added in admin.html appears in user.html and index.html immediately.

To reset the demo data, run this in the browser console:

js
localStorage.clear(); location.reload();
Limitations
No backend or authentication. Data exists only in one browser, and admin.html is open to anyone.
Not suitable for production use as is.
Roadmap
 Backend API and database (Node.js / Express, or Django)
 Admin login and role-based access
 Edit existing events
 Export registrations to CSV
 Email confirmation after registration
