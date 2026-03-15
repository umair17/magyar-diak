# 🇭🇺 Magyar Diák — Hungarian Language Learning App

> A complete A1–C2 Hungarian language learning Progressive Web App built with React.  
> Works fully offline. No app store. Install directly from your browser.

-----

## Live App

**[Launch Magyar Diák →](https://yourusername.github.io/magyar-diak/)**

> Replace `yourusername` with your actual GitHub username after deploying.

-----

## Install as an App (No App Store Required)

Magyar Diák is a **Progressive Web App (PWA)** — it installs directly from the browser onto your home screen and works completely offline after the first load.

### Android (Chrome)

1. Open the app URL in **Chrome**
1. Tap the **⋮ menu** (three dots, top-right)
1. Tap **“Add to Home screen”**
1. Tap **“Add”** on the confirmation
1. The app icon appears on your home screen — tap it to open fullscreen

### iPhone / iPad (Safari)

1. Open the app URL in **Safari** (must be Safari, not Chrome)
1. Tap the **Share button** (the square with an arrow pointing up, bottom of screen)
1. Scroll down and tap **“Add to Home Screen”**
1. Tap **“Add”** (top-right)
1. The app icon appears on your home screen

### Desktop (Chrome / Edge)

1. Open the app URL
1. Look for the **install icon** (⊕) in the address bar
1. Click **“Install Magyar Diák”**
1. The app opens in its own window without browser UI

> **Offline use:** The service worker caches everything on first load. After that, the app works with no internet connection — all 36 chapters, SRS cards, quizzes, and your personal data are stored locally on your device.

-----

## Features

### 📚 Curriculum — 36 Chapters, A1 to C2

Full structured curriculum based on *Core Concepts of Hungarian Language* by László Ragoncsa, supplemented with certified CEFR-aligned content.

|Level                      |Chapters|Topics                                                                                                                      |
|---------------------------|--------|----------------------------------------------------------------------------------------------------------------------------|
|**A1** — Absolute Beginner |8       |Alphabet, Vowel Harmony, Nouns & Plurals, Verbs, Vocabulary, Family, Daily Life, Food                                       |
|**A2** — Elementary        |6       |Cases, Adjectives, Pronouns, Possession, Articles, Numerals                                                                 |
|**B1** — Intermediate      |8       |Tenses, Verbal Prefixes, Moods, Location Suffixes, Modal Verbs, Irregular Verbs, Relative Clauses, Postpositions & Questions|
|**B2** — Upper Intermediate|6       |Word Order, Conjunctions, Passive Voice, Adverbs, Subjunctive, Body & Health                                                |
|**C1** — Advanced          |4       |Verbal Nouns & Participles, Word Formation, Information Structure                                                           |
|**C2** — Mastery           |4       |Register & Formality, Proverbs & Idioms, Language History, Literary Hungarian                                               |

Each chapter contains:

- **Theory** — clear explanations with grammar tables
- **20 example sentences** — Hungarian with English translations and usage notes
- **Vocabulary** — key words with audio pronunciation
- **Practice exercise** — multiple choice, true/false, or matching
- **Summary** — key takeaways with memory anchors

### 🧠 Spaced Repetition (SRS)

- SM-2 algorithm schedules reviews at the optimal memory interval
- Every vocabulary word and example from all 36 chapters becomes a flash card
- Rating buttons show the next review interval: **Again** (tomorrow) · **Hard** (2–3 days) · **Good** (4–7 days) · **Easy** (1–2 weeks)
- Session history and card progress persist across sessions

### 🎯 Practice Modes

|Mode                |Description                                                     |
|--------------------|----------------------------------------------------------------|
|**SRS Review**      |Daily flash card sessions, 20 cards at a time                   |
|**Level Quizzes**   |187 multiple-choice questions across all 6 levels               |
|**Verb Drill**      |10-question conjugation sessions — definite and indefinite forms|
|**Sentence Builder**|Translate English sentences into Hungarian, with pronunciation  |

### 📝 My Notes

|Tab               |Description                                                         |
|------------------|--------------------------------------------------------------------|
|**Quiz Bank**     |Create your own MCQ questions, edit and delete them                 |
|**Add to Quizzes**|Add questions directly to any built-in level’s quiz bank            |
|**My Chapters**   |Create custom chapters at any CEFR level                            |
|**Sentences**     |Save example sentences with translations, tags, and grammar notes   |
|**Vocabulary**    |Personal word list with part of speech, example sentences, and notes|

### 🔊 Pronunciation

Every Hungarian word and example sentence has a **speak button** using the Web Speech API. Tap any 🔊 icon to hear the word pronounced in Hungarian.

### 🌍 Themes

Four colour themes with WCAG AA compliant contrast — switchable from the nav panel or Settings:

|Theme            |Style                                          |
|-----------------|-----------------------------------------------|
|**Piros** (Red)  |Warm off-white background, Hungarian red accent|
|**Fehér** (White)|Pure white, deep navy accent                   |
|**Zöld** (Green) |Crisp light, forest green accent               |
|**Arany** (Gold) |Dark background, gold accent                   |

### 📊 Progress Tracking

- XP system with 10 levels — earn XP for completing chapters and quizzes
- Per-level progress bars on the home screen
- Quiz best scores stored per level
- Streak counter for consecutive days of study
- Completed chapters list in Profile

### 💾 Data Management

All data is stored locally on your device using `localStorage`. You can export a full JSON backup and import it on another device.

**Export/import format:** `.json` — see the schema panel in Profile → Data Management.

-----

## How to Use

### Starting Out (A1)

1. Tap **Learn** in the bottom nav
1. Tap **A1 — Absolute Beginner**
1. Tap **The Alphabet & Pronunciation** — your first chapter
1. Read through **Theory**, swipe through **Examples**, try the **Practice** exercise
1. Tap **Complete · +30 XP** when you finish
1. Work through chapters in order — each level builds on the previous

### Daily Review Routine

1. Open the app
1. If the home screen shows **cards due for review**, tap the banner to start SRS
1. Rate each card honestly — the algorithm adjusts future intervals automatically
1. After review, continue with the next Learn chapter or a Quiz

### Adding Your Own Content

- **My Notes → Sentences**: Save any sentence you encounter in the wild
- **My Notes → Vocabulary**: Build your personal word list
- **My Notes → Add to Quizzes**: Create questions for chapters you find difficult
- **My Notes → My Chapters**: Write notes for topics not covered in the curriculum

-----

## Offline Behaviour

After the first visit, the service worker caches:

- `index.html` — the complete app (all 36 chapters, all 187 quiz questions, all UI)
- `manifest.json`, icons

Everything runs locally. No server requests are made during normal use. Internet is only needed to load React and Babel on the very first visit (cached immediately after).

-----

## Technology

- **React 18** — UI with hooks
- **Web Speech API** — Hungarian pronunciation
- **localStorage** — all data persistence
- **SM-2 algorithm** — spaced repetition scheduling
- **Service Worker** — offline caching
- **PWA manifest** — installable on iOS, Android, and desktop

No backend. No account required. No tracking.

-----

## Deploying Updates

When a new version of `index.html` is available:

1. Replace the file in your GitHub repo (drag and drop → Commit changes)
1. GitHub Pages deploys in ~60 seconds
1. On next app open, the service worker fetches the new version automatically

> **Note:** Users may need to close and reopen the app once for the update to apply, as the service worker serves the cached version until the new one is fully downloaded.

-----

## Project Structure

```
/
├── index.html        ← Complete React app (all curriculum, UI, SRS engine)
├── manifest.json     ← PWA metadata (name, icons, display mode)
├── sw.js             ← Service worker (offline caching)
├── icon-192.png      ← App icon (home screen)
└── icon-512.png      ← App icon (splash screen)
```

-----

## Curriculum Sources

Content is based on *Core Concepts of Hungarian Language* by László Ragoncsa, extended with certified CEFR-aligned material from:

- The Hungarian KER (Közös Európai Referenciakeret) framework
- Hungaricum curriculum guidelines
- Standard Hungarian linguistic reference: É. Kiss, Kiefer, Siptár — *A magyar nyelv leíró nyelvtana*
- Cultural and historical content sourced from Hungarian academic references

-----

## Licence

Personal and educational use. Content is based on published language learning materials.