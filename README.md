# Cloud Computing Learning Platform — Ibb University

A bilingual (Arabic/English), responsive, static educational website built with HTML5, CSS3, and vanilla JavaScript. It uses the supplied Ibb University emblem image and follows the reference dashboard's navy header, vertical course navigation, horizontal topic strip, and card-based content layout.

## Run locally

1. Extract the project folder.
2. Open `index.html` in a modern browser. Core content and navigation do not require a backend or `fetch()`.
3. An internet connection is used only to load Google Fonts. If offline, the browser falls back to local system fonts.

Optional local HTTP server (useful for browser tooling):

```bash
python -m http.server 8000
```

Then open `http://localhost:8000` from the project directory.

## Files

- `index.html` — semantic page shell and header/sidebar.
- `styles.css` — responsive dashboard, light/dark theme, tables, diagrams, and accessibility focus styles.
- `app.js` — bilingual topic content, navigation, glossary, diagrams, references, and persisted preferences.
- `assets/ibb-university-logo.jpg` — supplied university emblem image.
- `assets/reference-interface.png` — supplied CNN interface image retained as the visual reference.
- `TEST_REPORT.md` — scope and test status.

## Edit academic identity

Edit the `IDENTITY` object near the top of `app.js`. The instructor and student values currently reflect the details supplied with the task; change them if the course requires different values. A college-specific logo was not supplied separately, so the page does not invent one.

## Included learning sections

1. Cloud Computing
2. Infrastructure
3. Virtualization
4. Storage & Databases
5. Cloud Networking
6. Security
7. Docker & Containers
8. Deployments
9. Monitoring & Observability
10. Automation
11. Cloud-Based Research Repository
12. Terraform & IaC
13. Cloud Providers (Azure, Google Cloud, AWS)

The glossary contains bilingual searchable entries, categories, abbreviations, and definitions. The repository section is an architecture proposal only; no real cloud services are connected and no infrastructure is deployed.

## Important limits

- Cloud provider service details, names, regional availability, and prices can change; consult linked official documentation before using them in a real deployment.
- The Docker and Terraform snippets are educational examples; this project does not execute them or use cloud credentials.
- Browser `localStorage` stores language, theme, and last selected topic only. It does not store credentials or user research data.
- A separate faculty logo was not provided. The provided university emblem image is used as supplied; its source image includes a white background and is not altered into a fabricated logo.
