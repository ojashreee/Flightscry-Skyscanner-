# Flightscry-Skyscanner TASK 3
# ✈️ Flightscry

> Your flight itinerary, at a glance — no digging through emails, no squinting at confirmation PDFs.

Flightscry is Skyscanner's next idea: an app where travelers can pull up their flight details the moment they need them. This repo is the very first step in bringing that to life — a proof-of-concept UI built with **Backpack**, Skyscanner's own Android design system, showing exactly what that itinerary screen could look like.

## 🎯 About this submission

This repository contains my completed submission for the **Skyscanner Software Engineering Virtual Experience Program (Forage)** — Android task.

Skyscanner is building **Flightscry** to let users view their flight itineraries on their phones. This repo is a proof-of-concept (PoC) UI for the app, demonstrating what the interface could look like using dummy flight data, built entirely with Backpack components.

### The brief

Build an Android UI (Kotlin, Backpack `43.0.0`) that displays:

- ✈️ A **flight information card** with a flight number
- 🛫 A **departure card** with a 3-letter airport code and departure time
- 🛬 An **arrival card** with a 3-letter airport code and arrival time

## 📱 What it looks like

Three stacked cards, each with rounded corners and Backpack's typography doing the heavy lifting:

```
┌─────────────────────────────┐
│  Flight Information          │
│  Flight number: BA1326       │
└─────────────────────────────┘

┌─────────────────────────────┐
│  Departure                   │
│  LHR — 14:35                 │
└─────────────────────────────┘

┌─────────────────────────────┐
│  Arrival                     │
│  JFK — 17:50                 │
└─────────────────────────────┘
```

No clutter, no guesswork — exactly the information a traveler is glancing at their phone for, and nothing else.

## 🧩 What I implemented

| File | What it does |
|---|---|
| `MainActivity.kt` | Empty Activity entry point (min SDK 33) |
| `res/layout/activity_main.xml` | Three `BpkCardView` components (large corner style), each containing `BpkText` elements styled with Backpack's typography scale (`bpkTextHeading1`, `bpkTextHeading2`, `bpkTextSubheading`, `bpkTextLabel1`) and spacing tokens (`bpkSpacingBase`) |
| `build.gradle` | Backpack added as a dependency: `implementation 'net.skyscanner.backpack:backpack-android:43.0.0'` |

Every visual choice here — corner radius, type scale, spacing — comes straight from Backpack's design system, not hand-rolled values. That's the whole point of a shared component library: build once centrally, reuse everywhere, and any future visual refresh of Backpack updates this screen automatically.

## 🧰 Tech stack

- **Kotlin**
- **Android Studio** / Gradle
- **Backpack for Android** (`backpack-android:43.0.0`) — Skyscanner's UI component library
- Min SDK 33 (Android Tiramisu)

## 🚀 Running it

1. Open the project in **Android Studio** and let Gradle sync finish.
2. Click the green **Run** button to launch on the emulator (or a connected device).
3. You should see three stacked cards: **Flight Information**, **Departure**, and **Arrival** — populated with sample flight data.

## 💡 Why this matters

This is just a PoC, but it's a deliberate one: by building the UI entirely out of Backpack components rather than custom views, this screen is already speaking the same visual language as the rest of Skyscanner's apps. When this moves from prototype to production, swapping in real itinerary data is the easy part — the design system work is already done.

## 📄 License

This project was built as part of Skyscanner's Forage Virtual Experience Program, for educational and portfolio purposes.

<p align="center">
Built with Kotlin, Backpack, and a small obsession with airport codes. 🛫
</p>
