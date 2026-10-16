# College Event Management System

**Live demo:** https://2500080234.github.io/events/

A lightweight front-end web application for managing college events. Students can browse and register for events, and organisers can create events and review registrations.

Built with plain HTML, CSS and JavaScript. There is no build step and no dependencies.

## Features

**Student portal (user.html)**
- Browse upcoming events as ticket-style cards
- Search by title or venue and filter by category
- Register with name, roll number and college email
- Live seat counts, duplicate-registration check and full-event handling

**Admin dashboard (admin.html)**
- Summary stats: events, registrations and open seats
- Add new events (title, date, venue, category, seats, description)
- View the registrant list for each event
- Delete events together with their registrations

**Home page (index.html)**
- Highlights the next upcoming event with a day countdown
- Lists upcoming events and links to both portals

## Project structure

    events/
    |-- index.html   (landing page)
    |-- user.html    (student portal)
    |-- admin.html   (admin dashboard)
    |-- README.md

## Getting started

1. Clone the repository:

        git clone https://github.com/2500080234/events.git
        cd events

2. Open index.html in Chrome or Edge, or serve the folder locally:
   - VS Code: use the Live Server extension
   - Node.js: npx serve . then visit http://localhost:3000
   - Python: python -m http.server 8000 then visit http://localhost:8000

## How data is stored

Data is kept in the browser's localStorage under the cems. prefix (cems.events, cems.regs). The three pages share it, so an event added in admin.html appears in user.html and index.html immediately.

To reset the demo data, run this in the browser console:

    localStorage.clear(); location.reload();

## Limitations

- No backend or authentication. Data exists only in one browser, and admin.html is open to anyone.
- On the live demo, events added by an admin are not visible to other visitors.
- Not suitable for production use as is.

## Roadmap

- [ ] Backend API and database
- [ ] Admin login and role-based access
- [ ] Edit existing events
- [ ] Export registrations to CSV
- [ ] Email confirmation after registration

## Contributing

1. Create a branch: git checkout -b feature/short-name
2. Commit your changes: git commit -m "feat: describe change"
3. Push the branch: git push -u origin feature/short-name
4. Open a pull request into main

Commit messages follow the Conventional Commits style (feat:, fix:, docs:).
