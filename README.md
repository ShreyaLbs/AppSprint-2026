<p align="center">
  <img src="assets/banner.jpeg" alt="AppSprint 2026 Banner" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Hackathon-AppSprint%202026-7C3AED?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Duration-15%20Days-0D9488?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Mode-Virtual-2563EB?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Status-Open-16A34A?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/any%20-06B6D4?style=for-the-badge&logo=flutter"/>
</p>

<h1 align="center">🏆 AppSprint Solution Challenge 2026</h1>
<p align="center">
  A 15-day virtual app development hackathon where you build a mobile application,<br/>
  solve a real problem, and ship a working APK.
</p>

<p align="center">
  <a href="YOUR_REGISTRATION_FORM_LINK"><strong>📝 Register Now</strong></a> ·
  <a href="#-timeline"><strong>📅 Timeline</strong></a> ·
  <a href="#-challenge-tracks"><strong>🎯 Tracks</strong></a> ·
  <a href="#-judging-criteria"><strong>⚖️ Judging</strong></a> ·
  <a href="YOUR_WHATSAPP_LINK"><strong>💬 Join Community</strong></a>
</p>

---

# SymptomBridge

## Project Name
SymptomBridge

## Team Information
- **Team:** Solo
- **Name:** Shreya Ajith
- **Institution:** LBS Institute of Technology for Women (LBSITW), Thiruvananthapuram
- **Track:** HealthTech

## Problem Statement
Rural and low-connectivity communities often lack quick, reliable ways to
judge how urgent a health symptom is before reaching a doctor. Low literacy,
limited internet access, and language barriers make most existing
symptom-checker apps impractical for these users — they assume constant
connectivity, high literacy, and English-only interfaces.

## Solution
SymptomBridge is an **offline-first mobile app that provides urgency triage
guidance — not diagnosis.** Users select their symptoms, answer a few simple
follow-up questions (voice or tap), and receive a clear, color-coded urgency
result: self-care, see a doctor soon, or go to a hospital now — along with
basic next-step guidance for that level.

The app works fully offline, supports Malayalam and English, and is
designed around large, icon-based, low-literacy-friendly interactions.

## Features
- **12-symptom triage flow** with follow-up questions per symptom
- **Hybrid urgency engine**: deterministic clinical red-flag rules act as an
  authoritative safety layer for known-dangerous symptom combinations; a
  trained Random Forest classifier (transpiled to run natively on-device,
  no external ML runtime needed) adds nuanced judgment and a confidence
  score for cases that don't hit a hard red flag
- **Explainability panel** — every result shows *why* it was reached, in
  plain language, including model confidence when the ML path is used
- **Multi-symptom combination detection** — some symptom pairs (e.g. fever +
  breathing difficulty) are escalated even when neither alone would be,
  reflecting that combined symptoms can be more serious than either in
  isolation
- **Basic intervention/first-aid guidance** per urgency level
- **Offline PHC/hospital directory pointer** (general guidance, not a live
  location lookup) on urgent results, plus India's national emergency
  number
- **Voice input** for symptom selection and answers, with a clear fallback
  message when unavailable offline (manual tap always works)
- **Malayalam and English** toggle across the entire app
- **Local history** of past checks, stored on-device only
- **Fully offline core flow** — no network calls required to use the app

## Tech Stack
- **Framework:** Expo (React Native), Expo Router
- **ML:** scikit-learn (RandomForestClassifier) trained in Python, transpiled
  to plain JavaScript via m2cgen for on-device inference with no external ML
  runtime dependency
- **Storage:** AsyncStorage (local history)
- **i18n:** i18next + react-i18next (English/Malayalam)
- **Voice:** @react-native-voice/voice
- **Fonts:** Noto Sans (Google Fonts) — covers both Latin and Malayalam script
- **Icons:** @expo/vector-icons

## AI Tool Disclosure
This project was built with assistance from:
- **Anthropic's Claude** — used for architecture planning, dataset design,
  training data generation and labeling, model training and evaluation,
  the model-to-JavaScript export pipeline, design direction, and debugging
  guidance throughout the build
- **Google's Antigravity** — used to generate and iterate on the app's UI
  and React Native implementation, based on detailed specifications and
  data contracts provided during development

All AI-assisted code and design decisions were reviewed, tested, and are
understood by the developer, including the ML pipeline, the triage engine's
hybrid decision logic, and the app's screen implementations.

## Installation Instructions
```bash
git clone https://github.com/ShreyaLbs/AppSprint-2026.git
cd AppSprint-2026
npm install
npx expo start
```
To build a release APK:
```bash
eas build -p android
```

## Screenshots
[ADD screenshots of: Home screen, Symptom picker, Follow-up questions,
Result screen (each urgency color), Explainability panel expanded, History
screen, Malayalam toggle view]

## Demo Video
[ADD link once recorded — YouTube (public/unlisted) or public Google Drive,
max 2 minutes]

## APK Download
[ADD link to GitHub Releases once built]

## Important Note
SymptomBridge provides **urgency triage guidance only** and does **not**
diagnose medical conditions. It is not a substitute for professional medical
advice, diagnosis, or treatment. Always consult a qualified doctor or health
worker for medical concerns.

## Future Scope
- Expand training data for the ML classifier with more real-world labeled
  cases, particularly to close the known recall gap on urgent-case detection
- Real location-based PHC/hospital lookup (requires connectivity or bundled
  regional facility data)
- Additional regional languages beyond Malayalam and English
- Play Store deployment
  Made with 💜 by App Development IG · muLearn LBSITW
</p>
