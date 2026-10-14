# Gridshare

Find a neighbor with power during a blackout.

When the power goes out, some people nearby still have a charging station, a generator or solar with a battery, and others have a phone at 5%. Gridshare puts the people with power on a map. You pick one, book an hour or more, and pay in USDC with Solana Pay. Your payment waits in escrow and goes to the neighbor only after your charge is done. Then you rate each other.

> **Status: MVP prototype.** This repo contains a clickable user-experience prototype. Neighbors, prices, sessions, ratings and transactions are mock data. No wallet connects and no money moves.

## Try it

Open `index.html` in a browser, or visit the GitHub Pages site once it's enabled.

1. On the **Map**, pick a neighbor with power.
2. Choose how many hours you need and tap **Book & pay**.
3. Pay with the Solana Pay QR. The amount is held in escrow.
4. Watch your phone charge, then tap **Finish & release payment**.
5. Rate your neighbor, then check **Sessions** for your history.
6. On **Share power**, switch yourself on to appear on the map.

## Project structure

```
gridshare/
├── index.html          # App markup: phone frame, map, booking, payment, charging and share screens
├── css/
│   └── styles.css      # Styles (dark "blackout night" theme)
├── js/
│   ├── data.js         # Mock data: neighbors with power, past sessions
│   ├── utils.js        # Helpers: navigation, toasts, formatting, payment QR drawing
│   └── app.js          # Map, booking, escrow payment, charging, rating, share mode
└── docs/
    ├── ARCHITECTURE.md # How the prototype works and the planned on-chain design
    └── ROADMAP.md      # What comes after the prototype
```

No build step and no dependencies. The scripts are plain JavaScript loaded in order, so the app also runs straight from the file system.

## Deploy to GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Choose **Deploy from a branch**, select `main` and `/ (root)`, and save.
4. The site appears at `https://<your-username>.github.io/<repo-name>/`.

## License

MIT. See [LICENSE](LICENSE).
