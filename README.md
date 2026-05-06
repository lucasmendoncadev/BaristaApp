# Barista

An intelligent coffee companion app for remote professionals. Barista helps you dial in your espresso, track your bean pantry, follow guided brew recipes, and discover new coffees — all powered by AI.

## Getting Started

### Prerequisites

- Node.js 18+
- [Expo CLI](https://docs.expo.dev/get-started/installation/)
- iOS Simulator (macOS) or Android Emulator, or the Expo Go app on a physical device

### Installation

```bash
npm install
```

### Environment Variables

Copy the example env file and fill in your credentials:

```bash
cp .env.example .env
```

| Variable | Description |
|----------|-------------|
| `EXPO_PUBLIC_SUPABASE_URL` | Your Supabase project URL |
| `EXPO_PUBLIC_SUPABASE_ANON_KEY` | Your Supabase anonymous key |
| `EXPO_PUBLIC_ANTHROPIC_API_KEY` | Anthropic API key (powers Brew Coach) |

### Running the App

```bash
npx expo start
```

Then press `i` for iOS simulator, `a` for Android emulator, or scan the QR code with Expo Go.

## Features

### Brew Coach
AI-powered voice assistant that helps you improve your technique, adjust variables, and troubleshoot extractions in real time.

### Dial-In Assistant
Log shots, visualize extraction curves, and get AI-driven recommendations to hit your target flavor profile.

### Bean Pantry
Track your coffee inventory with roast dates, freshness alerts, and peak-flavor notifications so you never brew stale beans.

### Brew Timer
Step-by-step guided brewing workflows for pour-over, espresso, AeroPress, and more — with dynamic timers and haptic cues.

### Marketplace
Buy and sell specialty beans within the community. Includes taste-profile matching, seller ratings, and order tracking.

### Brew Passport & Gamification
Earn stamps, maintain streaks, and unlock achievements as you explore new origins, methods, and roasters.

### Dashboard
A modular, configurable home screen with draggable blocks — schedule, history, quick-brew shortcuts, and community highlights.

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Expo SDK 55 / React Native |
| Navigation | Expo Router (file-based) |
| State | Zustand |
| Storage | AsyncStorage |
| Backend | Supabase (auth, database, realtime) |
| AI | Anthropic Claude API |
| Animations | react-native-reanimated |
| Audio | expo-audio (voice input for Coach) |

## Project Structure

```
app/              # Expo Router screens & layouts
  (tabs)/         # Tab navigator (home, brew, pantry, market)
  bean/           # Bean detail screens
  brew-guide/     # Guided brew flows
  coach/          # Brew Coach AI chat
  dial-in/        # Dial-in logging & analysis
  onboarding/     # First-launch onboarding
components/       # Reusable UI & feature components
stores/           # Zustand state stores
lib/              # Utilities & API clients
hooks/            # Custom React hooks
constants/        # Theme, colors, config
types/            # TypeScript type definitions
assets/           # Images, icons, splash screens
scripts/          # Build & dev helper scripts
```

## License

Private — all rights reserved.
