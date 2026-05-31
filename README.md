# Echo Music Library

Private Android music-library release assets for the Echo offline music player.

## Release assets

MP3 files are published as GitHub Release assets, not committed to this repository.
The Android app reads song metadata from Firestore and streams/downloads from each song document's `audioUrl`.

Current release tag: `music-v1`

## Firestore metadata

Prepared metadata lives in `manifests/`:

- `firestore-songs.music-v1.json`: app-shaped song records
- `firestore-songs.music-v1.csv`: spreadsheet-friendly review file
- `firestore-rest-documents.music-v1.json`: Firestore REST-style document payloads

Each song document uses the SHA-256 MP3 hash as `fileHash` and should use that same value as the Firestore document ID.
