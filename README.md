# 💍 Atif & Isma — Engagement Invitation & Event Guide Website

> **"IT'S HAPPENING."**  
> A modern, playful, internet-native digital engagement invitation and itinerary website for **Muhammad Atif & Ismasari**.

---

## ✨ Features

| Feature | Details |
|---|---|
| 🎨 **Design Aesthetic** | Gen Z Digital Scrapbook aesthetic — Polaroids, washi tape, stamps, stickers, and micro-interactions |
| 🌐 **Bilingual (EN / BM)** | Full English & Bahasa Melayu toggle with instant DOM updates and `localStorage` language memory |
| 📱 **Mobile-First & Responsive** | Custom mobile sticky navigation bar and desktop top navigation |
| ⏳ **Live Countdown** | Real-time countdown clock to the engagement ceremony (26 December 2026, 5:30 PM) |
| 📖 **How Did We Get Here?** | 6-part relationship timeline from Farah's IG story & MokNab to Timothy Café and getting engaged |
| 💑 **The Main Characters** | Interactive couple profiles for **Atif** (*The Isma Solution*) & **Isma** (*CEO of Always Right*) |
| 📸 **Receipts Gallery** | Polaroid photo gallery with candid handwritten annotations and photo popups |
| 🎵 **Spotify Music Player** | Floating audio soundtrack player featuring *"Bernaung"* by Feby Putri with direct Spotify link |
| 📋 **Ceremony Details** | Date, Time, Venue (**ONETWO KL**), Traditional Dress Code, and one-tap Google Maps & Waze links |
| 👗 **What Do I Wear?** | Dedicated dress code guide featuring **Team Atif** (*Butter Yellow*) and **Team Isma** (*Dusty Pink*) |
| 🕒 **Event Programme** | 13-stage tentative programme (*Atur Cara Majlis*) from 5:30 PM guest arrival to 10:00 PM conclusion |
| 🥚 **Interactive Easter Eggs** | Floating hearts canvas, secret stickers, "DO NOT CLICK ⚠️" modal, and the classic Konami code |
| ♿ **Accessibility** | Semantic HTML5 structure, ARIA live regions/modal attributes, and `prefers-reduced-motion` compliance |

---

## 🚀 Quick Start

1. **Open locally**: Double-click `index.html` or open in any local web server (e.g. Laragon, Live Server).
2. **Deploy to GitHub Pages**: Push to repository and enable GitHub Pages on the `main` branch root.
3. **Deploy to Netlify / Vercel**: Connect the repository or drag and drop the folder.

> ⚡ **Zero build tools required.** Pure HTML5, CSS3, and vanilla JavaScript.

---

## ✏️ Configuration & Customisation

### 1. Event Details & Backend Settings — `script.js`

Open [`script.js`](script.js) to configure the core event variables:

```js
const weddingConfig = {
  groom:       "Atif",
  bride:       "Ismasari",
  date:        "2026-12-26T17:30:00",   // ISO 8601 engagement datetime
  dateDisplay: "26 December 2026",      // Human-readable date
  timeDisplay: "5:30 PM — 10:00 PM",
  venue:       "ONETWO KL",
  address:     "3 Towers, 296, Jln Ampang, Kuala Ampang, 50450 Ampang, Wilayah Persekutuan Kuala Lumpur",
  mapsUrl:     "https://www.google.com/maps/dir/...",
  wazeUrl:     "https://waze.com/ul?ll=3.1609996,101.7418851&navigate=yes",
  musicUrl:    "assets/music/our-song.mp3",
  musicTitle:  "Bernaung",
  musicArtist: "Feby Putri",
  spotifyUrl:  "https://open.spotify.com/track/16Q9MOCDYgrgjEHx6Hx2rv",
  hashtag:     "#AtifIsmaForever",
  dressCode:   "Traditional Outfit",
};
```

---

### 2. Bilingual Support (i18n) — `script.js`

All text in the site is managed through the `translations` dictionary in [`script.js`](script.js):
- `translations.en`: English copy
- `translations.bm`: Bahasa Melayu copy

Elements in [`index.html`](index.html) use the `data-i18n="key"` attribute to automatically sync with the selected language.

```html
<h2 data-i18n="storyHeading">HOW DID WE GET HERE?</h2>
```

---

### 3. Timeline & Story Milestones — `index.html` & `script.js`

