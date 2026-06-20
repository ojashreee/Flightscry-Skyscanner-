# Flightscry

This repository contains my completed submission for the **Skyscanner Software Engineering Virtual Experience Program (Forage)** — Android task.

## About this submission

Skyscanner is building **Flightscry**, a new app to let users view their flight itineraries on their phones. This repo contains a proof-of-concept (PoC) UI for the app, built with **Backpack**, Skyscanner's Android UI component library, to demonstrate what the interface could look like using dummy flight data.

### The task

Build an Android UI (Kotlin, Backpack `43.0.0`) that displays:

- A **flight information card** with a flight number
- A **departure card** with a 3-letter airport code and departure time
- An **arrival card** with a 3-letter airport code and arrival time

### What I implemented

- `MainActivity.kt` — Empty Activity entry point (min SDK 33)
- `res/layout/activity_main.xml` — three `BpkCardView` components (large corner style), each containing `BpkText` elements styled with Backpack's typography scale (`bpkTextHeading1`, `bpkTextHeading2`, `bpkTextSubheading`, `bpkTextLabel1`) and spacing tokens (`bpkSpacingBase`)
- Backpack added as a Gradle dependency: `implementation 'net.skyscanner.backpack:backpack-android:43.0.0'`

### Running it

1. Open the project in Android Studio and let Gradle sync finish.
2. Click the green **Run** button to launch on the emulator (or a connected device).
3. You should see three stacked cards: Flight Information, Departure, and Arrival.
