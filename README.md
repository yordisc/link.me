![CI Status](https://img.shields.io/badge/Build-Passing-brightgreen?style=flathttps://github.com/yordisc/link.me-source/actions/workflows/ci.yml/badge.svglogo=github)

<div align="center">
  <strong>🇺🇸 English</strong> |
  <a href="./readme/README_ES.md">🇪🇸 Español</a> |
  <a href="./readme/README_IT.md">🇮🇹 Italiano</a>
</div>

<br />

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
- **Lazy Loading + Code Splitting:** Heavy components (QR, Ads, Socials) only load when needed.
- **Optimized Architecture:** Ultra-fast initial load.
- **PWA Enabled:** Works offline with Service Workers.
- **Lighthouse Perfect:** 100/100 performance score.

### 🎨 **Dynamic Theme System**
Powerful JSON-based system with 7 pre-built themes:
- **default** - Clean and modern base theme.
- **pepsi** - Inspired by the Pepsi brand.
- **7up** - Fresh and vibrant colors.
- **polar** - Cold arctic tones.
- **malta-polar** - Nostalgic warmth.
- **solera** - Golden elegance.
- **carorena** - Tropical beach design.

**Capabilities:**
- Automatic Light/Dark mode.
- Custom colors, shadows, and borders.
- Custom CSS gradient backgrounds.
- Create your own themes without touching the code.

### 🎬 **Multimedia Backgrounds**
Native support for multiple formats as wallpaper:
- **Images:** JPG, PNG, WebP.
- **Animated GIFs:** For dynamic backgrounds.
- **MP4 Videos:** With automatic loop playback.
- **CSS Gradients:** Custom gradient backgrounds.

### 🧩 **Flexible Layouts**

#### **📋 List Layout**
Classic vertical design for traditional navigation.

#### **🎯 Smart Grid Layout**
Advanced grid system with auto-organization:
- **Rectangular Buttons:** Take up full width (2 columns).
- **Square Buttons:** Take up 1 individual column.
- **Normal Buttons (Smart Grouping):** If there are two consecutive normal buttons, they stack vertically in one column to maintain symmetry with squares.
- **Responsive Design:** Perfectly adapts to any screen size.

### 🌟 **Smart Embeds**
Automatic platform detection system that decides the best way to display content:

#### **📺 Native Embeds (Iframe)**
Direct playback within the profile:
- **YouTube:** Standard videos, Shorts, and Live streams.
- **Spotify:** Songs, albums, and full playlists.
- **TikTok:** Embedded videos with native player.
- **Google Maps:** Embedded interactive maps.
- **CodePen:** Live code previews (ideal for portfolios).
- **Google Drive:** PDF documents with integrated viewer.

#### **🎴 Smart Cards (Secure Cards)**
For platforms that block iframes (CORS/X-Frame-Options), generates elegant cards with the native style of each brand:
- **Instagram, LinkedIn, Twitter/X, GitHub (Repos), Letterboxd, Spotify (Profiles).**

### 🎵 **"Spotify Live" Widget (Real-Time)**
Integration with the **Lanyard** API to show what you are listening to on Spotify LIVE via your Discord status:

**Active State (playing music):**
- Animated album art.
- Real-time song and artist name.
- Synchronized progress bar.
- Animated audio visualizer.

**Inactive State (not playing):**
- Automatically transforms into a standard "Follow me on Spotify" button.

**Required Setup:**
- Discord account connected with Spotify.
- Public Discord profile.
- Discord User ID.

### 🖼️ **Smart Image Viewer**
Buttons can open images in full screen without leaving the profile. Ideal for:
- **Payment QR Codes:** Binance Pay, Zelle, Bitcoin, PayPal.
- **Certificates/Diplomas:** Display high-resolution achievements.
- **Flyers/Promotions:** Quick visual information.
- **Galleries:** Showcase work or products.

**Features:**
- Zoom and smooth navigation.
- Download button included (except for profile picture for privacy).
- Simple activation: add `#view` to the end of any image URL.

### ☁️ **Smart Media Resolver (Cloud Manager)**
Link resolution engine that allows using cloud storage services directly as Avatar, Background, or Button Images without searching for direct links:

**Supported Platforms:**
- **Google Drive:**
  - **Images:** Automatically uses the HD thumbnail CDN (`lh3`) for instant loading and to avoid blocks.
  - **Videos:** Use the `#video` parameter at the end of the URL to force player mode.
- **pCloud, Dropbox, Reddit:** Direct media extraction.

**Advantages:**
- Automatic file type detection (image/video).
- No need to manually generate direct download links.
- Automatic loading optimization.

### 🎭 **Animations & UI/UX Effects**

#### **📜 Text Marquee (Auto-Scroll)**
If a button's text is too long to fit the available space, a smooth infinite scrolling animation automatically activates to make it fully readable.

#### **🎠 Social Media Carousel**
When there are more than 4 social icons, the bar automatically converts into a sliding ribbon with smooth horizontal scroll.

#### **✨ Fluid Transitions**
- Optimized animations with Framer Motion.
- Elegant hover effects.
- Micro-interactions that enhance the experience.

### 🔀 **Drag & Drop (Optional)**
Drag and drop functionality to:
- Reorder links in real-time.
- Rearrange social buttons.
- Position the "Join" (Subscribe) button.
- Changes persist during the session.

### 🛡️ **ContentGuard™ - Anti-AdBlock System**
Advanced monetization protection system that detects ad blockers (uBlock Origin, AdGuard, AdBlock Plus) using multiple techniques:

**Detection Methods:**
1. **Local Bait Trap:** Attempts to load typically blocked files (`ads.js`, `prebid.js`).
2. **Network Trap:** Verifies connection with real ad servers.
3. **Cosmetic Trap (DOM):** Detects if elements with classes like `.adsbox` are hidden by the browser.

**Features:**
- Obfuscated code to avoid detection by filter lists.
- Protected component and variable names.
- Spaces prepared for Google AdSense with security validation.

*⚠️ Note: In development mode (`npm run dev`), blocking may be disabled to facilitate programming.*

### 💰 **Monetization System**
- Google AdSense integration.
- Optimized ad spaces.
- Anti-block protection included.
- Floating ad sidebars.

### 📱 **Mobile First Design**
- Responsive design that **automatically hides "boxes/cards" on mobile** for an immersive full-screen experience.
- Touch optimization for mobile navigation.
- Adaptive interface according to the device.
- Smooth transitions between breakpoints.

### 🔐 **Security & Privacy**
- **AES Encryption:** Profile data saved in `sessionStorage` is encrypted with CryptoJS to prevent casual reading or modification from the console.
- **No Invasive Tracking:** We do not collect personal data without consent.
- **Sensitive Data Protection:** TypeScript type system for delicate information.

### 📍 **Flexible Social Positioning**
Total control over where your social icons appear:
- **`top`**: In the profile card, under the bio.
- **`bottom`**: At the end of the link list, with a visual separator.
- **`both`**: In both places (useful for very long profiles).

### 🔗 **Smart Interactive Buttons**
Three types of buttons with unique features:
- **Normal:** Standard button with icon and text.
- **Square:** Square button with background image.
- **Rectangular:** Wide banner-style button with featured image.

---

## 🛠️ Technologies Used

### **Core Framework**
- **React 19.1.1** - UI Library with latest features.
- **TypeScript 5.9.3** - Robust static typing.
- **Vite 7.1.7** - Next-generation build tool.
- **React Router DOM 7.9.5** - Dynamic routing (`/:username`).

### **Styles & Animations**
- **Tailwind CSS 3.4.18** - Utility-first CSS framework.
- **Styled Components 6.1.19** - CSS-in-JS for theming.
- **Framer Motion 12.23.24** - Fluid animation library.
- **PostCSS 8.5.6** + **Autoprefixer 10.4.21** - CSS processing.

### 🕹️ Gamification & Easter Eggs
The platform includes hidden or activatable interactive experiences:

#### **🏃 Pepsiman Runner**
An "Endless Runner" style game integrated directly into the application.
- Custom components (Obstacles, Game Over screen).
- Seamless integration with the visual theme.

#### **💻 Terminal Mode**
An interactive command-line console (`src/components/Games/Terminal`) for advanced users or as a backend developer portfolio.
- Support for custom commands.
- Text-based navigation.

### **Core Utilities**
- **@dnd-kit (core 6.3.1 + sortable 10.0.0)** - Complete Drag & Drop system.
- **React Hook Form 7.66.0** + **Yup 1.7.1** - Form validation.
- **Zustand 5.0.8** - Lightweight state management.
- **date-fns 4.1.0** - Modern date manipulation.

### **Special Features**
- **react-qr-code 2.0.18** - QR code generation.
- **crypto-js 4.2.0** - AES encryption for local data.
- **idb 8.0.3** - Modern IndexedDB wrapper.
- **react-icons 5.5.0** - Extensive icon library.
- **lucide-react 0.552.0** - Additional optimized icons.

### **Analytics & Tracking**
- **react-ga4 2.1.0** - Google Analytics 4 integration.

### **Dev Tools**
- **Vite Plugin PWA 1.1.0** - Automatic PWA configuration.
- **Vitest 4.0.8** - Ultra-fast testing framework.
- **Storybook 10.0.5** - Isolated component development.
- **ESLint 9.36.0** + **Prettier 3.6.2** - Linting and formatting.
- **TypeScript ESLint 8.45.0** - TS specific rules.
- **gh-pages 6.3.0** - Automated deployment.

---

## 📦 Installation & Local Usage

### **Prerequisites**
- **Node.js:** v18.0.0 or higher.
- **npm:** v9.0.0 or higher (or yarn/pnpm equivalent).
- **Git:** To clone the repository.

### **Installation Steps**

#### **1. Clone the Repository (Private)**
```bash
git clone [https://github.com/yordisc/link.me-source.git](https://github.com/yordisc/link.me-source.git)
cd link.me
````

#### **2. Install Dependencies**

```bash
npm install
```

#### **3. Start Development Server**

```bash
npm run dev
```

Visit **`http://localhost:5173/`** in your browser.

#### **4. Build for Production**

```bash
npm run build
```

Compiled files will be in the `dist/` folder.

#### **5. Production Preview**

```bash
npm run preview
```

-----

## ⚙️ Profile Configuration (JSON)

All content is managed via JSON files in the `public/data/` folder.

### **Create Your Profile**

Create a file with your username: `public/data/jose.json`

### **Full JSON Structure**

```json
{
  "profile": {
    "username": "jose",
    "displayName": "José Developer",
    "bio": "Frontend Dev | Creator | Tech Enthusiast 🚀",
    "avatarUrl": "[https://your-cdn.com/avatar.jpg](https://your-cdn.com/avatar.jpg)",
    "avatarImages": [
      {
        "id": "main",
        "url": "[https://your-cdn.com/avatar.jpg](https://your-cdn.com/avatar.jpg)",
        "alt": "Main Profile"
      },
      {
        "id": "fun",
        "url": "[https://your-cdn.com/avatar-fun.jpg](https://your-cdn.com/avatar-fun.jpg)",
        "alt": "Fun Mode"
      }
    ],
    "theme": "pepsi",
    "settings": {
      "backgroundImage": "/videos/background.mp4",
      "hideThemeButton": false
    },
    "socialButtons": {
      "enabled": true,
      "draggable": true
    },
    "joinButton": {
      "enabled": true,
      "text": "Subscribe",
      "url": "[https://newsletter.com](https://newsletter.com)",
      "backgroundColor": "#000000",
      "textColor": "#FFFFFF"
    }
  },
  "links": [
    {
      "id": "portfolio",
      "type": "rectangular",
      "title": "🎨 My Portfolio",
      "url": "[https://myweb.com](https://myweb.com)",
      "visible": true,
      "icon": "linkcustom"
    },
    {
      "id": "instagram",
      "type": "normal",
      "title": "Instagram",
      "url": "[https://instagram.com/your_user](https://instagram.com/your_user)",
      "visible": true,
      "icon": "instagram"
    }
  ]
}
```

-----

## 🔗 Link Types & Examples

### **1. Normal Button (Standard)**

Standard button with icon and text. Ideal for general links.

```json
{
  "id": "portfolio",
  "type": "normal",
  "title": "My Web Portfolio",
  "url": "[https://myweb.com](https://myweb.com)",
  "icon": "globe",
  "visible": true,
  "styles": {
    "backgroundColor": "#3b82f6",
    "color": "white"
  }
}
```

**Available Icons:** `instagram`, `twitter`, `facebook`, `linkedin`, `github`, `youtube`, `tiktok`, `spotify`, `globe`, `mail`, `phone`, `linkcustom`, etc.

-----

### **2. Square Button**

Compact button with background image. Perfect for grid-like layouts.

```json
{
  "id": "project1",
  "type": "square",
  "title": "E-commerce Project",
  "url": "[https://project.com](https://project.com)",
  "imageUrl": "[https://cdn.com/project-thumbnail.jpg](https://cdn.com/project-thumbnail.jpg)",
  "visible": true
}
```

-----

### **3. Rectangular Button (Banner)**

Wide banner-style button with featured image. Ideal for highlighted content.

```json
{
  "id": "featured",
  "type": "rectangular",
  "title": "🚀 Featured Project 2024",
  "url": "[https://big-project.com](https://big-project.com)",
  "imageUrl": "[https://cdn.com/banner-project.jpg](https://cdn.com/banner-project.jpg)",
  "visible": true
}
```

-----

### **4. YouTube Embed**

Embed videos, shorts, or live streams directly into your profile.

```json
{
  "id": "video-tutorial",
  "type": "embed",
  "provider": "youtube",
  "url": "[https://youtube.com/watch?v=VIDEO_ID](https://youtube.com/watch?v=VIDEO_ID)",
  "shape": "rectangular",
  "visible": true
}
```

**Supported Formats:**

  - Videos: `https://youtube.com/watch?v=VIDEO_ID`
  - Shorts: `https://youtube.com/shorts/VIDEO_ID`
  - Lives: `https://youtube.com/live/VIDEO_ID`

-----

### **5. Spotify Embed**

Embed songs, albums, or playlists with native player.

```json
{
  "id": "my-playlist",
  "type": "embed",
  "provider": "spotify",
  "url": "[https://open.spotify.com/playlist/37i9dQZF1DXcBWIGoYBM5M](https://open.spotify.com/playlist/37i9dQZF1DXcBWIGoYBM5M)",
  "shape": "rectangular",
  "visible": true
}
```

**Supported Types:**

  - Songs: `https://open.spotify.com/track/TRACK_ID`
  - Albums: `https://open.spotify.com/album/ALBUM_ID`
  - Playlists: `https://open.spotify.com/playlist/PLAYLIST_ID`

-----

### **6. Spotify Live Widget (Real-Time)**

Shows what you are listening to LIVE via Lanyard + Discord.

```json
{
  "id": "spotify-now-playing",
  "type": "embed",
  "provider": "spotify-bio",
  "title": "🎵 Listening right now",
  "url": "[https://open.spotify.com/user/TU_USUARIO_SPOTIFY](https://open.spotify.com/user/TU_USUARIO_SPOTIFY)",
  "originalUrl": "YOUR_DISCORD_USER_ID",
  "shape": "rectangular",
  "visible": true
}
```

**Required Setup:**

1.  Connect Spotify to your Discord account.
2.  Keep your Discord profile public.
3.  Get your Discord User ID.
4.  Replace `YOUR_DISCORD_USER_ID` with your actual ID.

**How to get your Discord User ID:**

1.  Enable Developer Mode in Discord (Settings → Advanced).
2.  Right-click on your profile → Copy ID.

-----

### **7. Image/QR Viewer with https://www.google.com/search?q=%23view**

Opens images in full screen when clicked. Perfect for payment QR codes.

```json
{
  "id": "qr-binance",
  "type": "square",
  "title": "💳 Pay with Binance",
  "imageUrl": "[https://unsplash.com/crypto-preview.jpg](https://unsplash.com/crypto-preview.jpg)",
  "url": "[https://drive.google.com/file/d/YOUR_QR_ID/view?usp=sharing#view](https://drive.google.com/file/d/YOUR_QR_ID/view?usp=sharing#view)",
  "visible": true
}
```

**How it works:**

  - **`imageUrl`**: Beautiful cover image for the button (decorative).
  - **`url`** + **`#view`**: Actual image that will open in the viewer (functional).

**Use Cases:**

  - Binance Pay, Zelle, Bitcoin QR codes.
  - Certificates or diplomas.
  - Event flyers.
  - Restaurant menus.

-----

### **8. Videos from Google Drive**

Use videos stored in Google Drive directly.

```json
{
  "id": "video-demo",
  "type": "rectangular",
  "title": "📹 Project Demo Video",
  "url": "#",
  "imageUrl": "[https://drive.google.com/file/d/VIDEO_ID/view?usp=sharing#video](https://drive.google.com/file/d/VIDEO_ID/view?usp=sharing#video)",
  "visible": true
}
```

**Important:** Add `#video` to the end of the Google Drive URL to force player mode.

-----

### **9. TikTok Embed**

Embed TikTok videos with native player.

```json
{
  "id": "tiktok-viral",
  "type": "embed",
  "provider": "tiktok",
  "url": "[https://tiktok.com/@user/video/1234567890](https://tiktok.com/@user/video/1234567890)",
  "shape": "square",
  "visible": true
}
```

-----

### **10. Google Maps Embed**

Show your location or important places.

```json
{
  "id": "my-office",
  "type": "embed",
  "provider": "googlemaps",
  "url": "[https://maps.google.com/?q=Latitude,Longitude](https://maps.google.com/?q=Latitude,Longitude)",
  "shape": "rectangular",
  "visible": true
}
```

-----

### **11. CodePen Embed**

Perfect for developers: show your live code.

```json
{
  "id": "demo-code",
  "type": "embed",
  "provider": "codepen",
  "url": "[https://codepen.io/user/pen/PEN_ID](https://codepen.io/user/pen/PEN_ID)",
  "shape": "rectangular",
  "visible": true
}
```

-----

### **12. Smart Cards (Instagram, LinkedIn, Twitter, GitHub)**

For platforms that block iframes, an elegant card with preview is generated.

```json
{
  "id": "linkedin-profile",
  "type": "embed",
  "provider": "linkedin",
  "url": "[https://linkedin.com/in/your-profile](https://linkedin.com/in/your-profile)",
  "shape": "normal",
  "visible": true
}
```

**Platforms with Smart Cards:**

  - Instagram
  - LinkedIn
  - Twitter (X)
  - GitHub (repositories)
  - Letterboxd

-----

## 🎨 Theme System

### **Included Themes**

| Theme | ID | Description |
|------|-----|-------------|
| **Default** | `default` | Modern and clean base theme |
| **Pepsi** | `pepsi` | Blue and red, inspired by the brand |
| **7UP** | `7up` | Fresh and vibrant lemon green |
| **Polar** | `polar` | Cold arctic tones |
| **Malta Polar** | `malta-polar` | Nostalgic golden warmth |
| **Solera** | `solera` | Premium golden elegance |
| **Carorena** | `carorena` | Tropical beach design |

### **Apply a Theme**

In your profile JSON file:

```json
{
  "profile": {
    "theme": "pepsi"
  }
}
```

### **Create Your Own Theme**

Create a file at `public/data/themes/my-theme.json`:

```json
{
  "id": "my-custom-theme",
  "name": "My Custom Theme",
  "structure": {
    "layout": "grid",
    "avatarShape": "circle",
    "cardStyle": "elevated"
  },
  "light": {
    "colors": {
      "primary": "#6366f1",
      "secondary": "#8b5cf6",
      "accent": "#ec4899",
      "background": "#ffffff",
      "text": "#1f2937",
      "textSecondary": "#6b7280",
      "textMuted": "#9ca3af",
      "border": "#e5e7eb"
    },
    "backgrounds": {
      "page": "linear-gradient(135deg, #667eea 0%, #764ba2 100%)",
      "card": "#ffffff"
    },
    "shadows": {
      "card": "0 4px 6px -1px rgb(0 0 0 / 0.1)",
      "cardHover": "0 20px 25px -5px rgb(0 0 0 / 0.1)"
    },
    "borders": {
      "card": "1px solid #e5e7eb",
      "button": "1px solid #d1d5db"
    }
  },
  "dark": {
    "colors": {
      "primary": "#818cf8",
      "secondary": "#a78bfa",
      "accent": "#f472b6",
      "background": "#111827",
      "text": "#f9fafb",
      "textSecondary": "#d1d5db",
      "textMuted": "#9ca3af",
      "border": "#374151"
    },
    "backgrounds": {
      "page": "linear-gradient(135deg, #1e3a8a 0%, #7c3aed 100%)",
      "card": "#1f2937"
    },
    "shadows": {
      "card": "0 4px 6px -1px rgb(0 0 0 / 0.3)",
      "cardHover": "0 20px 25px -5px rgb(0 0 0 / 0.3)"
    },
    "borders": {
      "card": "1px solid #374151",
      "button": "1px solid #4b5563"
    }
  }
}
```

-----

## 📍 Social Media Configuration

Social icons are automatically generated from your main `links` list when the `icon` matches a known social network (instagram, twitter, github, etc.) and you have `socialButtons.enabled: true`.

```json
"profile": {
  "socialButtons": {
    "enabled": true,
    "draggable": true
  }
}
```

**`style` Options:**

  - **`circles`**: Circular icons (default).
  - **`squares`**: Square icons.
  - **`rounded`**: Icons with rounded borders.

**`position` Options:**

  - **`top`**: Appears in the profile card, under the bio.
  - **`bottom`**: At the end of all links, with a separator.
  - **`both`**: In both locations (useful for long profiles).

**`draggable`:**

  - **`true`**: Allows reordering icons with drag & drop.
  - **`false`**: Fixed order.

### **Automatic Carousel**

When you configure **more than 4 social icons**, the bar automatically converts into a **sliding ribbon** with smooth horizontal scroll.

-----

## 📂 Project Structure

```bash
link.me/
│
├── public/
│   ├── data/
│   │   ├── themes/       # JSON Themes (default, etc.)
│   │   ├── yordisc.json         # User profiles
│   │   ├── jose.json
│   │   └── maria.json
│   └── backgrounds/             # Multimedia resources
│
├── src/
│   ├── components/
│   │   ├── ads/              # Monetization system
│   │   │   ├── AdSenseUnit.tsx
│   │   │   ├── ContentGuard.tsx # Anti-AdBlock System
│   │   │   └── FloatingAdSidebars.tsx
│   │   ├── avatar/              # Avatar and viewer
│   │   │   ├── AvatarViewer.tsx
│   │   │   └── EnhancedAvatar.tsx
│   │   ├── buttons/             # Button components
│   │   │   ├── NormalButton.tsx
│   │   │   ├── SquareButton.tsx
│   │   │   ├── RectangularButton.tsx
│   │   │   ├── SocialButtons.tsx
│   │   │   ├── ...
│   │   │   └── Terminal/        # Interactive Console
│   │   ├── widgets/             # External Widgets
│   │   │   └── SpotifyWidget.tsx
│   │   └── Layout/              # Base Structure
│   │
│   ├── contexts/   # State Management (ThemeContext)
│   ├── hooks/      # Custom Hooks (useLanyard, etc)
│   ├── utils/      # Utilities (crypto.ts)
│   └── types/      # TypeScript Definitions
│
├── package.json
├── vite.config.ts
└── tailwind.config.js
```

-----

## 🚀 Deployment

### **GitHub Pages (Automated)**

The project is pre-configured to deploy to GitHub Pages with a single command:

```bash
npm run deploy
```

**Automated Process:**

1.  Compiles the project (`npm run build`).
2.  Uploads the `dist/` folder to the `gh-pages` branch.
3.  GitHub Pages publishes automatically.

**Your site will be available at:**

```
[https://yordisc.github.io/link.me/](https://yordisc.github.io/link.me/)
```

**Configuration in `package.json`:**

```json
{
  "homepage": "[https://yordisc.github.io/link.me](https://yordisc.github.io/link.me)",
  "scripts": {
    "predeploy": "npm run build",
    "deploy": "gh-pages -d dist --repo [https://ghp_TOKEN@github.com/yordisc/link.me.git](https://ghp_TOKEN@github.com/yordisc/link.me.git)"
  }
}
```

-----

## 🛡️ Control de Calidad y Testing

Este proyecto cuenta con un pipeline de Integración Continua (CI) automatizado con GitHub Actions. Con cada actualización, se ejecutan auditorías de rendimiento, pruebas de lógica y simulaciones de usuario.

Los reportes detallados del último despliegue están disponibles públicamente:

| Auditoría | Herramienta | Reporte en Vivo |
| :--- | :---: | :--- |
| **Performance & SEO** | ![Lighthouse](https://img.shields.io/badge/-Lighthouse-F44B21?style=flat-square&logo=lighthouse&logoColor=white) | [🚀 **Ver Reporte HTML**](https://yordisc.github.io/link.me/reports/performance/index.html) |
| **Tests Unitarios** | ![Vitest](https://img.shields.io/badge/-Vitest-729B1B?style=flat-square&logo=vitest&logoColor=white) | [🧪 **Ver Resultados JSON**](https://yordisc.github.io/link.me/reports/unit/vitest-results.json) |
| **Tests E2E** | ![Cypress](https://img.shields.io/badge/-Cypress-17202C?style=flat-square&logo=cypress&logoColor=white) | [🤖 **Ver Datos Raw**](https://yordisc.github.io/link.me/reports/e2e/cypress-summary.json) |

> ℹ️ *Nota: Estos reportes se regeneran automáticamente en la carpeta `/reports` de la rama `gh-pages` con cada deploy exitoso.*

### **Style Guides**

  - ✅ Use **TypeScript** for all new code.
  - ✅ Follow the configured **ESLint** rules.
  - ✅ Write **unit tests** for critical features.
  - ✅ Document complex functions with **JSDoc**.
  - ✅ Use **semantic commits**:
      - `feat:` New feature
      - `fix:` Bug fix
      - `docs:` Documentation changes
      - `style:` Formatting, missing semicolons, etc.
      - `refactor:` Code refactoring
      - `test:` Adding tests
      - `chore:` Updating dependencies, etc.

### **Report Bugs**

If you find a bug, please [open an issue](https://github.com/yordisc/link.me/issues) with:

  - Clear description of the problem.
  - Steps to reproduce it.
  - Expected vs. actual behavior.
  - Screenshots if possible.
  - Browser/OS information.

-----

## 📄 License

Distributed under the **MIT License**. See `LICENSE` file for more information.

This means you can:

  - ✅ Use commercially
  - ✅ Modify the code
  - ✅ Distribute
  - ✅ Private use

Under the conditions of:

  - 📋 Including the copyright notice
  - 📋 Including the MIT license

-----

## 🙏 Acknowledgments

This project would not be possible without these amazing tools and communities:

  - **[React Team](https://react.dev/)** - For the best UI library.
  - **[Vite](https://vitejs.dev/)** - Ultra-fast build tool.
  - **[Tailwind CSS](https://tailwindcss.com/)** - CSS framework that speeds up development.
  - **[React Icons](https://react-icons.github.io/)** - Thousands of icons ready to use.
  - **[Framer Motion](https://www.framer.com/motion/)** - Smooth and easy animations.
  - **[Lanyard API](https://github.com/Phineas/lanyard)** - Real-time Discord status.
  - **[Unsplash](https://unsplash.com/)** - High-quality free images.
  - **Open Source Community** - For sharing knowledge.

-----

## 📞 Contact and Support

### **Creator**

👨‍💻 **Yordisc**

  - GitHub: [@yordisc](https://github.com/yordisc)
  - Project: [link.me](https://github.com/yordisc/link.me)

### **Get Help**

  - 📖 [Full Documentation](https://www.google.com/search?q=%23)
  - 💬 [Discussions](https://github.com/yordisc/link.me/discussions)
  - 🐛 [Report Bug](https://github.com/yordisc/link.me/issues)
  - 💡 [Request Feature](https://github.com/yordisc/link.me/issues/new?labels=enhancement)

-----

\<div align="center"\>

## ⭐ If you like the project, don't forget to give it a star ⭐

[](https://github.com/yordisc/link.me/stargazers)
[](https://github.com/yordisc/link.me/network/members)

-----

**Made with ☕ by [Yordisc](https://github.com/yordisc)**

*"One link at a time, building your perfect digital presence"*

\</div\>