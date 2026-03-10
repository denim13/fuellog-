# FuelLog PWA — Deploy Guide

Science-based macro tracker for your PPL recomp plan.
Tracks protein, carbs, fat & water across 5 timed meals around your 1am gym session.

---

## 🚀 Deploy to Your Phone in ~10 Minutes

### Step 1 — Make sure Node.js is installed
Download from: https://nodejs.org (LTS version)
Check it works: open Terminal and run `node -v`

---

### Step 2 — Install dependencies

Unzip the `fuellog-pwa` folder, then in Terminal:

```bash
cd fuellog-pwa
npm install
```

---

### Step 3 — Test locally (optional)

```bash
npm run dev
```

Opens at http://localhost:5173
Press Ctrl+C to stop.

---

### Step 4 — Push to GitHub

1. Go to https://github.com → **New repository** → name it `fuellog` → **Public** → **Create**
2. In Terminal (inside fuellog-pwa folder):

```bash
git init
git add .
git commit -m "FuelLog PWA"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/fuellog.git
git push origin main
```

**If push fails**, go to github.com/YOUR_USERNAME/fuellog and click **"uploading an existing file"**,
then drag in everything EXCEPT the `node_modules` folder.

---

### Step 5 — Deploy on Vercel (free)

1. Go to https://vercel.com → sign in with GitHub
2. Click **Add New → Project**
3. Select your `fuellog` repo
4. Click **Deploy** — done in ~30 seconds
5. Your URL: `https://fuellog-abc123.vercel.app`

---

### Step 6 — Install on your phone 📱

**iPhone (Safari only):**
1. Open your Vercel URL in Safari
2. Tap the Share button (box with arrow up)
3. Scroll down → **Add to Home Screen** → **Add**

**Android (Chrome):**
1. Open your Vercel URL in Chrome
2. Tap the three-dot menu → **Install app** or **Add to Home screen**
3. Tap **Add**

The app works offline after first load. All data saved locally on device.

---

## 📋 What's Tracked

| Meal | Time | Protein | Carbs | Fat |
|------|------|---------|-------|-----|
| Breakfast | ~8:00am | 40g | 50g | 15g |
| Lunch | ~1:00pm | 35g | 40g | 15g |
| Dinner | ~7:00pm | 35g | 40g | 15g |
| Pre-Workout | ~11:30pm | 35g | 70g | 10g |
| Post-Workout | ~2:30–3am | 40g | 45g | 5g |
| **Total** | | **185g** | **245g** | **65g** |

---

## 🛠 Customising

All targets and meals live in `src/App.jsx`:
- `TARGETS` — daily kcal, protein, carbs, fat, water goals
- `MEALS` — meal times, per-meal macro targets, fish guide amounts
- `FOOD_DB` — the food database (add your own entries here)

---

## 💾 Data

Stored in `localStorage` under key `liftlog-nutrition-v1`.
Works on one device. For multi-device sync, Supabase free tier is a good next step.

---

Built for gains. 🐟
