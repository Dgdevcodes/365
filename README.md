# 365 Tools Center

Internal utility dashboard for Juan365 operations team.

---

## Tools

| Tool | Description |
|------|-------------|
| **DL APP** | Download app bonus tracker |
| **QRPH** | QR payment tracker |
| **Telemarketing** | Number verification tracker |
| **Reporting** | Incident/concern reporting |
| **Reports** | Live chat archive reports |
| **Daily Stats** | Per-shift daily statistics |
| **Weekly Stats** | Weekly performance summary |
| **Most Concern** | Top concern categories |

---

## Setup

### 1. Update GAS URLs

Open `365Tools_v6.html` and find the `CONFIG` block near the top of the `<script>` section:

```js
const CONFIG = {
  DLAPP_URL:     "https://script.google.com/macros/s/...",
  QRPH_URL:      "https://script.google.com/macros/s/...",
  TM_URL:        "https://script.google.com/macros/s/...",
  LIVE_DATA_URL: "https://script.google.com/macros/s/..."
};
```

Replace each URL with your deployed Google Apps Script Web App URL.

### 2. Deploy to GitHub Pages

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set Source to **GitHub Actions**
4. Push to `main` — auto-deploys via the included workflow

---

## File Structure

```
├── 365Tools_v6.html        # Main app (single file)
├── manifest.json           # PWA manifest (installable on mobile)
├── 404.html                # Redirect fallback for GitHub Pages
├── .github/
│   └── workflows/
│       └── deploy.yml      # Auto-deploy on push to main
└── README.md
```

---

## Mobile Install (PWA)

Open the deployed GitHub Pages URL on your phone browser → tap **Add to Home Screen**. Runs as a full-screen app, no browser bar.

---

## Version History

| Version | Notes |
|---------|-------|
| v6.1 | GitHub Pages setup, PWA support, config block, version badge |
| v6.0 | Ultra-premium SaaS redesign (Linear/Stripe/Apple Vision Pro inspired) |
