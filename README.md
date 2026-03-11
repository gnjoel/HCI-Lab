# HCI-Lab
This is Learning Platform for HCI on Usability Testing

# 🧪 HCI Lab — Usability Testing Platform

> An interactive, browser-based usability evaluation platform for the **Human Computer Interaction** course at Asia-Pacific International University (APIU).

<div align="center">

![HCI Lab](https://img.shields.io/badge/HCI_Lab-Usability_Testing-06B6D4?style=for-the-badge)
![Course](https://img.shields.io/badge/Course-Human_Computer_Interaction-8B5CF6?style=for-the-badge)
![Institution](https://img.shields.io/badge/Institution-APIU-EC4899?style=for-the-badge)
![License](https://img.shields.io/badge/License-CC_BY--NC_4.0-green?style=for-the-badge)

</div>

---

## 📌 Overview

**HCI Lab** is a purpose-built educational web application that guides student groups through two core usability testing methodologies — **Heuristic Evaluation** and **Think-Aloud Protocol** — using a simulated e-commerce website ([AIU-Mart](https://aiu-mart.vercel.app/)) as the test subject.

The platform provides each group with a dedicated, color-themed workspace, auto-saves all progress to the browser's localStorage, captures timestamps for every evaluation phase, and generates a printable group report with JSON export for submission.

---

## 🌐 Live Demo

| Platform | URL |
|---|---|
| 🧪 HCI Lab | **[https://hci-lab.vercel.app](https://hci-lab.vercel.app)** |
| 🛍️ AIU-Mart (Target System) | **[https://aiu-mart.vercel.app](https://aiu-mart.vercel.app)** |

> Replace the links above with your actual deployed URLs.

---

## 🎓 Course Information

| Field | Details |
|---|---|
| **Course** | Human Computer Interaction |
| **Institution** | Asia-Pacific International University (APIU) |
| **Location** | Muak Lek, Saraburi, Thailand |
| **Topics Covered** | Heuristic Evaluation, Think-Aloud Protocol, Usability Testing |
| **Prerequisite Knowledge** | Nielsen's 10 Usability Heuristics |

---

## 👥 Groups

The platform supports 10 student groups (3 members each = 30 students total). Each group has a unique color theme and icon.

| # | Group Name | Theme |
|---|---|---|
| 01 | MIZ | 🔬 Cyan |
| 02 | Design Thinkers | 🔥 Orange |
| 03 | The Visionaries | ⚡ Green |
| 04 | RBG | 💜 Purple |
| 05 | The Unity Crew Group | 🌸 Pink |
| 06 | Ninja | ⭐ Yellow |
| 07 | NoClassTomorrow | 🌊 Blue |
| 08 | UserVerse | 🍀 Emerald |
| 09 | ASA Design | 🎯 Rose |
| 10 | Group I | 🌙 Violet |

---

## 🗂️ Platform Structure

Each group workspace contains four sections navigated via a sidebar:

```
Landing Page (Group Selection)
 └── Group Workspace
      ├── 🚀 Introduction        — Briefing, roles, AIU-Mart link
      ├── 📋 Heuristic Evaluation — Rate all 10 Nielsen heuristics (0–4 severity)
      ├── 🎙️ Think-Aloud Protocol — 4 tasks with live timer, observations, issue logger
      └── 📊 Group Report         → Full printable report with timestamps
```

---

## ✨ Features

### 🎨 Design
- Dark / Light mode toggle (preference saved to localStorage)
- Animated star field background
- Each group has a unique neon color accent theme
- Confetti celebration on phase completion
- Fully responsive — works on desktop, tablet, and mobile

### 📋 Heuristic Evaluation
- All 10 Nielsen Usability Heuristics listed with descriptions
- Severity rating buttons (0 = No Problem → 4 = Critical)
- Notes textarea per heuristic
- Visual indicator when a heuristic has been rated

### 🎙️ Think-Aloud Protocol
- 4 structured task cards (Simple → Medium → Complex → Error Recovery)
- Scenario card with facilitator script built in
- **Live session timer** per task (start / pause / reset)
- Observation notes textarea
- **Quick Issue Logger** — log one-line issues as tags, deletable
- Mark task complete with visual confirmation

### ⏱️ Timestamp Tracking
Automatically recorded and displayed in the report:

| Timestamp | When Captured |
|---|---|
| Heuristic Evaluation Started | Click "Begin Phase 1" |
| Heuristic Evaluation Completed | Click "Complete Phase 1" |
| Think-Aloud Protocol Started | Same moment as heuristic end |
| Think-Aloud Protocol Completed | Click "Complete Phase 2" |
| Per-task Timer | Saved when task is marked complete |
| Report Submitted | Click "Submit Report" |

### 📄 Report & Submission
- **Full Report Page** — dedicated printable white-background report
- Group member name fields (Participant, Facilitator, Observer)
- Phase timestamps and durations
- All heuristic ratings with notes
- All task observations and issue logs
- Phase comparison with auto-generated key insight
- **🖨️ Print / Save as PDF** — browser print dialog
- **💾 Export JSON** — downloads structured `.json` file for instructor
- **✅ Submit** — stamps report as submitted in localStorage

### 💾 Data Persistence
- All data auto-saved to `localStorage` every time a change is made
- Auto-save indicator visible on screen
- Progress persists across page refreshes
- Theme preference (dark/light) persisted

---

## 🧪 Evaluation Workflow

### Group Roles

| Role | Member | Responsibility |
|---|---|---|
| **Participant** | Member 1 | Performs tasks, verbalizes all thoughts |
| **Facilitator** | Member 2 | Reads task cards, prompts participant to keep talking |
| **Observer** | Member 3 | Records verbal comments, hesitations, issues |

### Session Flow

```
1. Instructor shares the HCI Lab URL with all groups
2. Each group selects their group card on the landing page
3. [Introduction] Read briefing → open AIU-Mart in a new tab
4. [Phase 1] Complete Heuristic Evaluation (rate ≥ 5 heuristics to proceed)
5. [Phase 2] Complete Think-Aloud Protocol (complete ≥ 2 tasks to proceed)
6. [Report] Open Full Report → add member names → Submit / Print / Export
```

### Facilitator Script
> *"We are testing the website, not you. Please say out loud everything you are thinking. There are no wrong answers. I cannot help during tasks but I will remind you to keep talking if you go quiet."*

**Reminder prompt when participant is silent:**
> *"Can you tell me what you are thinking right now?"*

---

## 🛠️ Technical Details

| Property | Value |
|---|---|
| **Type** | Single-file HTML application |
| **Frameworks** | None — vanilla HTML, CSS, JavaScript |
| **Fonts** | Google Fonts: Orbitron, Syne, JetBrains Mono |
| **Storage** | Browser localStorage (client-side only) |
| **Dependencies** | None (no npm, no backend) |
| **File** | `index.html` |
| **Lines of Code** | ~1,800+ |

---

## 🚀 Deployment

### Vercel (Recommended)

1. Create a folder called `hci-lab` containing:
   - `index.html` (renamed from `hci-lab.html`)
   - `vercel.json` (see below)

2. Create `vercel.json`:
```json
{
  "version": 2,
  "builds": [
    { "src": "index.html", "use": "@vercel/static" }
  ],
  "routes": [
    { "src": "/(.*)", "dest": "/index.html" }
  ]
}
```

3. Go to [vercel.com](https://vercel.com) → **Add New → Project** → drag and drop folder → **Deploy**

### GitHub Pages

1. Create a public GitHub repository called `hci-lab`
2. Upload `index.html`
3. Go to **Settings → Pages → main branch → root → Save**
4. Live at: `https://yourusername.github.io/hci-lab/`

---

## ⚠️ localStorage Notice

HCI Lab stores all student data in the **browser's localStorage** — not on a server. This means:

- ✅ Data persists across page refreshes on the **same device and browser**
- ✅ Students can resume where they left off if they return to the same device
- ❌ Data does **not** sync across devices or browsers
- ❌ Clearing browser cache/data will erase saved progress
- ✅ Students should **Export JSON** or **Print to PDF** before ending the session

---

## 📁 Repository Structure

```
hci-lab/
├── index.html        # Complete application (single file)
├── vercel.json       # Vercel static deployment config
├── README.md         # This file
├── LICENSE           # CC BY-NC 4.0
└── .gitignore        # Git ignore rules
```

---

## 🔗 Related Projects

| Project | Description | Link |
|---|---|---|
| AIU-Mart | Simulated e-commerce target system | [aiu-mart.vercel.app](https://aiu-mart.vercel.app) |
| HCI Lab | This usability testing platform | [hci-lab.vercel.app](https://hci-lab.vercel.app) |

---

## 📄 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license.

You are free to share and adapt this material for **educational purposes**, provided you give appropriate credit and do not use it for commercial purposes.

See [LICENSE](./LICENSE) for full terms.

---

## ⚠️ Disclaimer

HCI Lab and AIU-Mart are **fictional prototypes** created solely for educational use within the Human Computer Interaction course at APIU. All products, brands, prices, and transactions shown are simulated. No real purchases are processed.

---

*Developed for the Human Computer Interaction course — Asia-Pacific International University (APIU), Muak Lek, Saraburi, Thailand*
