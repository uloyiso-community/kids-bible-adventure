# ✝️ UCC Kids Bible Adventure

> **"Impacting Generations"** — Uloyiso Community Church

A world-class, offline-first, gamified Sunday School Progressive Web App (PWA) for children aged 5–12. Built for **Uloyiso Community Church (UCC)**, Johannesburg, South Africa.

[![Live App](https://img.shields.io/badge/Live%20App-GitHub%20Pages-6d28d9?style=for-the-badge&logo=github)](https://uloyiso-community.github.io/kids-bible-adventure)
[![License](https://img.shields.io/badge/License-MIT-f5c842?style=for-the-badge)](LICENSE.md)
[![Lessons](https://img.shields.io/badge/Lessons-51-10b981?style=for-the-badge)]()
[![PWA](https://img.shields.io/badge/PWA-Offline%20Ready-3b82f6?style=for-the-badge)]()

---

## 🌟 What Is This?

UCC Kids Bible Adventure turns Sunday School into an exciting game. Children explore 51 Bible lessons across 21 units, earn XP and Faith Coins, unlock badges, and build a streak — all while learning God's Word.

It works **completely offline** after the first load. No app store. No data plan required. Just one HTML file.

---

## ✅ Features

### 📖 51 Full Bible Lessons across 21 Units
| Unit | Topic |
|------|-------|
| 1 | Jesus Begins His Ministry |
| 2 | Jesus Makes the Difference |
| 3 | Miracles & Ministry |
| 4 | The Plan of Salvation |
| 5 | The Ten Commandments |
| 6 | God is Unique and Powerful |
| 7 | We Imitate Jesus |
| 8 | The Church Around the World |
| 9 | God's Mercy |
| 10 | God's Faithful Servants |
| 11 | God's Amazing Power |
| 12 | The Story of Christmas |
| 13 | Worship & Praise |
| 14 | Prayer Changes Things |
| 15 | The Holy Spirit |
| 16 | Jesus the King Returns |
| 17 | Living for God Every Day |
| 18 | Heroes of Faith |
| 19 | The Church — God's Family |
| 20 | God's Word — Our Foundation |
| 21 | Sharing Your Faith |

Each lesson includes:
- 📖 Child-friendly Bible story (ages 5–12)
- 🎮 Interactive memory verse word-game
- ✅ 5-question quiz with instant feedback
- 🎯 Real-life weekly challenge
- 💬 Family discussion questions

### 🎮 Gamification
- ⚡ **XP System** — earn points for every activity
- 🪙 **Faith Coins** — currency for engagement
- ⭐ **Stars** — 1–3 per lesson based on quiz score
- 🔥 **Daily Streak** — keeps kids coming back
- 🏅 **12 Badges** — Scripture Master, Faith Builder, etc.
- 🏆 **10 Levels** — Beginner Explorer → Mighty Disciple

### 👨‍👩‍👧 Parent Dashboard
- Weekly progress summary
- Auto-generated prayer guide
- Family discussion questions
- Real-life challenge for the week
- Progress export

### 📴 Offline-First PWA
- Works in airplane mode after first visit
- Installable to home screen (Android & iOS)
- Service worker caches entire app
- No internet required for lessons, quizzes, or games

### 💬 Feedback System
- Children can report confusion, suggest improvements, request features, or share praise
- Earns +5 XP per submission (encourages engagement)

---

## 🚀 Deployment

### GitHub Pages (Recommended)
1. Fork or clone this repo
2. Go to **Settings → Pages → Source → Deploy from branch → main → / (root)**
3. App goes live at `https://uloyiso-community.github.io/kids-bible-adventure`

### Vercel
```bash
npx vercel --prod
```

### Local
Just open `index.html` in any browser. No server needed.

---

## 🛠️ Tech Stack

This is intentionally **zero-dependency**. One file. No build step. No npm. No framework.

| Layer | Technology |
|-------|-----------|
| UI | Vanilla HTML + CSS (custom design system) |
| Logic | Vanilla JavaScript (ES6+) |
| Fonts | Google Fonts (Fredoka One + Nunito) |
| Storage | LocalStorage (offline persistence) |
| PWA | Service Worker + Web App Manifest (injected) |
| Deployment | GitHub Pages / Vercel / Any static host |

---

## 📁 Repository Structure

```
kids-bible-adventure/
├── index.html          # The entire app (225KB, self-contained)
├── README.md           # This file
├── LICENSE.md          # MIT License
├── .gitignore          # Standard ignores
└── .github/
    └── workflows/
        └── deploy.yml  # Auto-deploy to GitHub Pages on push
```

---

## 🔧 Development

To modify the app, edit `index.html` directly. Key sections are clearly commented:

```
// DATA          — All 51 lessons (line ~1311)
// STATE         — User progress model
// PERSISTENCE   — LocalStorage save/load
// RENDER        — UI generation functions
// GAMIFICATION  — XP, coins, badges, levels
// PWA           — Manifest, service worker, offline
// FEEDBACK      — Suggestion system
```

### Adding a Lesson
Add a new lesson object to the appropriate unit in the `UNITS` array:

```javascript
{
  id: 52,                          // next sequential ID
  title: "Your Lesson Title",
  scripture: "Book Chapter:Verses",
  icon: "🌟",
  xpReward: 60,
  coinReward: 12,
  keyLesson: "One sentence takeaway",
  story: "Child-friendly story text...",
  memoryVerse: "The verse text",
  memoryRef: "Reference",
  quiz: [
    { q: "Question?", opts: ["A","B","C","D"], ans: 0 }  // ans = index
  ],
  challenge: "Weekly real-life challenge",
  discussions: ["Question 1", "Question 2", "Question 3"]
}
```

---

## 🌍 Vision

> This app is designed to scale beyond UCC — to become a resource for churches globally. If you represent a church or ministry that would like to use or adapt this, please reach out.

**Built with love for the children of Uloyiso Community Church.**  
*Impacting Generations — one lesson at a time.*

---

## 🙏 Contributing

Pull requests welcome. Please keep the zero-dependency philosophy — no npm packages, no build tools, no frameworks. The app must remain a single deployable HTML file.

1. Fork the repo
2. Create a branch: `git checkout -b feature/new-lessons`
3. Make changes to `index.html`
4. Test locally by opening in a browser
5. Submit a PR with a description of what was added/changed

---

## 📄 License

[MIT License](LICENSE.md) — free to use, adapt, and redistribute with attribution.

© 2025 Uloyiso Community Church | Johannesburg, South Africa
