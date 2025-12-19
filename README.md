Simple School Management (SPA)

Overview
- A minimal single-page application to manage Students and Classes.
- Data stored locally in the browser using LocalStorage (no backend required) by default.

How to run (frontend)
1. Open `index.html` in your browser (double-click or open with the browser).
2. Use the `Students` and `Classes` tabs to add, edit, and delete records.

Server (optional)
You can run an optional backend that provides persistent storage, authentication, and CSV import/export.

Run server
1. cd server
2. npm install
3. npm start

Defaults:
- Server runs on port 3000
- Seed admin user: username `admin`, password `admin`

Syncing
- Use the login inputs in the header to authenticate with the server (`admin`/`admin` by default).
- `Push` will create/update classes and students on the server from local storage.
- `Pull` will replace local storage with server data.
- `Export CSV` downloads local students as CSV.
- `Import CSV` imports a CSV file into local storage (columns: name,age,class).

Files
- `index.html` — the entire app (HTML/CSS/JS).
- `server/` — Node/Express server with SQLite persistence and CSV endpoints.

Next steps you might want
- Improve merge logic when pushing to server to avoid duplicates.
- Add role-based auth and web UI for multiple users.

Notes
- The frontend seeds a couple of classes and students on first load.
- To reset data, clear site data / localStorage for this page in your browser.
