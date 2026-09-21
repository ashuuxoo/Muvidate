# MuviDate 🎬

> A social watch-party web app for watching movies together with synchronized playback, real-time chat, and voice notes.

[![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5%2B-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-8-646CFF?logo=vite&logoColor=white)](https://vite.dev/)
[![Firebase](https://img.shields.io/badge/Firebase-12-FFCA28?logo=firebase&logoColor=black)](https://firebase.google.com/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

## Overview

MuviDate is a modern movie watch-party application built with React and Firebase. It combines a streaming-style movie catalog with private watch rooms so friends can watch the same video together.

### Highlights

- 🎥 Synchronized watch rooms with a 4-digit room code
- ▶️ Real-time playback synchronization
- 💬 Live room chat and voice-note support
- 🔐 Firebase Authentication with anonymous sessions and username/password accounts
- 🎞️ Movie catalog powered by Firestore
- 🔎 Search and genre filtering
- 📱 Responsive desktop and mobile UI
- 🖼️ Movie details, posters and featured hero banner
- ♻️ Persistent browser sessions

## Tech Stack

| Layer | Technology |
| --- | --- |
| UI | React 19, TypeScript |
| Build | Vite |
| Styling | Tailwind CSS |
| Icons | Lucide React |
| Motion | Motion |
| Backend | Firebase Authentication, Firestore, Realtime Database |
| AI | Google Gemini SDK |

## Architecture

The project uses a component-driven React frontend, while Firebase provides authentication, movie data, room state, chat and real-time synchronization.

```text
src/
├── components/       # UI, modals, player and watch-room features
├── context/          # React application state / auth context
├── lib/              # Firebase, media and API utilities
├── App.tsx           # Main application orchestration
├── main.tsx          # React entry point
├── types.ts          # Shared TypeScript models
└── index.css         # Global styles
```

### Watch-party flow

```text
Browse catalog
     │
     ├── Create room ──► 4-digit code
     │                       │
     │                       ├── Synced playback
     │                       ├── Participants
     │                       ├── Live chat
     │                       └── Voice notes
     │
     └── Join room ─────────► Shared watch session
```

## Getting Started

### Prerequisites

- Node.js 18+ (20+ recommended)
- npm, pnpm, yarn, or Bun
- A Firebase project with the required services enabled

### 1. Clone

```bash
git clone https://github.com/ashuuxoo/Muvidate.git
cd Muvidate
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

```bash
cp .env.example .env.local
```

Fill in the Firebase and Gemini values required by your deployment.

> Never commit real secrets or production environment files.

### 4. Run locally

```bash
npm run dev
```

The development server runs on port **3000** by default.

### 5. Build for production

```bash
npm run build
npm run preview
```

### 6. Type-check

```bash
npm run lint
```

## Firebase Setup

MuviDate uses:

- **Firebase Authentication** for anonymous and username/password sessions
- **Cloud Firestore** for user profiles and movie catalog data
- **Realtime Database** for watch-room state and synchronization

Before deployment, configure appropriate Firebase Authentication, Firestore and Realtime Database rules. Client-side configuration is not a security boundary.

## Environment Variables

See [`.env.example`](.env.example).

| Variable | Purpose |
| --- | --- |
| `GEMINI_API_KEY` | Gemini API access |
| `APP_URL` | Application/base URL |
| `VITE_FIREBASE_API_KEY` | Firebase web API key override |
| `VITE_FIREBASE_AUTH_DOMAIN` | Firebase Auth domain |
| `VITE_FIREBASE_PROJECT_ID` | Firebase project ID |
| `VITE_FIREBASE_STORAGE_BUCKET` | Firebase Storage bucket |
| `VITE_FIREBASE_MESSAGING_SENDER_ID` | Firebase messaging sender ID |
| `VITE_FIREBASE_APP_ID` | Firebase app ID |
| `VITE_FIREBASE_DATABASE_URL` | Realtime Database URL |

## Useful Scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the Vite development server |
| `npm run build` | Create a production build |
| `npm run preview` | Preview the production build |
| `npm run lint` | Run TypeScript type-checking |
| `npm run clean` | Remove generated build/server artifacts |

## Key Components

- `Navbar` — search, profile and room actions
- `HeroBanner` — featured movie presentation
- `MovieCard` / `MovieDetailModal` — catalog browsing
- `CreateRoomModal` / `JoinRoomModal` — room lifecycle
- `WatchRoom` — synchronized watch-party experience
- `VideoPlayer` — playback UI and synchronization
- `RoomChat` — live chat
- `VoiceNoteRecorder` / `VoiceNotePlayer` — voice messages
- `ProfileModal` / `UsernameSetupModal` — account onboarding

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for the development workflow and pull-request expectations.

## Security

Please do not commit credentials, tokens, private user data or production database exports.

For suspected vulnerabilities, see [SECURITY.md](SECURITY.md).

## Roadmap

Possible future improvements include stronger room moderation, reconnect recovery, broader media compatibility, automated CI, synchronization test coverage and further accessibility improvements.

## License

MuviDate is licensed under the MIT License. See [LICENSE](LICENSE).

## Author

**Ashis Kumar Das**

GitHub: [@ashuuxoo](https://github.com/ashuuxoo)
