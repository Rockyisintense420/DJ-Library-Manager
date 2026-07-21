# DJ Library Manager — Design Doc

## Overview
AI-powered library manager for DJs. Scans a local music collection, tags tracks
with useful metadata, and organizes the library so it's gig-ready.

## Goals
- Scan a folder (or set of folders) of audio files and build a library index.
- Auto-tag tracks with metadata relevant to DJs (BPM, key, genre, energy, etc.).
- Detect duplicates and low-quality files.
- Organize/export the library into a structure usable by DJ software
  (e.g. Rekordbox, Serato, Traktor).

## Non-Goals (for now)
- Streaming/purchasing music.
- Live performance/mixing features.

## Core Features
1. **Library Scan** — walk a directory tree, find audio files, extract existing
   tags (ID3, etc.).
2. **AI Tagging** — analyze audio to fill in missing metadata (BPM, musical
   key, genre, mood/energy) where tags are missing or unreliable.
3. **Organization** — rename/move files or generate playlists based on
   configurable rules (by genre, BPM range, key, etc.).
4. **Duplicate Detection** — flag duplicate or near-duplicate tracks.
5. **Export** — output formats compatible with common DJ software.

## Tech Stack
- **Language:** Python (per `.gitignore`)
- Audio analysis library: TBD (e.g. `librosa`, `essentia`)
- Metadata handling: TBD (e.g. `mutagen`)
- CLI vs GUI: TBD

## Open Questions
- Which DJ software should export support target first?
- Local-only processing, or allow cloud/AI API calls for tagging?
- CLI tool, desktop GUI, or both?

## Status
Early planning stage — no code yet. This doc is a living draft; update as
decisions are made.
