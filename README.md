# 🏗️ ESTRUCTURA 2K26 — V3 Cinematic Edition
### Mobile-First · Ultra-Premium · Production Ready
**Nirmaan Society · Civil Engineering · DCRUST Murthal**

---

## 🚀 What's New in V3

### Mobile-First Overhaul
- **Touch-optimized** — larger tap targets, no hover-only features, mobile scroll smooth
- **`-webkit-tap-highlight-color: transparent`** — no flash on tap
- **Viewport-fit: cover** — fills notch/island on iPhone
- **`100svh`** — hero fills exactly the phone screen (no URL-bar issues)
- **Barlow Condensed Italic** — cinematic festival font, loads fast
- **Reduced particle count** on mobile (30 vs 60 on desktop) for performance
- **Canvas disabled** on ultra-low-end devices (≤2 CPU cores)

### Design Upgrade
- **Cinematic amber gradient hero** with animated scroll line
- **Hollow stroke title** — "CTURA" in amber outline, "ESTRU" solid white
- **Bento gallery mosaic** — spans for visual hierarchy on all sizes
- **Animated preloader** — 10 characters drop in one-by-one with perspective
- **Glowing top-border** on countdown strip
- **Amber fire gradient button** with inset highlight
- **Full-width mobile menu** with staggered link reveal

---

## 📁 Structure

```
estructura-v3/
├── index.html          ← Complete, semantic HTML
├── css/style.css       ← Mobile-first CSS (~1000 lines)
├── js/app.js           ← All JS, touch-optimized
├── data/config.js      ← 🔑 Edit ALL content here
├── images/gallery/     ← Drop real photos here
└── README.md
```

---

## 📱 Mobile Breakpoints

| Width        | Layout                       |
|---|---|
| < 540px      | Single column, full-width    |
| 540–767px    | 2-column events + stats      |
| 768–899px    | 4-col gallery, 2-col team    |
| 900–1199px   | Desktop nav, 2-col layouts   |
| 1200px+      | Full desktop, sticky sidebar |

---

## ✏️ Edit Content

**One file: `data/config.js`**

```js
festDate:        "2026-05-15T09:00:00", // Changes countdown
festDateDisplay: "15 May 2026",
venue:           "MV Block, DCRUST Murthal",
registrationURL: "https://forms.gle/YOUR_LINK",
lastRegDate:     "10 May 2026",
```

---

## 🖼️ Add Real Photos

Place photos in `images/gallery/`, then in `js/app.js` find `initGallery()` and change each cell:

```js
cell.innerHTML = `
  <img src="images/gallery/photo${i+1}.jpg" alt="${p.l}" loading="lazy"
       style="width:100%;height:100%;object-fit:cover;border-radius:inherit;">
`;
```

---

## 🌐 Deploy

### Netlify (Fastest)
1. Drag `estructura-v3/` folder to [netlify.com](https://netlify.com)
2. Done. Live in 20 seconds.

### GitHub Pages
1. Upload to repo → Settings → Pages → Branch: main
2. Live at `username.github.io/repo`

### Vercel
```bash
npx vercel --yes
```

---

*V3 · Made by Nikhil Sain · ESTRUCTURA 2K26 · Nirmaan Society · DCRUST Murthal*
