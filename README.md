# Teacher Toolkit ΕΠΑΛ

Offline εκπαιδευτικό toolkit για καθηγητές/καθηγήτριες ΕΠΑΛ.

## Modules

- 🎮 Impostor
- 🃏 Flashcards
- ❓ Quiz
- 🎡 Random Wheel
- 📚 Database Manager
- ⚙️ Settings

Όλα τα modules χρησιμοποιούν τις ίδιες βάσεις λέξεων.

## GitHub Pages setup

Upload **the contents of this folder** to a GitHub repository, not the ZIP itself.

Expected structure:

```txt
teacher-toolkit-epal/
├── index.html
├── manifest.json
├── sw.js
├── css/
│   └── style.css
├── js/
│   ├── app.js
│   └── storage.js
├── data/
│   ├── anatomia.json
│   └── ygieini.json
└── assets/
    └── icon.svg
```

Then enable GitHub Pages:

1. Repository → Settings
2. Pages
3. Source: Deploy from a branch
4. Branch: main
5. Folder: `/ (root)`
6. Save

## Auto-save

The app saves databases, settings and statistics in the browser using `localStorage`.

This means:

- Data is saved automatically on the same browser/device.
- Data is **not** uploaded to GitHub.
- Different computers/browsers have different local data.
- To move data to another device, use **Export** and then **Import**.

## Lesson packs

The app supports `.epack` / `.json` imports with this structure:

```json
{
  "app": "Teacher Toolkit ΕΠΑΛ",
  "version": 1,
  "databases": [
    {
      "subject": "Ανατομία",
      "name": "Ανατομία - Πακέτο",
      "categories": [
        {
          "name": "Όργανα",
          "words": [
            {
              "term": "Καρδιά",
              "hint": "Μυώδες όργανο που αντλεί αίμα.",
              "definition": "Μυώδες όργανο του κυκλοφορικού συστήματος.",
              "quiz": "Σε ποιο σύστημα ανήκει;"
            }
          ]
        }
      ]
    }
  ]
}
```

## PWA

The project includes:

- `manifest.json`
- `sw.js`
- `assets/icon.svg`

When hosted through GitHub Pages, supported browsers can install it as an app and use it offline after the first visit.
