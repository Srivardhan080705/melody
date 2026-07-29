<div align="center">
<img src="fastlane/metadata/android/en-US/images/icon.png" width="160" height="160" style="display: block; margin: 0 auto"/>
<h1>Melody</h1>
<p>A music client that fuses Spotify and YouTube Music into one seamless experience</p>

[![Latest release](https://img.shields.io/github/v/release/FrancescoGrazioso/Meld?style=for-the-badge)](https://github.com/FrancescoGrazioso/Meld/releases/latest)
[![GitHub license](https://img.shields.io/github/license/FrancescoGrazioso/Meld?style=for-the-badge)](https://github.com/FrancescoGrazioso/Meld/blob/main/LICENSE)
[![Downloads](https://img.shields.io/github/downloads/FrancescoGrazioso/Meld/total?style=for-the-badge)](https://github.com/Srivardhan080705/melody/releases/tag/v0.8.1)

</div>

## What is Melody?

**Melody** is an Android music client that brings together the best of Spotify and YouTube Music. It uses your Spotify account to power personalized recommendations, search, and home content — while streaming audio through YouTube Music.

The name "Melody" reflects the core idea: **melding** two music platforms into a single, unified listening experience.

### Why Melody?

- **Spotify's personalization** — Your top tracks, favorite artists, and curated playlists from Spotify drive the recommendations
- **YouTube Music's catalog** — Access YouTube Music's vast library for streaming, including rare tracks, live performances, and remixes
- **No setup required** — Just log in with your Spotify account directly in the app. No developer dashboard, no Client ID, no extra steps
- **No Spotify Premium required** — Melody uses Spotify's data APIs (not streaming), so a free Spotify account is all you need
- **Built-in recommendation engine** — A custom algorithm builds personalized queues using your Spotify listening history, without relying on deprecated API endpoints

## Features

### Spotify Integration
- **Spotify as search source** — Search results powered by Spotify, with automatic YouTube Music matching for playback
- **Spotify as home source** — Home screen populated with your Spotify top tracks, top artists, playlists, and new releases
- **Spotify-only mode** — Option to hide all YouTube-based content and show exclusively Spotify-powered sections on the home screen
- **Smart queue generation** — Custom recommendation engine that builds radio-like queues from your Spotify taste profile (top tracks/artists across 3 time ranges, genre similarity, popularity matching)
- **Spotify library sync** — Access your Spotify playlists and liked songs directly in the app
- **Spotify-to-YouTube matching** — Fuzzy matching algorithm with local caching for fast, accurate track resolution
- **Manual match override** — If a Spotify track is matched to the wrong YouTube video, you can manually fix it by pasting the correct YouTube link. The override is saved permanently and takes priority over automatic matching
- **Spotify album browsing** — Dedicated album screen for Spotify albums with full tracklist, metadata, and one-tap playback
- **Hybrid profile cache** — 3-tier data strategy (GraphQL → REST API → local DB) with persistent caching for instant home screen loading on app restart, automatic rate-limit handling, and parallel artist image enrichment
- **Artist navigation** — Tap any Spotify artist on the home screen to navigate directly to their YouTube Music artist page

### Lossless Audio (Experimental)
- **Qobuz backend** — Optional FLAC and Hi-Res (up to 24-bit / 192 kHz) streaming via the Qobuz catalog, replacing YouTube Music's lossy audio
- **Deterministic matching** — Uses ISRC (the universal track identifier shared by Spotify and Qobuz) so Spotify-sourced tracks resolve to their exact Qobuz counterpart without ambiguity
- **Persistent match cache** — Once a track has been resolved on Qobuz, the match is saved locally so subsequent plays skip the search step entirely
- **Multi-backend fallback** — Three independent Qobuz resolvers (Monokenny, Jumo, Squid) are tried in sequence if the primary one is rate-limited or unavailable
- **Quality tiers** — Choose between AAC 320 kbps, CD quality (16-bit / 44.1 kHz), or Hi-Res (up to 24-bit / 192 kHz) per your preference and connection
- **Automatic YouTube fallback** — If a track isn't on Qobuz, or all resolvers fail, playback falls back silently to the standard YouTube Music stream — no error, no skip
- **Hidden behind a toggle** — Disabled by default; opt-in from the Spotify integration settings

### Core Music Features
- Play any song or video from YouTube Music
- Background playback
- Personalized quick picks
- Library management
- Listen together with friends
- Download and cache songs for offline playback
- Search for songs, albums, artists, videos and playlists
- Live lyrics
- YouTube Music account login support
- Syncing of songs, artists, albums and playlists, from and to your account
- Skip silence
- Import playlists
- Audio normalization
- Adjust tempo/pitch
- Local playlist management
- Reorder songs in playlist or queue
- Home screen widget with playback controls
- Light / Dark / Black / Dynamic theme
- Sleep timer
- Material 3 design
- Discord Rich Presence
