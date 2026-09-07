===========================================================
PROJECT: Unified CCTV Integration & Analytics Platform
===========================================================

--- OVERVIEW ---
Statewide CCTV registry & command-center platform: unified multi-
stream video wall (HLS), AI-based ANPR (Automatic Number Plate
Recognition) analytics, watchlist alerting, GIS-based vehicle
journey tracking, camera onboarding, coverage-gap analysis, audit
logs, and a login/security-shield module.

--- ⚠️ IMPORTANT (READ BEFORE UPLOADING) ---
Aa project ma PHP BILKUL NATHI — no /php or /php-backend folder
exists at all. Backend fully Node.js + Express (server.ts) che, JWT
+ bcrypt thi authentication, cors + helmet security. Database pan
real nathi — src/server/mockDb.ts ma mock/in-memory data che. Jo
tara GitHub repo set ma "badhe PHP" jota hoy to aa ek exception che
— tu chahe to ene alag mention kari deje ke "backend: Node.js" instead
of PHP, athva tu mane kahe to hu aana mate ek PHP+MySQL backend pan
banavi aapi shaku.

--- TECH STACK (actual, as-is) ---
Frontend        : React 19 + TypeScript + Vite 6
Styling         : Tailwind CSS 4
Maps            : Leaflet (GIS vehicle tracking)
Charts          : Recharts (analytics/dashboards)
Video           : hls.js (multi-camera live video wall)
Backend         : Node.js + Express (server.ts via `tsx`)
Auth/Security   : JWT (jsonwebtoken) + bcryptjs + helmet + cors
AI              : Google Gemini API (@google/genai) — ANPR/analytics
                  assist features
Data (current)  : Mock/in-memory DB — src/server/mockDb.ts
                  (NO real database connected)

--- FOLDER STRUCTURE ---
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

--- ENV VARIABLES (.env) ---
GEMINI_API_KEY  = your Google Gemini API key
APP_URL         = app's hosted URL
JWT_SECRET      = secret key for signing JWT tokens
SESSION_SECRET  = secret key for session/HMAC

--- SETUP / RUN LOCALLY ---
1. npm install
2. Copy .env.example -> .env and fill GEMINI_API_KEY, JWT_SECRET,
   SESSION_SECRET
3. npm run dev          (starts tsx server.ts)
4. Build for prod: npm run build
5. Start prod build: npm start

--- IF YOU WANT A REAL PHP + MYSQL BACKEND ---
This one needs a full backend rebuild since nothing PHP exists yet:
  1. Design MySQL schema: cameras, users, vehicles/anpr_logs,
     watchlist, alerts, audit_logs tables
  2. Recreate server.ts's Express routes as PHP endpoints (use
     password_hash/password_verify instead of bcryptjs, and PHP
     JWT library or PHP sessions instead of jsonwebtoken)
  3. Point frontend fetch calls to the new PHP API base URL
(Let me know if you want this PHP+MySQL version built out.)

--- SUGGESTED GITHUB REPO NAME ---
unified-cctv-integration-analytics-platform

--- SUGGESTED SHORT DESCRIPTION (repo tagline) ---
Statewide CCTV command-center platform — unified video wall, AI ANPR
detection, watchlist alerts, GIS vehicle tracking & coverage-gap
analysis (React + Node.js/Express).

--- SUGGESTED TOPICS/TAGS ---
react, typescript, vite, tailwindcss, nodejs, express, jwt-auth,
leaflet, gemini-api, cctv, anpr, surveillance, gis

--- .gitignore NOTE ---
node_modules, dist, .env already ignored — good to push as is.
