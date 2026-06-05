# TrashTrack Rwanda

**Smart waste collection for households, drivers, and collection companies in Kigali.**

TrashTrack Rwanda is an interactive **HTML prototype** for a waste-management platform: bilingual marketing site (English / Ikinyarwanda), a multi-role web app, company pricing, GIS maps, household registration with QR contracts, and MoMo auto-payment flows.

> This repository is a **front-end prototype** for demonstration and coursework. There is no backend, database, or real payment integration.

---

## Live demo (GitHub Pages)

After you enable Pages, your site will be available at:

```text
https://YOUR_GITHUB_USERNAME.github.io/REPO_NAME/
```

| Page | URL |
|------|-----|
| Landing site | `/` → `index.html` |
| Platform app | `/trashtrack_prototype.html` |

Replace `YOUR_GITHUB_USERNAME` and `REPO_NAME` with your GitHub account and repository name.

---

## Features

### Marketing site (`index.html`)
- Home, About, Services, Pricing, Contact
- English & Ikinyarwanda language toggle
- Company plan pricing with **SMS billed on each client’s monthly bill** ($0.02 / 26 RWF per SMS)

### Platform app (`trashtrack_prototype.html`)

| Role | Highlights |
|------|------------|
| **Client** (household or business) | SMS notifications, service contract & QR, auto-payment SMS log, complaints (USSD `*284*77#` + portal) |
| **Driver** | GIS route map (green / red / yellow collection status), QR scan for paid/unpaid, stops, collection status |
| **Admin** (collection company) | Dashboard, payments, SMS centre, routes, schedules, **registration** (contract + unique QR), **GIS audit map**, household registry, complaints, reports, MoMo sync |

**Admin staff roles at login:** CEO & Founder, COO, Human Resources, Finance, Chief Auditor, IT (Super Admin).

**Maps:** [Leaflet](https://leafletjs.com/) + [OpenStreetMap](https://www.openstreetmap.org/) (free GIS).

---

## Project structure

```text
Trashtrack_protoype/
├── index.html                 # Public marketing website
├── trashtrack_prototype.html  # Full app prototype (login + portals)
├── assets/
│   ├── logo.png
│   ├── hero-collection.jpg
│   ├── about-community.jpg
│   └── driver-operations.jpg
└── README.md
```

Optional local files (not required for the live demo): business plan PDF, extra images.

---

## Run locally

No build step or Node.js required.

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_GITHUB_USERNAME/REPO_NAME.git
   cd REPO_NAME
   ```
2. Open `index.html` in a browser, or use a simple local server:
   ```bash
   # Python 3
   python -m http.server 8080
   ```
3. Visit `http://localhost:8080` and click **Login** or open `trashtrack_prototype.html`.

**Demo login:** choose portal and role on the login screen — no password in this prototype.

---

## Deploy on GitHub Pages (free)

1. Push this folder to a GitHub repository (see `.gitignore` for suggested exclusions).
2. On GitHub: **Settings → Pages**.
3. **Build and deployment → Source:** Deploy from a branch.
4. **Branch:** `main` (or `master`) · **Folder:** `/ (root)`.
5. Save. Wait 1–2 minutes, then open the Pages URL shown in settings.

**Tip:** Keep `index.html` at the repository root so the landing page loads at `/`.

---

## Tech stack

| Layer | Tools |
|-------|--------|
| Markup & style | HTML5, CSS3 |
| Icons | [Bootstrap Icons](https://icons.getbootstrap.com/) |
| Fonts | Inter, Plus Jakarta Sans (Google Fonts) |
| Maps | Leaflet 1.9 + OpenStreetMap tiles |
| Charts (admin) | Chart.js |
| QR preview (demo) | QR Server API |

---

## Pricing model (prototype)

- **Collection companies** pay a monthly platform fee (Starter / Professional / Enterprise).
- **SMS** is charged **per message on each household’s bill** (not as a separate household platform fee in the pricing UI).
- Households use the client portal for contract, notifications, auto-pay messages, and complaints — billing is via their collector.

---

## Authors & context

Prototype developed for waste-collection operations in **Kigali, Rwanda**, aligned with the TrashTrack Rwanda business concept (household SMS reach, company dashboards, driver routes, MoMo, and transparency).

**Institution:** Glasgow Caledonian University (project / dissertation prototype).

---

## License

This project is provided for **educational and demonstration purposes**. Add a license file (e.g. MIT) if you plan to open-source it formally.

---

## Contact

- **Email:** hello@trashtrack.rw *(demo)*
- **Location:** Kigali, Rwanda

For issues or feedback on the prototype, open a GitHub **Issue** on this repository.