The story chronicles 6 key milestones:
1. **How We Know Us**: First IG stories connection (popcorn cart & matcha story).
2. **The First Meet**: MokNab Pantai Dalam.
3. **The Lepak Gang**: Atif, Isma, Bab & Farah.
4. **The "Oh No, I Like You" Era**: Panic, butterflies, overthinking, and unsent drafts *(Atif's POV)*.
5. **The First Date**: Timothy Café (pasta, coffee & tiramisu).
6. **The "We're Actually Getting Engaged" Era**: The love, stress, joy, and gratitude.

To edit text or add milestones, update the `.timeline-item` elements in [`index.html`](index.html) and their corresponding entries in `translations`.

---

### 4. Dress Code Colours & Themes — `index.html` & `style.css`

The dress code highlights two color palettes:
- **Team Atif**: Butter Yellow (`#FDF0A6` / soft pastel yellow & buttercream)
- **Team Isma**: Dusty Pink (`#D8A4A4` / soft pink, blush & mauve tones)
- **Theme**: Traditional Attire (Baju Kurung & Baju Melayu)

---

### 5. Programme / Tentative Schedule — `index.html`

The event schedule features a chronological list of 13 milestones:
- `5:30 PM`: Arrival of Guests & Isma's Family
- `5:45 PM`: Arrival of Atif's Family
- `6:00 PM`: Engagement Ceremony Begins (Hantaran Procession)
- `6:05 PM`: Recitation of Doa
- `6:10 PM`: Speech & Presentation of Intentions
- `6:15 PM`: Response by Bride's Family
- `6:20 PM`: Ring Ceremony (*Upacara Menyarungkan Cincin*) 💍
- `6:30 PM`: Photography Session 📸
- `6:45 PM`: Dinner 🍽️
- `7:15 PM`: Maghrib Prayer 🕌
- `7:45 PM`: Mingling & Casual Photos
- `9:30 PM`: Gift Handover (*Balas Hantaran*) 🎁
- `10:00 PM`: End of Ceremony ✨

---

### 6. Background Audio / Music Player

Audio files are stored in `assets/music/`:
- `our-song.mp3` & `our-song.m4a`
- Configured in `weddingConfig.musicUrl`
- Plays *"Bernaung"* by Feby Putri on guest interaction (starts muted/paused by default to comply with browser autoplay policies).

---

### 7. Optional Backend Integration (Google Sheets & Firebase)

For RSVP tracking or guestbook wishes, the site contains built-in hooks for:
- **Google Sheets**: Master spreadsheet for guest lists.
- **Firebase Firestore**: Real-time cloud database.

Credentials can be supplied in `weddingConfig.googleSheetsUrl` and `weddingConfig.firebaseConfig`. Full details are available in [`BACKEND-SETUP.md`](BACKEND-SETUP.md).

---

## 🥚 Easter Eggs

| Easter Egg | How to Trigger |
|---|---|
| 🎊 **Floating Hearts Canvas** | Click the ♥ heart button in the hero or footer, or double-click/tap any polaroid in the gallery |
| 👀 **Secret Sticker** | Click the ❤️ heart sticker in the scrapbook hero section 3 times |
| 💀 **"DO NOT CLICK ⚠️"** | Click the secret button at the bottom of the page to trigger the modal |
| 🕹️ **Konami Code** | Press `↑ ↑ ↓ ↓ ← → ← → B A` on your keyboard |

---

## 📁 File Structure

```text
/
├── index.html          ← Semantic markup, layouts, all sections & modal overlays
├── style.css           ← Design system tokens, scrapbook styles, animations & responsive layout
├── script.js           ← Configuration, audio player, countdown, i18n, easter eggs & interactions
├── BACKEND-SETUP.md    ← Optional Google Sheets & Firebase setup guide
├── README.md           ← Project documentation
└── assets/
    ├── images/         ← Photos, gallery memories, icons & avatars
    ├── music/          ← Wedding/engagement song audio files (.mp3, .m4a)
    └── icons/          ← Custom vector assets & icons
```

---

## 🎨 Design Tokens

Key styling tokens in [`style.css`](style.css):

```css
:root {
  --bg:           #FFFDF7;   /* Scrapbook warm paper background */
  --bg-card:      #FFFFFF;   /* Clean card base */
  --accent:       #E8533A;   /* Primary bold terracotta / red-orange */
  --accent2:      #F5C842;   /* Warm golden yellow accent */
  --text:         #1A1A1A;   /* Crisp dark heading & body text */
  --text-muted:   #666660;   /* Secondary descriptive text */
  --text-light:   #999990;   /* Muted captions & timestamps */
  --font-heading: 'Syne', sans-serif;
  --font-body:    'Plus Jakarta Sans', sans-serif;
  --font-hand:    'Caveat', cursive;
}
```

---

## 📱 Tested Breakpoints

- 320px (iPhone SE)
- 375px (iPhone 13 / 14 / 15 mini)
- 390px / 393px (iPhone 14 / 15 / 16)
- 430px (iPhone 14 / 15 Plus & Pro Max)
- 768px (iPad Mini / Portrait Tablets)
- 1024px (iPad Pro / Small Laptops)
- 1440px+ (Desktop Monitors)

---

## 💍 Atif & Isma

**26 December 2026 · ONETWO KL**  
*#AtifIsmaForever*
