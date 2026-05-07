# QuizLive Attendee Phone

QuizLive is a static, Firebase-powered live quiz app for events, classrooms, and team sessions. It includes an attendee phone view, an admin control panel, and a host display with QR-code joining, live questions, scoring, leaderboards, and final results.

## Project Structure

```text
.
├── index.html          # Attendee phone interface
├── admin-panel.html    # Host/admin control panel
├── host-display.html   # Public room display and leaderboard
└── js/
    ├── index.js
    ├── admin-panel.js
    └── host-display.js
```

The app has no build step. Firebase, QRCode.js, and fonts are loaded from CDNs.

## Run Locally

From the repository root:

```bash
python3 -m http.server 8000
```

Open these pages in your browser:

- `http://localhost:8000/admin-panel.html`
- `http://localhost:8000/index.html`
- `http://localhost:8000/host-display.html`

You can use demo mode without Firebase, or connect a Firebase Realtime Database for live multi-device play.

## Firebase Setup

1. Create a Firebase project.
2. Enable Realtime Database.
3. Copy your Firebase API key and project ID.
4. Open `admin-panel.html` or `host-display.html`.
5. Enter the Firebase values and room code.
6. Share the generated join link or QR code with attendees.

Do not commit private credentials. Keep local secrets out of the repository.

## Host on GitHub Pages

1. Push this repository to GitHub.
2. Go to repository **Settings**.
3. Open **Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose the `main` branch and `/ (root)` folder.
6. Save the settings.

After GitHub publishes the site, open:

```text
https://YOUR_USERNAME.github.io/YOUR_REPOSITORY_NAME/
```

Main pages:

- Attendee page: `/index.html`
- Admin panel: `/admin-panel.html`
- Host display: `/host-display.html`

If you use QR links, make sure the base join URL points to your GitHub Pages URL.

## Usage Flow

1. Open the admin panel and connect Firebase or start demo mode.
2. Add or confirm quiz questions.
3. Share the attendee join link.
4. Start the quiz and advance through questions.
5. Review leaderboard and final results.

## Notes

- A modern browser is required.
- Live play requires internet access for Firebase and CDN scripts.
- For best results, test the full flow on at least one host screen and one attendee phone before an event.
