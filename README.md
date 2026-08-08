# 🏢 ResiRoom Pro | Hybrid Cloud PWA

> **Premium, Real-time Room & Resident Management App** 🏠🚀

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Supabase](https://img.shields.io/badge/Backend-Supabase%20%2F%20Local-green)](https://supabase.com/)
[![PWA](https://img.shields.io/badge/PWA-Ready-blue)](https://web.dev/progressive-web-apps/)

ResiRoom Pro is a high-performance web application designed for mobile-first room management. It bridges the gap between simple spreadsheets and complex property management software by providing a sleek, real-time interface that works across any device with resilient local + cloud sync.

## 🌟 Key Features

- **🔄 Instant Sync**: Real-time cloud sync with Supabase (plus fallback mode).
- **📴 Local-First Resilience**: Works 100% offline with zero data loss using browser memory.
- **⚙️ In-App Database Settings UI**: Update Supabase credentials, switch storage provider, or run SQL setup directly from the UI.
- **🛡️ Data Backup & Restore**: 1-click JSON backup export & restore to guarantee your booking data is never erased.
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

## 🛠️ Database Setup (Supabase / Free Tier)

To link your project to your cloud database or recover a paused project:

1. **Table Schema**: Create a `resi_data` table in your Supabase SQL Editor:
   ```sql
   CREATE TABLE IF NOT EXISTS public.resi_data (
     id int8 PRIMARY KEY,
     content jsonb,
     created_at timestamptz DEFAULT now()
   );
   ALTER TABLE public.resi_data ENABLE ROW LEVEL SECURITY;
   CREATE POLICY "Allow All" ON public.resi_data FOR ALL USING (true) WITH CHECK (true);
   ```
2. **Connect via UI**: Click **Database Settings** inside the app top bar and enter your **Project URL** & **Anon Key**.

## 📱 How to Install

### On iOS (iPhone/iPad)
- Open in Safari -> Tap **Share** -> **Add to Home Screen**.

### On Android
- Open in Chrome -> Tap **Menu** -> **Install App**.

## 💻 Technical Implementation
- **UI Framework**: Tailwind CSS (CDN)
- **State Management**: Hybrid (Local-First + Cloud Sync)
- **Icons**: Lucide JS
- **Export Engine**: SheetJS
- **Realtime Protocol**: Supabase PostgREST + Realtime Engine


---
*Created with ❤️ for premium management.*
