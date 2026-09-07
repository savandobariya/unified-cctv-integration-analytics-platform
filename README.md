<div align="center">

# 📹 Unified CCTV Integration & Analytics Platform

Statewide CCTV registry & command-center platform — unified multi-stream video wall (HLS), AI-based ANPR (Automatic Number Plate Recognition) analytics, watchlist alerting, GIS-based vehicle journey tracking, camera onboarding, coverage-gap analysis, and audit logs.

</div>

---

## ⚠️ Important Note

This project was generated in **Google AI Studio**. **There is no PHP anywhere in this project** — no `/php` or `/php-backend` folder exists at all. The backend is fully **Node.js + Express** (`server.ts`), with JWT + bcrypt authentication and cors + helmet security.

There's also no live database — `src/server/mockDb.ts` holds mock/in-memory data.

If your repo collection is meant to be "all PHP," this one's the exception — either label it clearly as Node.js-based, or ask if you'd like a PHP+MySQL backend built for it.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React 19 + TypeScript + Vite 6 |
| Styling | Tailwind CSS 4 |
| Maps | Leaflet (GIS vehicle tracking) |
| Charts | Recharts (analytics/dashboards) |
| Video | hls.js (multi-camera live video wall) |
| Backend | Node.js + Express (`server.ts` via `tsx`) |
| Auth / Security | JWT (`jsonwebtoken`) + `bcryptjs` + `helmet` + `cors` |
| AI | Google Gemini API (`@google/genai`) — ANPR/analytics assist |
| Data | Mock/in-memory DB — `src/server/mockDb.ts` (no live database) |

---

## 📁 Folder Structure

```
unified-cctv-platform/
├── index.html
├── package.json
├── vite.config.ts
├── tsconfig.json
├── .env.example
├── server.ts                     # Express server, auth, APIs
└── src/
    ├── main.tsx
    ├── App.tsx
    ├── index.css
    ├── types.ts
    ├── data/
    │   └── videoStreams.ts
    ├── server/
    │   ├── mockDb.ts             # in-memory mock database
    │   └── security.ts           # JWT/bcrypt helpers
    ├── utils/
    │   ├── apiSafe.ts
    │   ├── audio.ts
    │   └── exportReports.ts
    └── components/
        ├── Navbar.tsx / OfficialEmblem.tsx
        ├── LoginPage.tsx / SecurityShieldModal.tsx
        ├── DashboardOverview.tsx
        ├── AnprAnalytics.tsx / GapAnalysis.tsx
        ├── GisMapRegistry.tsx / VehicleTracking.tsx
        ├── WatchlistAlerts.tsx / AuditLogsModal.tsx
        ├── BulkImportModal.tsx / OnboardCameraModal.tsx
        ├── ArchitectureDocs.tsx / UserProfileModal.tsx
        ├── UnifiedVideoWall.tsx / VideoWall.tsx
        └── videowall/
            ├── VideoWallGrid.tsx / CameraTile.tsx
            ├── CameraSidebar.tsx / TopStatusBar.tsx
            ├── BottomTicker.tsx / LiveAlertsPanel.tsx
            ├── AddVideoModal.tsx / VideoManagerModal.tsx
            └── CCTVCanvasScene.ts
```

---

## 🔑 Environment Variables

```env
GEMINI_API_KEY=your_google_gemini_api_key
APP_URL=http://localhost:3000
JWT_SECRET=your_jwt_signing_secret
SESSION_SECRET=your_session_hmac_secret
```

---

## 🚀 Setup / Run Locally

```bash
# 1. Install dependencies
npm install

# 2. Copy env file and fill in GEMINI_API_KEY, JWT_SECRET, SESSION_SECRET
cp .env.example .env

# 3. Start dev server
npm run dev

# 4. Build for production
npm run build

# 5. Start production build
npm start
```

---

## 🔄 Building a Real PHP + MySQL Backend

This one needs a full backend build since nothing PHP exists yet:

1. Design a MySQL schema: `cameras`, `users`, `vehicles`/`anpr_logs`, `watchlist`, `alerts`, `audit_logs` tables
2. Recreate `server.ts`'s Express routes as PHP endpoints (use `password_hash`/`password_verify` instead of bcryptjs, and a PHP JWT library or PHP sessions instead of `jsonwebtoken`)
3. Point frontend fetch calls to the new PHP API base URL

*(Ask if you'd like this PHP+MySQL version built out.)*

---

## 🏷️ Suggested Repo Metadata

**Description:**
> Statewide CCTV command-center platform — unified video wall, AI ANPR detection, watchlist alerts, GIS vehicle tracking & coverage-gap analysis (React + Node.js/Express).

**Topics:**
`react` `typescript` `vite` `tailwindcss` `nodejs` `express` `jwt-auth` `leaflet` `gemini-api` `cctv` `anpr` `surveillance` `gis`
