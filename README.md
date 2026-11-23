# Cloud Computing Learning Platform — Ibb University

A bilingual (Arabic/English), responsive, static educational website built with HTML5, CSS3, and vanilla JavaScript. It uses the supplied Ibb University emblem and the supplied student photograph in a closing academic profile section. The layout retains the navy header, vertical course navigation, horizontal topic strip, and focused lesson view.

## Run locally

1. Extract the project folder.
2. Open `index.html` in a modern browser. Core content and navigation do not require a backend or `fetch()`.
3. The site does not require external fonts, APIs, or a backend for its core features. Typography uses local system-font fallbacks, so the interface remains usable offline.

Optional local HTTP server (useful for browser tooling):

```bash
python -m http.server 8000
```

Then open `http://localhost:8000` from the project directory.

## Files

- `index.html` — semantic page shell and header/sidebar.
- `styles.css` — responsive dashboard, light/dark theme, tables, diagrams, and accessibility focus styles.
- `refinements.css` — isolated layout, typography, interaction, and closing-profile refinements.
- `app.js` — bilingual topic content, navigation, glossary, diagrams, references, and persisted preferences.
- `assets/ibb-university-logo.jpg` — supplied university emblem image.
- `assets/student-profile.jpg` — supplied student photograph, optimized without cropping or changing its aspect ratio.
- `assets/reference-interface.png` — supplied interface reference retained from the original project.
- `TEST_REPORT.md` — scope and test status.

## Edit academic identity

Edit the `IDENTITY` object near the top of `app.js` to change the student or supervisor display names in Arabic and English. The university emblem is used as supplied; no separate college logo was provided.

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

## Publish on GitHub Pages

1. Create a GitHub repository for this project.
2. Upload the **contents** of the `cloud-computing-platform` folder, including `index.html`, the CSS/JS files, and `assets/`.
3. Open **Settings → Pages** in the repository.
4. Under Build and deployment, choose **Deploy from a branch**, select the intended branch (usually `main`) and folder (`/ (root)`), then save.
5. Wait for GitHub Pages to publish the site, open the generated URL, and verify the university emblem, closing photo, navigation, language switch, and theme switch.
6. Keep asset paths relative (for example, `assets/student-profile.jpg`) so they work when the site is published under a repository path.

No deployment URL is included because this project has not been published from this workspace.

## Important limits

- Cloud provider service details, names, regional availability, and prices can change; consult linked official documentation before using them in a real deployment.
- The Docker and Terraform snippets are educational examples; this project does not execute them or use cloud credentials.
- Browser `localStorage` stores language, theme, and last selected topic only. It does not store credentials or user research data. If browser storage is disabled, the page still runs but preferences may not persist.
- A separate faculty logo was not provided. The provided university emblem image is used as supplied; its source image includes a white background and is not altered into a fabricated logo.
