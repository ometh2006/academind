# 🎓 AcadeMind · Study Dashboard

A beautiful, offline-first Windows desktop app for students to track academic progress, manage subjects, record test scores, and analyse performance — with no cloud, no accounts, just your data.

---

## ✨ Features

| Feature | Details |
|---|---|
| 🏠 Dashboard | KPIs, trend charts, grade doughnut, smart alerts |
| 📚 Subjects | Add subjects with colours + codes; manage tests |
| 📊 Analytics | Per-subject deep dive: consistency, trend, projected grade |
| 📋 History | Searchable/filterable full test log; export CSV |
| ⏳ Countdown | Exam date countdown timer |
| 🌙 / ☀️ Theme | Sleek dark default + light mode toggle |
| 💾 Data | 100% local (localStorage); export/import JSON backups |

---

## 🚀 Getting the Windows App (No coding needed!)

### Step 1 — Upload to GitHub
1. Create a free account at [github.com](https://github.com) if you don't have one.
2. Click **+** → **New repository** → name it `academind` → click **Create repository**.
3. Upload all these files keeping the folder structure:
   ```
   academind/
   ├── index.html
   ├── main.js
   ├── package.json
   ├── assets/
   │   └── icon.ico        ← (optional) your custom icon
   └── .github/
       └── workflows/
           └── build.yml
   ```
   **Easiest way:** Drag all files into the GitHub web interface, then click **Commit changes**.

### Step 2 — Let GitHub build your app
1. In your repo, click the **Actions** tab.
2. You'll see **Build AcadeMind Windows App** — it starts automatically after your first push.
3. Wait ~3–5 minutes for it to finish ✅.

### Step 3 — Download your .exe
1. Click the completed workflow run.
2. Scroll to **Artifacts** at the bottom.
3. Click **AcadeMind-Windows-Installer** to download a ZIP.
4. Extract it — inside you'll find:
   - `AcadeMind Study Dashboard Setup X.X.X.exe` — full installer
   - `AcadeMind Study Dashboard X.X.X.exe` — portable (no install needed)

### Step 4 — Run it!
Double-click the installer or portable exe. Windows may show a SmartScreen warning — click **More info → Run anyway** (this happens because the app isn't signed with a paid certificate).

---

## 🏷 Creating a Release (with a download link)

To get a permanent download link you can share:

1. Go to your repo → **Releases** → **Create a new release**.
2. In the **Tag** field type `v1.0.0` and click **Create new tag**.
3. Click **Publish release**.
4. GitHub Actions will build the app and automatically attach the `.exe` files to the release!

---

## 🖼 Adding a Custom Icon (Optional)

Replace `assets/icon.ico` with your own icon:
- Must be `.ico` format, 256×256px recommended.
- Free converter: [convertio.co](https://convertio.co/png-ico/)

---

## 🔧 Grades Scale

| Grade | Percentage |
|---|---|
| **A** | 75% and above |
| **B** | 65–74% |
| **C** | 55–64% |
| **S** | 35–54% |
| **F** | Below 35% |

---

## 📦 Tech Stack

- **Frontend:** Pure HTML5 / CSS3 / Vanilla JS
- **Charts:** [Chart.js](https://www.chartjs.org/)
- **Desktop shell:** [Electron](https://www.electronjs.org/)
- **Packaging:** [electron-builder](https://www.electron.build/)
- **CI/CD:** GitHub Actions

---

## 🔒 Privacy

All data stays on **your device only** in browser localStorage. Nothing is ever sent to any server.
