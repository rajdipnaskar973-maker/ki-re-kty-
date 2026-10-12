<<<<<<< HEAD
# Durga Pujo Bole Kotha — দুর্গা পুজো বলে কথা

> A mobile-first, authentic Durga Puja pandal discovery and optimal road-route planning web application for Kolkata and beyond.

---

## 🌟 Overview & Key Features

- **Festive Aesthetic**: Deep vermilion red (`#B3261E`), gold (`#D9A441`), cream (`#FFF6E5`), and maroon (`#6E1510`), inspired by traditional Bengali Durga Puja artistry, alpona motifs, and conch shells.
- **Pandal Dataset**: 122 curated pandals across North, South, and Central Kolkata (`public/kolkata_puja_pandals_starter_dataset.json`).
- **Free OpenStreetMap Geocoding**: Real-time autocomplete suggestions via Photon Komoot (biased to Kolkata coordinates `lat: 22.5726, lon: 88.3639`).
- **Real Road Routing & Matrices**: Powered by OSRM demo server and OpenRouteService, returning genuine driving, walking, and transit navigation.
- **Exact & Heuristic Optimization (1 to 30 stops)**:
  - **1 to 12 stops**: Exact **Held-Karp** Dynamic Programming with bitmasks ($O(n^2 \cdot 2^n)$) guaranteeing the shortest Hamiltonian path.
  - **13 to 30 stops**: **Nearest-Neighbour initial solution** improved with iterative **2-opt** (segment reversal) and **Or-opt** (chain relocations).
  - Fixed starting point and final destination.
- **Walking Threshold (1.5 km default)**: Legs under threshold offer walking; longer legs suggest driving/cab and transit links.
- **Visiting Workflow**: Mark stops as visited, skip stops, advance to next stop, or recalculate on the go.
- **Saved Plans**: Save multiple itineraries with custom names in browser `localStorage`.
- **Serverless API Proxying**: Ready for Vercel deployment under `/api` to securely hold private keys server-side.

---

## 🚀 Quick Setup Guide

### 1. Requirements
- Node.js 18+ (tested on Node 20+)
- npm or pnpm

### 2. Installation
```bash
git clone <repo-url>
cd "Durga Puja Bole Kotha"
npm install
```

### 3. Running in Development
```bash
npm run dev
```
Open `http://localhost:5173` in your browser.

### 4. Running Tests
```bash
npm test
```

### 5. Production Build
```bash
npm run build
npm run preview
```

---

## 🔑 External API Keys (Optional)

The application works out of the box with zero required API keys using the public OpenStreetMap Photon geocoder and OSRM demo servers.

For higher rate limits in production deployments:
1. **OpenRouteService**: Get a free API key at [openrouteservice.org/dev/#/signup](https://openrouteservice.org/dev/#/signup).
   - In Vercel, set the environment variable `ORS_API_KEY` in Project Settings > Environment Variables.
2. **MapTiler** (optional vector tiles): Get a free key at [cloud.maptiler.com/account/keys/](https://cloud.maptiler.com/account/keys/).

---

## 📱 Mobile Experience (390px Viewport)

Designed strictly for mobile screens (e.g. iPhone / Android standard viewports):
- Touch targets $\ge 48\text{ px}$.
- Sticky bottom action bar.
- Zero horizontal overflow.
- Accessible WCAG AA contrast.
- PWA installable manifest on Android.

---

## 🏛️ Dataset Verification Status

- Total Curated Pandals: 122
  - North Kolkata: 73
  - South Kolkata: 42
  - Central Kolkata: 7
- Coordinates: Stored as `null` initially in starter dataset, looked up via Photon geocoder on demand, and stored in browser `localStorage` upon user confirmation.
=======
# ki-re-kty-
>>>>>>> eaebe76061485757cd41f9f800b21c21e6bc33df
