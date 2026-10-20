# ON ROAD — Assistance routière

Company website for On Road, serving Montréal and surrounding areas.

- Phone: 438-882-4400
- Email: info@aronroad.com
- Services: battery boosts, spare tire changes, fuel delivery, and vehicle unlocking. No towing.
- French-first interface with an English switch.
- Scroll-responsive overhead car and road scene, with a reduced-motion fallback.

Developed for Mohamad El-Darsa’s business with AI assistance. This repository is a starting point for ongoing hands-on development and learning.

## Run on your Mac

Open Terminal and run:

```bash
git clone https://github.com/ja3fari/onRoad-Website.git
cd onRoad-Website
python3 -m http.server 8000
```

Open http://localhost:8000 in your browser. Stop the server with Control+C. No npm installation or build step is required.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Page structure, bilingual copy, navigation and request dialog |
| `styles.css` | Brand colors, layout, responsive styles and illustrated car |
| `app.js` | Language switching, request preparation and scroll effects |
| `assets/logo.jpg` | Company logo |

## What currently works

Call links open the visitor’s phone app. Email links open their email app. The request form creates a message which the visitor can copy or open in their SMS app; they must send it themselves. Nothing is automatically submitted to a server or saved in a database.

## Deployment

The current Sites-hosted version is maintained separately at https://onroad-assistance.brightkrill1024.chatgpt.site and is currently owner-private. Pushing to this GitHub repository does not update that deployment automatically. This source can be served by any static web host; use the repository root as the published directory and no build command. Public launch and domain configuration are separate steps.

## Your first contribution

1. Create a branch: `git switch -c add-opening-hours`.
2. Add the confirmed opening hours in French and English in `index.html`.
3. Preview locally and check both languages and a narrow mobile layout.
4. Run `node --check app.js` if Node.js is installed.
5. Commit and push:

```bash
git add index.html
git commit -m "Add business opening hours"
git push -u origin add-opening-hours
```

Open a pull request on GitHub so the change can be reviewed before merging.

## Before public launch

- Confirm business hours and exact service coverage.
- Test phone, email and SMS links on an actual phone.
- Test scrolling, language switching and reduced-motion settings in Safari and Chrome, on desktop and mobile. Browser visual QA has not yet been completed.
- Configure public hosting and an owned domain if desired.

## Future backend

A later version can add server-validated service requests, a database, notifications and an authenticated management screen. No backend is included in this version. Keep API credentials on the server and out of GitHub and frontend code.

## Rights

No open-source license is granted by this repository. Company branding and website assets are retained for the company’s use.
