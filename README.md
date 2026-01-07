# SmarterGerman Widgets

Interactive learning widgets for SmarterGerman courses.

## Widgets

### Karaoke Player (`/karaoke/`)
Synced lyrics player with German/English translations.

**Usage:**
```
https://[username].github.io/smartergerman-widgets/karaoke/?song=toeff-toeff
```

**Current songs:** 8 A1 songs (will grow to 50+)

| Parameter | Song |
|-----------|------|
| `toeff-toeff` | Töff Töff (L04) |
| `bescheidenheit` | Bescheidenheit ist eine Zier (L08) |
| `deswegen` | Deswegen bin ich ja da (L09) |
| `fix-und-foxi` | Fix und Foxi (L10) |
| `ich-sehe-was` | Ich sehe was (L11) |
| `kann-ich-ihnen-helfen` | Kann Ich Ihnen Helfen? (L12) |
| `hunde` | Hunde Kann Er Nicht Leiden (L13) |
| `es-regnet` | Es Regnet, Gott Segnet (L14) |

### Article Trainer (`/article-trainer/`)
Practice der/die/das with noun ending patterns.

## Embedding in LifterLMS

```html
<iframe
  src="https://[username].github.io/smartergerman-widgets/karaoke/?song=toeff-toeff"
  width="100%"
  height="700"
  frameborder="0">
</iframe>
```

## Adding Songs to Karaoke Player

Edit `karaoke/index.html`, add to the `songs` object:

```javascript
'song-key': {
  title: 'Song Title',
  lesson: 'A1 Lesson XX',
  audio: 'https://smartergerman.com/wp-content/uploads/2026/01/filename.m4a',
  lyrics: [
    [0.0, "German text", "English translation"],
    [5.5, "Next line", "Translation"],
  ]
}
```

Lyrics format: `[timestamp_seconds, "German", "English"]`

## Server Backup

For emergency fallback, copy widgets to:
```
smartergerman.com/widgets/karaoke/index.html
smartergerman.com/widgets/article-trainer/index.html
```
