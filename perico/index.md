# Perico

<p align="center">
  <img src="./logo.jpeg" alt="Perico logo" width="200">
</p>

**Flashcard app with spaced repetition (not only for language learning).**

Perico helps you memorize vocabulary and phrases using the SM-2 spaced repetition algorithm. Import your own decks via CSV or download an example to get started.

I have been using tools such as Anki, great, but could not update decks as I kept building them, aside from within the app. True pain, inputing cards one by one,
from my phone, is a no-go, so I ended up with massive fancy decks shared by other users. Greed might trick one into believe more is better but in my case, this was a great way for losing my way.

I now build my decks with AI. I study Chinese with the Assimil method. My current flow is:
1. Study the textbook
2. Log the vocabulary and sentences by speaking it to an AI (e.g ChatGPT does indeed understand my Chinese prononciation). Writing the vocabulary works fine but speaking for the lazy works just as well.
3. Prompt the AI to generate the CSV following the required format: 
> Generate a CSV with columns:
> - number: a string, format as `lesson_level:card_nb`
> - front: the text in our langauge, the question
> - back: the answer (e.g the translation)
> - hint: the pinyin text
> - tag: `lesson_level`

I format the number as: `lesson_level:card_nb` and use the hints for various info I want to have access to before revealing the answer (e.g Pinyin prononciation for Chinese learning, but can be any
other hint).

---

## Features

- **SM-2 Spaced Repetition** — Cards are scheduled based on how well you know them, optimizing long-term retention
- **Multiple Study Modes** — Standard (flip cards), Listening (local TTS audio), Multiple Choice, and Speed mode
- **CSV Import** — Bring your own decks in a simple CSV format
- **Cloud Sync** — Optionally sync your decks via GitHub (Google Drive and such coming next if requested)
- **Text-to-Speech** — Decent enough pronunciations for cards in supported language!
- **Dark Mode** — Full light/dark/system theme support
- **Offline First** — All data stored locally on your device, no account required

---

## Quick Start

### 1. Import a Deck

Prepare a CSV file with these columns:

| Column | Required | Description |
|--------|----------|-------------|
| `number` | Yes | Unique string ID for each card (e.g. `1`, `L3-12`) |
| `front` | Yes | The question or prompt |
| `back` | Yes | The answer |
| `hint` | No | Optional hint shown during review |
| `tag` | No | Optional tag for organizing cards |

Example:

```csv
number,front,back,hint,tag
1,hello,hola,common greeting,basics
2,goodbye,adiós,,basics
```

Open Perico, tap **Import**, and select your CSV file. Cards are matched by `number` — re-importing updates existing cards without losing your review progress.

### 2. Review Cards

From the home screen, tap a deck to see how many cards are due. Tap **Review** to start a session.

- Cards show the **front** first — try to recall the answer
- Tap to **flip** and see the back
- Rate your recall: **Again**, **Hard**, **Good**, or **Easy**
- Your rating determines when the card appears next

### 3. Study Modes

- **Standard** — Classic flip-card review
- **Listening** — Hear the card via text-to-speech, then recall the written form
- **Multiple Choice** — Pick the correct answer from options
- **Speed** — Timed review for quick recall practice

### 4. Example Deck

Download this English-Spanish starter deck to try Perico:

**[example-deck.csv](./example-deck.csv)** (~20 common phrases)

---

## Privacy Policy

**Perico — Flashcard App**
Last updated: March 9, 2026

### Overview

Perico is a flashcard app with spaced repetition. This policy explains what data Perico collects and how it is used.

### Data Storage

All flashcard data (decks, cards, review history, and settings) is stored **locally on your device** using SQLite. No data is sent to any server unless you explicitly enable cloud sync.

### Cloud Sync (Optional)

If you choose to enable cloud sync:

- **GitHub Sync**: Your deck data is stored in a private GitHub Gist under your GitHub account. You authenticate directly with GitHub. Perico does not store your GitHub password — authentication credentials are stored securely in your device's Keychain/Keystore.
- **Google Drive Sync** (if available): Your deck data is stored in your Google Drive. Authentication credentials are stored securely in your device's Keychain/Keystore.

Cloud sync is entirely optional and user-initiated. You can disable it at any time.

### No Data Collection

Perico does not collect, transmit, or share any data. There are no analytics, no tracking, no ads, and no third-party SDKs. The only external services involved are those you explicitly connect for cloud sync (GitHub, Google Drive).

### Changes to This Policy

We may update this privacy policy from time to time. Changes will be posted on this page with an updated "Last updated" date.

### Contact

If you have questions about this privacy policy, please contact: **ha.lagrange9000@gmail.com**

---

## Copyright

Copyright 2026 Dedalum. All rights reserved.
