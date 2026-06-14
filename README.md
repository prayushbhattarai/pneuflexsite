# PneuFlex Mobile Redesign

This redesign keeps your ESP32/backend behavior, but changes the app UI.

## What changed

- Patient app is mobile-first.
- Solid dark blue background.
- No gradients.
- No top tabs in the patient app.
- Bottom navigation bar with:
  - Dashboard
  - Goals
  - Past Sessions
  - Settings
- Bluetooth button in the top-left opens the IP connect menu.
- Therapist dashboard is only available at:

```txt
http://localhost:5173/therapist
```

## Run

Backend:

```bash
cd server
npm install
npm start
```

Client:

```bash
cd client
npm install
npm run dev
```

Patient app:

```txt
http://localhost:5173
```

Therapist dashboard:

```txt
http://localhost:5173/therapist
```

No firmware re-upload is required if your current V2 firmware already supports `/status`, `/start`, `/stop`, `/emergency`, `/resetEmergency`, `/setSettings`, and `/calibrate`.


## This build

- Patient view widened for iPad display.
- Therapist route expanded into a clinical dashboard with patient profile, adherence, ROM metrics, safety alerts, notes, export, and report section.
