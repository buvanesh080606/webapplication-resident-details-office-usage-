# 🏢 ResiRoom Pro | Hybrid Cloud PWA

> **Premium, Real-time Room & Resident Management App** 🏠🚀

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Supabase](https://img.shields.io/badge/Backend-Supabase-green)](https://supabase.com/)
[![PWA](https://img.shields.io/badge/PWA-Ready-blue)](https://web.dev/progressive-web-apps/)

ResiRoom Pro is a high-performance web application designed for mobile-first room management. It bridges the gap between simple spreadsheets and complex property management software by providing a sleek, real-time interface that works across any device.

## 🌟 Key Features

- **🔄 Instant Sync**: Every update is broadcast via Supabase Realtime—no refreshing needed.
- **📴 Offline First**: Uses localStorage for instant loads, syncing with the cloud silently in the background.
- **📲 PWA Support**: Installable on iOS, Android, and Desktop with a custom app icon.
- **📊 Universal Data Export**: Export data to Universal Excel format (`.xls`) for 100% compatibility across all devices.
- **🏠 Multi-House Management**: Effortlessly switch between different properties and locations.
- **📅 Visual Booking Grid**: Intuitive monthly view for tracking resident stays.

## 🚀 Deployment (GitHub Pages)

You can host this project for free using **GitHub Pages**:

1. Create a new repository on GitHub.
2. Push these files (`index.html`, `manifest.json`, `sw.js`, `README.md`, `resiroom_icon.png`).
3. Go to **Settings** -> **Pages**.
4. Set the **Source** to the `main` branch and click **Save**.
5. Your app is now live at `https://your-username.github.io/your-repo-name/`.

## 🛠️ Database Setup (Supabase)

To link your project to your own cloud database:

1. **Table Schema**: Create a `resi_data` table.
   ```sql
   id: int8 (Primary Key)
   content: jsonb (Allows NULL)
   created_at: timestamptz (Default: now())
   ```
2. **Initial Row**: Insert one row with `id: 1` and `content: {}`.
3. **Enable Realtime**: Go to **Database** > **Replication** > **Enable for `resi_data`**.
4. **RLS Policy**: Add an "Enable access to all users" policy to allow the app to communicate with the DB.

## 📱 How to Install

### On iOS (iPhone/iPad)
- Open in Safari -> Tap **Share** -> **Add to Home Screen**.

### On Android
- Open in Chrome -> Tap **Menu** -> **Install App**.

## 💻 Technical Implementation
- **UI Framework**: Tailwind CSS (CDN)
- **State Management**: Hybrid (Local + Cloud Sync)
- **Icons**: Lucide JS
- **Export Engine**: SheetJS
- **Realtime Protocol**: Supabase PostgREST + Realtime Engine

---
*Created with ❤️ for premium management.*
