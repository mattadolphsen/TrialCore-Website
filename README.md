# TrialCore Static Website

This folder is ready to upload to a normal static host such as Netlify, Vercel, GitHub Pages, Cloudflare Pages, or a traditional web server.

## File Structure

```text
trialcore-website/
├── index.html
├── platform.html
├── features.html
├── safety-compliance.html
├── resources.html
├── about.html
├── contact.html
├── assets/
│   ├── css/
│   │   └── styles.css
│   └── images/
│       ├── trialcore-logo.svg
│       └── trialcore-dashboard-preview.png
└── README.md
```

## Preview Locally

From the project root, start any simple static server and open `platform.html`.

Examples:

```bash
python3 -m http.server 8000
```

or

```bash
npx serve .
```

## Deploy

Upload the entire project root to your host. The site does not depend on absolute local paths, so it should work from a normal web root without extra configuration.

## How to Edit Text

- Update page copy directly inside each HTML file.
- Shared styling lives in `assets/css/styles.css`.
- Navigation appears in the header of each page.

## How to Replace the Dashboard Image

- Replace `assets/images/trialcore-dashboard-preview.png` with a new PNG or WebP.
- Keep the same filename if you want to avoid changing the HTML.
- If you use a different filename, update the `<img>` tag in `platform.html`.

## Known Limitations

- `contact.html` uses a static mailto-based fallback for demo purposes.
- If you want hosted lead capture, connect the form to a backend or a form service.
- `index.html` is a redirect-style helper page that sends visitors to `platform.html`.

## Notes

- `platform.html` is the main product page.
- `index.html` redirects to `platform.html`.
- `resources.html` contains the Privacy Policy, Terms of Service, and Security & Compliance tabs.
- The dashboard preview is stored as a normal image file in `assets/images/`.
