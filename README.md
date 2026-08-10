<div align="center">

<img src="./logo.png" alt="AMU Batch X Logo" width="140" style="border-radius: 28px;" />

# 🎓 AMU BATCH X

### The Official Student Academic Companion Application
**Department of Computer Science · Aligarh Muslim University (AMU)**  
*Engineered for MCA Batch 2026–2028*

<br/>

[![Official Website](https://img.shields.io/badge/Official%20Website-amubatchx.app-166534?style=for-the-badge&logo=googlechrome&logoColor=white)](https://www.amubatchx.app)
[![Download Portal](https://img.shields.io/badge/Download%20Only%20From-amubatchx.app-22c55e?style=for-the-badge&logo=android&logoColor=white)](https://www.amubatchx.app)

<br/>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Android%208.0%2B-3DDC84?style=flat-square&logo=android&logoColor=white" alt="Platform Android 8.0+" />
  <img src="https://img.shields.io/badge/Frontend-React%2019%20%7C%20Vite%208-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React 19 Vite 8" />
  <img src="https://img.shields.io/badge/Language-TypeScript%205.7-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Styling-Tailwind%20CSS%20v4-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white" alt="Tailwind CSS v4" />
  <img src="https://img.shields.io/badge/Runtime-Capacitor%207-119EFF?style=flat-square&logo=capacitor&logoColor=white" alt="Capacitor 7" />
  <img src="https://img.shields.io/badge/Database-Supabase%20PostgreSQL-3ECF8E?style=flat-square&logo=supabase&logoColor=white" alt="Supabase" />
  <img src="https://img.shields.io/badge/Cloud%20Messaging-Firebase%20FCM-FFCA28?style=flat-square&logo=firebase&logoColor=black" alt="Firebase FCM" />
  <img src="https://img.shields.io/badge/Architecture-Offline%20First-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="Offline First" />
  <img src="https://img.shields.io/badge/Status-Active%20Production-success?style=flat-square" alt="Status Active" />
</p>

</div>

---

## ⚠️ Important Distribution Notice: No Direct Downloads

> ### 🔒 Official Download Policy
> **There are NO direct APK downloads, binary releases, or file mirrors hosted on GitHub or third-party repositories.**  
> 
> To safeguard student devices, prevent unauthorized APK tampering, maintain cryptographic signature integrity, and guarantee automated in-app update delivery, **Batch X must be downloaded exclusively from the official verified web portal:**
> 
> 👉 **[https://www.amubatchx.app/](https://www.amubatchx.app/)**
> 
> *Do not install builds from untrusted third-party mirrors or unverified links.*

---

## 📖 About AMU BATCH X

**AMU BATCH X** is a specialized, production-grade digital academic companion engineered for postgraduate scholars in the **Department of Computer Science at Aligarh Muslim University (AMU)**, tailored specifically for the **MCA Batch (2026–2028)**.

The platform eliminates everyday academic uncertainty on campus by:
- Enforcing AMU's mandatory **75% minimum attendance rule** with real-time safe bunker margin calculations.
- Displaying real-time, room-mapped lecture timetables (**CS-01, CS-02, CS-03, CS-04, Systems Labs, and Unix Lab 2**).
- Providing peer-verified crowd updates for schedule delays, cancellations, and classroom reallocations.
- Broadcasting official departmental notices, examination schedules, and circulars within 5 seconds.
- Hosting an offline-accessible repository of lecture notes, lab assignments, and Previous Year Questions (PYQs).

---

## 🌟 Core Features & Modules

### 1. 📊 Smart Attendance Ledger & 75% AMU Rule Engine
- **AMU 75% Compliance Calculator**: Instantly informs students how many lectures they can safely miss without falling below the 75% examination eligibility cutoff, or how many consecutive classes they must attend to restore eligibility.
- **Categorized Tracking**: Independent tracking ledgers for Theory lectures and Practical Laboratory sessions.
- **Persistent Local Records**: Quick attendance tallying preserved in offline cache with cloud synchronization.

### 2. 📅 Room-Mapped Dynamic Timetable
- **Real-Time Lecture Resolution**: Automatically identifies the active lecture, remaining time, next upcoming class, and teacher details.
- **Classroom Mapping**: Precise venue indicators across department halls: **CS-01, CS-02, CS-03, CS-04, Systems Lab 1, and Unix Lab 2**.
- **Academic Calendar Integration**: Seamless handling of university holidays, examination recesses, and adjusted weekend timetables.

### 3. 👥 Crowdsourced Class Rescheduling & Peer Verification
- **Community Alert Submissions**: Students can report sudden class delays, faculty leaves, or room relocations.
- **Upvote / Downvote Verification**: Reports require community validation before altering the live schedule status, preventing false information.
- **Moderator Controls**: Administrative oversight for verifying and locking schedules.

### 4. 🔔 Sub-5-Second Circulars & Pre-Lecture Chimes
- **Instant Department Circulars**: High-priority push notifications dispatched via **Firebase Cloud Messaging (FCM)** for exam timetables, semester registrations, and urgent notices.
- **5-Minute Pre-Class Local Alarms**: Intelligent background chimes alert students 5 minutes before their next class commences, even in silent or battery-saver modes.

### 5. 📚 Academic Vault (Notes, Assignments & PYQs)
- **Coursework Vault**: Structured repository of lecture notes, lab manuals, and syllabus breakdowns organized semester-wise.
- **Previous Year Question Papers (PYQs)**: Comprehensive archives of Mid-Semester, End-Semester, and Internal examination papers.
- **Offline Storage**: Downloaded academic PDFs remain fully accessible when network access is unavailable.

### 6. 🌐 Zero-Latency Offline-First Architecture
- Full offline operational capability: Schedules, course materials, and personal records load instantaneously without active network connectivity.
- Background differential synchronization updates data cleanly once campus Wi-Fi or cellular connections reconnect.

### 7. 🔄 Native In-App Auto-Updater
- Integrated native package updater: Checks Supabase version manifests on launch and securely streams update packages.
- Android `FileProvider` package verification enables frictionless in-place application upgrades without manual file management.

---

## 🛠️ Complete Technical Architecture

AMU BATCH X is built on an enterprise hybrid mobile stack combining reactive web primitives with native Android system APIs.

```
┌─────────────────────────────────────────────────────────────┐
│                 AMU BATCH X Architecture                    │
└─────────────────────────────────────────────────────────────┘
                              │
         ┌────────────────────┴────────────────────┐
         ▼                                         ▼
┌─────────────────────────────┐       ┌─────────────────────────────┐
│    Mobile Companion App     │       │    Official Web Platform    │
│  React 19 + Vite 8 + Cap 7  │       │  Next.js 16 + Turbopack     │
│   Tailwind CSS v4 + Java    │       │     amubatchx.app           │
└──────────────┬──────────────┘       └──────────────┬──────────────┘
               │                                     │
               └──────────────────┬──────────────────┘
                                  ▼
               ┌─────────────────────────────────────┐
               │         Cloud Infrastructure        │
               │   Supabase (PostgreSQL 15+ & RLS)   │
               │   Firebase Cloud Messaging (FCM)    │
               │   Object Storage CDN (Release Hub)  │
               └─────────────────────────────────────┘
```

### Layer-by-Layer Tech Stack Breakdown

| Architectural Layer | Technologies | Purpose & Implementation Details |
| :--- | :--- | :--- |
| **Client Core / UI** | **React 19**, **TypeScript 5.7**, **Vite 8** | Ultra-responsive component hierarchy, strict typing, sub-millisecond hot-module reloading |
| **Styling & Design System** | **Tailwind CSS v4**, **Lucide React** | Modern OLED dark and light modes, CSS theme tokens, glassmorphic card primitives, fluid micro-animations |
| **Hybrid Native Bridge** | **Capacitor 7** | Native Android integration via `@capacitor/android`, `@capacitor/app`, `@capacitor/filesystem`, `@capacitor/preferences` |
| **Native Custom Plugin** | **Android Java (`AppUpdateInstallerPlugin`)** | Custom Java bridge handling APK download verification, `FileProvider` URI generation, and native `ACTION_VIEW` package installation |
| **Backend & Database** | **Supabase (PostgreSQL 15+)** | Cloud database with Row-Level Security (RLS) policies, Realtime WebSocket change streams, and relational data integrity |
| **Cloud Storage** | **Supabase Object Storage** | CDN-backed storage buckets for department notices, course syllabi, lecture notes, and version release artifacts |
| **Push & Local Alerts** | **Firebase FCM & Local Notifications** | Multi-channel cloud broadcast push engine coupled with 5-minute pre-class local hardware chimes (`notification.wav`) |
| **Security & Auth** | **bcryptjs** & Custom Signature Auth | Secure PIN hashing, student whitelist verification (enrollment/roll number mapping), and tamper detection |
| **Web Distribution Portal** | **Next.js 16**, **Vercel Edge Network** | High-performance official web hub hosted at [amubatchx.app](https://www.amubatchx.app) |

---

## 📱 Installation & Setup Guide

### Getting the App
1. **Visit the Official Portal**:  
   Open your browser and navigate to **[https://www.amubatchx.app/](https://www.amubatchx.app/)**.
2. **Download the Verified Package**:  
   Follow the download link on the official portal to fetch the verified APK.
3. **Android Security Setting**:  
   If prompted, navigate to **Settings → Security** (or tap the browser prompt) and enable **"Allow installation from this source"**.
4. **Install & Launch**:  
   Open the APK, tap **Install**, and launch **AMU BATCH X**.
5. **Student Authentication**:  
   Enter your university enrollment number and roll number to initialize your personal timetable, attendance ledger, and class group.

---

## 📋 System Requirements

| Parameter | Minimum Specification | Recommended |
| :--- | :--- | :--- |
| **Operating System** | Android 8.0 (Oreo / API Level 26) | Android 12.0+ (API Level 31+) |
| **Architecture** | Universal (arm64-v8a, armeabi-v7a, x86_64) | arm64-v8a |
| **Network** | Offline supported; periodic sync required | 4G / 5G / Campus Wi-Fi |
| **Storage Space** | ~25 MB base installation | 50 MB+ (for cached notes & PYQs) |
| **Permissions** | Notification access (for class chimes) | Storage (for PDF vault downloads) |

---

## 👥 Engineering & Collaboration

The **AMU BATCH X** ecosystem is developed and maintained collaboratively by student software engineers from the Department of Computer Science, Aligarh Muslim University:

- **Sameer Ahmad** — *Lead Mobile Architect & Full-Stack Engineer*  
  GitHub: [@sameerahmad005](https://github.com/sameerahmad005) · [@sameerahmadansaribackup](https://github.com/sameerahmadansaribackup)  
  Portfolio: [sameerahmadansari.me](https://sameerahmadansari.me) · LinkedIn: [sameer-abrar](https://linkedin.com/in/sameer-abrar)

- **Ali Saqulain** — *Web Platform Engineering & Core Collaborator*  
  GitHub: [@Alisaqulain](https://github.com/Alisaqulain) · LinkedIn: [ali-saqulain](https://www.linkedin.com/in/ali-saqulain-7404a8287)

- **Okash** — *Student Engineering Contributor*

### Official Links
- 🌐 **Official Web Portal**: [https://www.amubatchx.app/](https://www.amubatchx.app/)
- 📱 **Official Documentation Portal**: [https://github.com/sameerahmadansaribackup/batch-x](https://github.com/sameerahmadansaribackup/batch-x)

---

## 📜 Disclaimer

**AMU BATCH X** is an independent student academic companion application built by and for the student community of the Department of Computer Science at Aligarh Muslim University. It is not affiliated with, officially endorsed by, or operated by the university's administrative offices. All department names, course codes, and trademarks belong to their respective owners.

---

<div align="center">

**Built with passion and pride for Department of Computer Science · Aligarh Muslim University**  
*Empowering scholars through intelligent software.*

</div>
