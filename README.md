<div align="center">
  <p>
    <strong>🇺🇸 English</strong> | 
    <a href="./readme/README_ES.md">🇪🇸 Español</a> | 
    <a href="./readme/README_IT.md">🇮🇹 Italiano</a>
  </p>
</div>

# 🌲 Link.Me Clone - Advanced Link in Bio Platform

[![React](https://img.shields.io/badge/React-19.1-61dafb?logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178c6?logo=typescript)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-7.1-646cff?logo=vite)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4-38bdf8?logo=tailwindcss)](https://tailwindcss.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

A highly customizable, fast, and modern "Link in Bio" web application. It allows users to create profiles with multiple links, dynamic themes, background video integration, multimedia embeds, and monetization, all managed through simple JSON files.

🔗 **Demo:** [https://yordisc.github.io/link.me/](https://yordisc.github.io/link.me/)

---

## 🚀 Key Features

### ⚡ **Extreme Performance**

- **Lazy Loading + Code Splitting:** Heavy components (QR, Ads, Social Media) only load when needed.
- **Optimized Architecture:** Ultra-fast initial load.
- **PWA Enabled:** Works offline with Service Workers.
- **Lighthouse Perfect:** 100/100 performance score.

### 🎨 **Dynamic Theme System**

Powerful JSON-based system with 7 pre-built themes:

- **default** - Modern and clean base theme
- **pepsi** - Inspired by the Pepsi brand
- **7up** - Fresh and vibrant colors
- **polar** - Cold arctic tones
- **malta-polar** - Nostalgic warmth
- **solera** - Golden elegance
- **carorena** - Tropical design

**Functionalities:**

- Automatic Light/Dark mode
- Custom colors, shadows, and borders
- Backgrounds with custom CSS gradients
- Create your own themes without touching code

### 🎬 **Multimedia Backgrounds**

Native support for multiple formats as wallpaper:

- **Images:** JPG, PNG, WebP
- **Animated GIFs:** For dynamic backgrounds
- **MP4 Videos:** With automatic loop playback
- **CSS Gradients:** Custom gradient backgrounds

### 🧩 **Flexible Layouts**

#### **📋 List Layout**

Classic vertical design for traditional navigation.

#### **🎯 Smart Grid Layout**

Advanced grid system with auto-organization:

- **Rectangular Buttons:** Take up full width (2 columns).
- **Square Buttons:** Take up 1 individual column.
- **Normal Buttons (Smart Grouping):** If two normal buttons are consecutive, they stack vertically in one column to maintain symmetry with squares.
- **Responsive Design:** Adapts perfectly to any screen size.

### 🌟 **Smart Embeds**

Automatic platform detection system that decides the best way to display content:

#### **📺 Native Embeds (Iframe)**

Direct playback within the profile:

- **YouTube:** Standard videos, Shorts, and live streams
- **Spotify:** Songs, albums, and full playlists
- **TikTok:** Embedded videos with native player
- **Google Maps:** Embedded interactive maps
- **CodePen:** Live code previews (ideal for portfolios)
- **Google Drive:** PDF documents with integrated viewer

#### **🎴 Smart Cards (Secure Cards)**

For platforms that block iframes (CORS/X-Frame-Options), generates elegant cards with the brand's native style:

- **Instagram, LinkedIn, Twitter/X, GitHub (Repos), Letterboxd, Spotify (Profiles)**

### 🎵 **"Spotify Live" Widget (Real Time)**

Integration with the **Lanyard** API to show what you are listening to on Spotify LIVE via your Discord status:

**Active State (playing music):**

- Animated album art
- Song and artist name in real-time
- Synchronized progress bar
- Animated audio visualizer

**Inactive State (no playback):**

- Automatically transforms into a standard "Follow me on Spotify" button

**Required Configuration:**

- Discord account connected to Spotify
- Public Discord profile
- Discord User ID

### 🖼️ **Smart Image Viewer**

Buttons can open images in full screen without leaving the profile. Ideal for:

- **Payment QR Codes:** Binance Pay, Zelle, Bitcoin, PayPal
- **Certificates/Diplomas:** Show achievements in high resolution
- **Flyers/Promotions:** Quick visual information
- **Galleries:** Display work or products

**Features:**

- Zoom and smooth navigation
- Download button included (except for profile picture for privacy)
- Simple activation: add `#view` at the end of any image URL

### ☁️ **Smart Media Resolver (Cloud Manager)**

Link resolution engine allowing the use of cloud storage services directly as Avatar, Background, or Button Images without searching for direct links:

**Supported Platforms:**

- **Google Drive:** - **Images:** Automatically uses the HD thumbnail CDN (`lh3`) for instant loading and to avoid blocks.
  - **Videos:** Use the `#video` parameter at the end of the URL to force player mode.
- **pCloud, Dropbox, Reddit:** Direct media extraction.

### 🎭 **UI/UX Animations & Effects**

- **📜 Text Marquee:** Auto-scroll for long text.
- **🎠 Social Carousel:** Horizontal scroll for >4 icons.
- **✨ Smooth Transitions:** Optimized with Framer Motion.

### 🛡️ **ContentGuard™ - Anti-AdBlock System**

Advanced monetization protection system that detects ad blockers (uBlock Origin, AdGuard, AdBlock Plus) using multiple techniques (Local Trap, Network Trap, Cosmetic Trap).

### 💰 **Monetization System**

- Google AdSense Integration
- Optimized ad spaces with anti-block protection
- Floating sidebars for ads

### 🔐 **Security & Privacy**

- **AES Encryption:** Profile data in `sessionStorage` is encrypted.
- **No Invasive Tracking:** No personal data collection without consent.

---

## 🛠️ Tech Stack

- **React 19.1.1**
- **TypeScript 5.9.3**
- **Vite 7.1.7**
- **Tailwind CSS 3.4.18**
- **Framer Motion 12.23.24**
- **Zustand 5.0.8** (State Management)

---

## 📦 Installation & Local Usage

### **Prerequisites**

- **Node.js:** v18.0.0+
- **npm:** v9.0.0+

### **Steps**

1. **Clone the Repository**
   ```bash
   git clone [https://github.com/yordisc/link.me-source.git](https://github.com/yordisc/link.me-source.git)
   cd link.me
   ```
````

2.  **Install Dependencies**

    ```bash
    npm install
    ```

3.  **Start Development Server**

    ```bash
    npm run dev
    ```

4.  **Build for Production**

    ```bash
    npm run build
    ```

---

## ⚙️ Profile Configuration (JSON)

All content is managed via JSON files in `public/data/`.

### **Complete JSON Structure Example**

```json
{
  "profile": {
    "username": "jose",
    "displayName": "José Developer",
    "bio": "Frontend Dev | Creator 🚀",
    "avatarUrl": "[https://your-cdn.com/avatar.jpg](https://your-cdn.com/avatar.jpg)",
    "theme": "pepsi",
    "socialButtons": {
      "enabled": true,
      "draggable": true
    }
  },
  "links": [
    {
      "id": "portfolio",
      "type": "rectangular",
      "title": "🎨 My Portfolio",
      "url": "[https://myweb.com](https://myweb.com)",
      "visible": true
    }
  ]
}
```

For full documentation on button types (Square, Embeds, Smart Cards), please refer to the source code or the Spanish documentation for detailed examples.

---

## 🚀 Deployment

**GitHub Pages (Automated)**

```bash
npm run deploy
```

The project is pre-configured to deploy to GitHub Pages automatically.

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.

---

\<div align="center"\>
\<b\>Created with ☕ by \<a href="https://github.com/yordisc"\>Yordisc\</a\>\</b\>
\</div\>