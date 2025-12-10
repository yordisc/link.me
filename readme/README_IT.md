![CI Status](https://github.com/yordisc/link.me-source/actions/workflows/ci.yml/badge.svg)

<div align="center">
  <a href="../README.md">🇺🇸 English</a> |
  <a href="./README_ES.md">🇪🇸 Español</a> |
  <strong>🇮🇹 Italiano</strong>
</div>

<br />

# 🌲 Link.Me Clone - Piattaforma Avanzata di Link in Bio

[![React](https://img.shields.io/badge/React-19.1-61dafb?logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178c6?logo=typescript)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-7.1-646cff?logo=vite)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4-38bdf8?logo=tailwindcss)](https://tailwindcss.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](../LICENSE)

Un'applicazione web "Link in Bio" altamente personalizzabile, veloce e moderna. Permette agli utenti di creare profili con link multipli, temi dinamici, integrazione di video di sfondo, embed multimediali e monetizzazione, il tutto gestito tramite semplici file JSON.

🔗 **Demo:** [https://yordisc.github.io/link.me/](https://yordisc.github.io/link.me/)

---

## 🚀 Caratteristiche Principali

### ⚡ **Prestazioni Estreme**
- **Lazy Loading + Code Splitting:** I componenti pesanti (QR, Ads, Social) vengono caricati solo quando necessario.
- **Architettura Ottimizzata:** Caricamento iniziale ultra rapido.
- **PWA Enabled:** Funziona offline con Service Workers.
- **Lighthouse Perfect:** Punteggio 100/100 nelle prestazioni.

### 🎨 **Sistema di Temi Dinamici**
Potente sistema basato su JSON con 7 temi predefiniti:
- **default** - Tema base moderno e pulito.
- **pepsi** - Ispirato al marchio Pepsi.
- **7up** - Colori freschi e vibranti.
- **polar** - Toni artici freddi.
- **malta-polar** - Calore nostalgico.
- **solera** - Eleganza dorata.
- **carorena** - Design tropicale da spiaggia.

**Funzionalità:**
- Modalità Chiaro/Scuro automatica.
- Colori, ombre e bordi personalizzati.
- Sfondi con gradiente CSS personalizzato.
- Creazione di temi propri senza toccare il codice.

### 🎬 **Sfondi Multimediali**
Supporto nativo per formati multipli come sfondo:
- **Immagini:** JPG, PNG, WebP.
- **GIF Animate:** Per sfondi dinamici.
- **Video MP4:** Con riproduzione in loop automatico.
- **Gradienti CSS:** Sfondi sfumati personalizzati.

### 🧩 **Layout Flessibili**

#### **📋 Layout a Elenco**
Design classico verticale per una navigazione tradizionale.

#### **🎯 Layout a Griglia Intelligente**
Sistema di griglia avanzato con auto-organizzazione:
- **Pulsanti Rettangolari:** Occupano l'intera larghezza (2 colonne).
- **Pulsanti Quadrati:** Occupano 1 colonna singola.
- **Pulsanti Normali (Raggruppamento Intelligente):** Se ci sono due pulsanti normali consecutivi, si impilano verticalmente in una colonna per mantenere la simmetria con i quadrati.
- **Design Responsivo:** Si adatta perfettamente a qualsiasi dimensione dello schermo.

### 🌟 **Embed Intelligenti**
Sistema automatico di rilevamento della piattaforma che decide il modo migliore per mostrare il contenuto:

#### **📺 Embed Nativi (Iframe)**
Riproduzione diretta all'interno del profilo:
- **YouTube:** Video standard, Shorts e trasmissioni dal vivo.
- **Spotify:** Canzoni, album e playlist complete.
- **TikTok:** Video incorporati con player nativo.
- **Google Maps:** Mappe interattive incorporate.
- **CodePen:** Anteprime di codice dal vivo (ideale per portfolio).
- **Google Drive:** Documenti PDF con visualizzatore integrato.

#### **🎴 Smart Cards (Schede Sicure)**
Per le piattaforme che bloccano gli iframe (CORS/X-Frame-Options), genera schede eleganti con lo stile nativo di ogni marchio:
- **Instagram, LinkedIn, Twitter/X, GitHub (Repository), Letterboxd, Spotify (Profili).**

### 🎵 **Widget "Spotify Live" (Tempo Reale)**
Integrazione con l'API di **Lanyard** per mostrare cosa stai ascoltando su Spotify IN DIRETTA tramite il tuo stato di Discord:

**Stato Attivo (riproduzione musica):**
- Copertina dell'album animata.
- Nome della canzone e dell'artista in tempo reale.
- Barra di avanzamento sincronizzata.
- Visualizzatore audio animato.

**Stato Inattivo (nessuna riproduzione):**
- Si trasforma automaticamente in un pulsante standard "Seguimi su Spotify".

**Configurazione richiesta:**
- Account Discord collegato a Spotify.
- Profilo Discord pubblico.
- Discord User ID.

### 🖼️ **Visualizzatore Immagini Intelligente (Smart Viewer)**
I pulsanti possono aprire immagini a schermo intero senza uscire dal profilo. Ideale per:
- **Codici QR di Pagamento:** Binance Pay, Zelle, Bitcoin, PayPal.
- **Certificati/Diplomi:** Mostrare risultati in alta risoluzione.
- **Flyers/Promozioni:** Informazioni visive rapide.
- **Gallerie:** Mostrare lavori o prodotti.

**Caratteristiche:**
- Zoom e navigazione fluida.
- Pulsante di download incluso (tranne per la foto del profilo per privacy).
- Attivazione semplice: aggiungi `#view` alla fine di qualsiasi URL immagine.

### ☁️ **Smart Media Resolver (Gestore Cloud)**
Motore di risoluzione dei link che permette di utilizzare servizi di cloud storage direttamente come Avatar, Sfondo o Immagini dei Pulsanti senza cercare link diretti:

**Piattaforme supportate:**
- **Google Drive:**
  - **Immagini:** Usa automaticamente la CDN delle miniature HD (`lh3`) per il caricamento istantaneo ed evitare blocchi.
  - **Video:** Usa il parametro `#video` alla fine dell'URL per forzare la modalità player.
- **pCloud, Dropbox, Reddit:** Estrazione diretta dei media.

**Vantaggi:**
- Rilevamento automatico del tipo di file (immagine/video).
- Non è necessario generare manualmente link di download diretto.
- Ottimizzazione automatica del caricamento.

### 🎭 **Animazioni ed Effetti UI/UX**

#### **📜 Testo a Scorrimento (Auto-Scroll)**
Se il testo di un pulsante è troppo lungo per lo spazio disponibile, si attiva automaticamente un'animazione di scorrimento infinito fluido per renderlo completamente leggibile.

#### **🎠 Carosello Social**
Quando ci sono più di 4 icone social, la barra si trasforma automaticamente in un nastro scorrevole con scroll orizzontale fluido.

#### **✨ Transizioni Fluide**
- Animazioni ottimizzate con Framer Motion.
- Effetti hover eleganti.
- Micro-interazioni che migliorano l'esperienza.

### 🔀 **Drag & Drop (Opzionale)**
Funzionalità di trascinamento per:
- Riordinare i link in tempo reale.
- Riorganizzare i pulsanti social.
- Posizionare il pulsante "Join" (Iscriviti/Unisciti).
- Le modifiche vengono mantenute durante la sessione.

### 🛡️ **ContentGuard™ - Sistema Anti-AdBlock**
Sistema avanzato di protezione della monetizzazione che rileva i blocchi pubblicitari (uBlock Origin, AdGuard, AdBlock Plus) tramite tecniche multiple:

**Metodi di Rilevamento:**
1. **Trappola Esca Locale:** Tenta di caricare file tipicamente bloccati (`ads.js`, `prebid.js`).
2. **Trappola di Rete:** Verifica la connessione con server pubblicitari reali.
3. **Trappola Cosmetica (DOM):** Rileva se elementi con classi come `.adsbox` vengono nascosti dal browser.

**Caratteristiche:**
- Codice offuscato per evitare il rilevamento da parte delle liste di filtri.
- Nomi di componenti e variabili protetti.
- Spazi preparati per Google AdSense con validazione di sicurezza.

*⚠️ Nota: In modalità sviluppo (`npm run dev`), il blocco potrebbe essere disabilitato per facilitare la programmazione.*

### 💰 **Sistema di Monetizzazione**
- Integrazione con Google AdSense.
- Spazi pubblicitari ottimizzati.
- Protezione anti-blocco inclusa.
- Sidebar fluttuanti per annunci.

### 📱 **Design Mobile First**
- Design responsivo che **nasconde automaticamente le "scatole/schede" su mobile** per un'esperienza immersiva a schermo intero.
- Ottimizzazione touch per la navigazione mobile.
- Interfaccia adattiva in base al dispositivo.
- Transizioni fluide tra i breakpoint.

### 🔐 **Sicurezza e Privacy**
- **Crittografia AES:** I dati del profilo salvati in `sessionStorage` sono cifrati con CryptoJS per prevenire letture casuali o modifiche dalla console.
- **Nessun Tracciamento Invasivo:** Non raccogliamo dati personali senza consenso.
- **Protezione Dati Sensibili:** Sistema di tipi TypeScript per informazioni delicate.

### 📍 **Posizionamento Flessibile dei Social**
Controllo totale su dove appaiono le tue icone social:
- **`top`**: Nella scheda del profilo, sotto la biografia.
- **`bottom`**: Alla fine della lista dei link, con separatore visivo.
- **`both`**: In entrambi i posti (utile per profili molto lunghi).

### 🔗 **Pulsanti Interattivi Intelligenti**
Tre tipi di pulsanti con caratteristiche uniche:
- **Normal:** Pulsante standard con icona e testo.
- **Square:** Pulsante quadrato con immagine di sfondo.
- **Rectangular:** Pulsante tipo banner largo con immagine in evidenza.

---

## 🛠️ Tecnologie Utilizzate

### **Core Framework**
- **React 19.1.1** - Libreria UI con le ultime funzionalità.
- **TypeScript 5.9.3** - Tipizzazione statica robusta.
- **Vite 7.1.7** - Build tool di nuova generazione.
- **React Router DOM 7.9.5** - Routing dinamico (`/:username`).

### **Stili e Animazioni**
- **Tailwind CSS 3.4.18** - Framework CSS utility-first.
- **Styled Components 6.1.19** - CSS-in-JS per i temi.
- **Framer Motion 12.23.24** - Libreria di animazioni fluide.
- **PostCSS 8.5.6** + **Autoprefixer 10.4.21** - Elaborazione CSS.

### 🕹️ Gamification ed Easter Eggs
La piattaforma include esperienze interattive nascoste o attivabili:

#### **🏃 Pepsiman Runner**
Un gioco stile "Endless Runner" integrato direttamente nell'applicazione.
- Componenti personalizzati (Ostacoli, Schermata Game Over).
- Integrazione fluida con il tema visivo.

#### **💻 Modalità Terminale**
Una console a riga di comando interattiva (`src/components/Games/Terminal`) per utenti avanzati o come portfolio per sviluppatori backend.
- Supporto per comandi personalizzati.
- Navigazione basata su testo.

### **Utility Core**
- **@dnd-kit (core 6.3.1 + sortable 10.0.0)** - Sistema completo Drag & Drop.
- **React Hook Form 7.66.0** + **Yup 1.7.1** - Validazione dei form.
- **Zustand 5.0.8** - Gestione dello stato leggera.
- **date-fns 4.1.0** - Manipolazione date moderna.

### **Funzionalità Speciali**
- **react-qr-code 2.0.18** - Generazione codici QR.
- **crypto-js 4.2.0** - Crittografia AES per dati locali.
- **idb 8.0.3** - Wrapper moderno per IndexedDB.
- **react-icons 5.5.0** - Libreria estesa di icone.
- **lucide-react 0.552.0** - Icone ottimizzate aggiuntive.

### **Analytics e Tracking**
- **react-ga4 2.1.0** - Integrazione Google Analytics 4.

### **Strumenti di Sviluppo**
- **Vite Plugin PWA 1.1.0** - Configurazione PWA automatica.
- **Vitest 4.0.8** - Framework di testing ultra-rapido.
- **Storybook 10.0.5** - Sviluppo isolato dei componenti.
- **ESLint 9.36.0** + **Prettier 3.6.2** - Linting e formattazione.
- **TypeScript ESLint 8.45.0** - Regole specifiche TS.
- **gh-pages 6.3.0** - Deployment automatizzato.

---

## 📦 Installazione e Uso Locale

### **Prerequisiti**
- **Node.js:** v18.0.0 o superiore.
- **npm:** v9.0.0 o superiore (o yarn/pnpm equivalente).
- **Git:** Per clonare il repository.

### **Passaggi di Installazione**

#### **1. Clonare il Repository (Privato)**
```bash
git clone [https://github.com/yordisc/link.me-source.git](https://github.com/yordisc/link.me-source.git)
cd link.me
````

#### **2. Installare le Dipendenze**

```bash
npm install
```

#### **3. Avviare il Server di Sviluppo**

```bash
npm run dev
```

Visita **`http://localhost:5173/`** nel tuo browser.

#### **4. Compilare per la Produzione**

```bash
npm run build
```

I file compilati si troveranno nella cartella `dist/`.

#### **5. Anteprima di Produzione**

```bash
npm run preview
```

-----

## ⚙️ Configurazione Profilo (JSON)

Tutto il contenuto è gestito tramite file JSON nella cartella `public/data/`.

### **Crea il tuo Profilo**

Crea un file con il tuo nome utente: `public/data/jose.json`

### **Struttura JSON Completa**

```json
{
  "profile": {
    "username": "jose",
    "displayName": "José Developer",
    "bio": "Frontend Dev | Creator | Tech Enthusiast 🚀",
    "avatarUrl": "[https://tuo-cdn.com/avatar.jpg](https://tuo-cdn.com/avatar.jpg)",
    "avatarImages": [
      {
        "id": "main",
        "url": "[https://tuo-cdn.com/avatar.jpg](https://tuo-cdn.com/avatar.jpg)",
        "alt": "Profilo Principale"
      },
      {
        "id": "fun",
        "url": "[https://tuo-cdn.com/avatar-fun.jpg](https://tuo-cdn.com/avatar-fun.jpg)",
        "alt": "Modalità Divertente"
      }
    ],
    "theme": "pepsi",
    "settings": {
      "backgroundImage": "/videos/sfondo.mp4",
      "hideThemeButton": false
    },
    "socialButtons": {
      "enabled": true,
      "draggable": true
    },
    "joinButton": {
      "enabled": true,
      "text": "Iscriviti",
      "url": "[https://newsletter.com](https://newsletter.com)",
      "backgroundColor": "#000000",
      "textColor": "#FFFFFF"
    }
  },
  "links": [
    {
      "id": "portfolio",
      "type": "rectangular",
      "title": "🎨 Il Mio Portfolio",
      "url": "[https://miosito.com](https://miosito.com)",
      "visible": true,
      "icon": "linkcustom"
    },
    {
      "id": "instagram",
      "type": "normal",
      "title": "Instagram",
      "url": "[https://instagram.com/tuo_utente](https://instagram.com/tuo_utente)",
      "visible": true,
      "icon": "instagram"
    }
  ]
}
```

-----

## 🔗 Tipi di Link ed Esempi

### **1. Pulsante Normale (Standard)**

Pulsante standard con icona e testo. Ideale per link generali.

```json
{
  "id": "portfolio",
  "type": "normal",
  "title": "Il Mio Portfolio Web",
  "url": "[https://miosito.com](https://miosito.com)",
  "icon": "globe",
  "visible": true,
  "styles": {
    "backgroundColor": "#3b82f6",
    "color": "white"
  }
}
```

**Icone disponibili:** `instagram`, `twitter`, `facebook`, `linkedin`, `github`, `youtube`, `tiktok`, `spotify`, `globe`, `mail`, `phone`, `linkcustom`, etc.

-----

### **2. Pulsante Quadrato (Square)**

Pulsante compatto con immagine di sfondo. Perfetto per layout a griglia.

```json
{
  "id": "progetto1",
  "type": "square",
  "title": "Progetto E-commerce",
  "url": "[https://progetto.com](https://progetto.com)",
  "imageUrl": "[https://cdn.com/progetto-thumbnail.jpg](https://cdn.com/progetto-thumbnail.jpg)",
  "visible": true
}
```

-----

### **3. Pulsante Rettangolare (Banner)**

Pulsante largo tipo banner con immagine in evidenza. Ideale per contenuti in primo piano.

```json
{
  "id": "in-evidenza",
  "type": "rectangular",
  "title": "🚀 Progetto in Evidenza 2024",
  "url": "[https://grande-progetto.com](https://grande-progetto.com)",
  "imageUrl": "[https://cdn.com/banner-progetto.jpg](https://cdn.com/banner-progetto.jpg)",
  "visible": true
}
```

-----

### **4. Embed di YouTube**

Incorpora video, shorts o trasmissioni dal vivo direttamente nel tuo profilo.

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

**Formati supportati:**

  - Video: `https://youtube.com/watch?v=VIDEO_ID`
  - Shorts: `https://youtube.com/shorts/VIDEO_ID`
  - Live: `https://youtube.com/live/VIDEO_ID`

-----

### **5. Embed di Spotify**

Incorpora canzoni, album o playlist con player nativo.

```json
{
  "id": "mia-playlist",
  "type": "embed",
  "provider": "spotify",
  "url": "[https://open.spotify.com/playlist/37i9dQZF1DXcBWIGoYBM5M](https://open.spotify.com/playlist/37i9dQZF1DXcBWIGoYBM5M)",
  "shape": "rectangular",
  "visible": true
}
```

**Tipi supportati:**

  - Canzoni: `https://open.spotify.com/track/TRACK_ID`
  - Album: `https://open.spotify.com/album/ALBUM_ID`
  - Playlist: `https://open.spotify.com/playlist/PLAYLIST_ID`

-----

### **6. Widget Spotify Live (Tempo Reale)**

Mostra cosa stai ascoltando IN DIRETTA tramite Lanyard + Discord.

```json
{
  "id": "spotify-now-playing",
  "type": "embed",
  "provider": "spotify-bio",
  "title": "🎵 Ascoltando ora",
  "url": "[https://open.spotify.com/user/TU_USUARIO_SPOTIFY](https://open.spotify.com/user/TU_USUARIO_SPOTIFY)",
  "originalUrl": "TUO_DISCORD_USER_ID",
  "shape": "rectangular",
  "visible": true
}
```

**Configurazione richiesta:**

1.  Collega Spotify al tuo account Discord.
2.  Mantieni il tuo profilo Discord pubblico.
3.  Ottieni il tuo Discord User ID.
4.  Sostituisci `TUO_DISCORD_USER_ID` con il tuo ID reale.

**Come ottenere il tuo Discord User ID:**

1.  Attiva la Modalità Sviluppatore su Discord (Impostazioni → Avanzate).
2.  Clicca col tasto destro sul tuo profilo → Copia ID.

-----

### **7. Visualizzatore Immagini/QR con https://www.google.com/search?q=%23view**

Apre le immagini a schermo intero al clic. Perfetto per codici QR di pagamento.

```json
{
  "id": "qr-binance",
  "type": "square",
  "title": "💳 Paga con Binance",
  "imageUrl": "[https://unsplash.com/crypto-preview.jpg](https://unsplash.com/crypto-preview.jpg)",
  "url": "[https://drive.google.com/file/d/ID_DEL_TUO_QR/view?usp=sharing#view](https://drive.google.com/file/d/ID_DEL_TUO_QR/view?usp=sharing#view)",
  "visible": true
}
```

**Come funziona:**

  - **`imageUrl`**: Bella immagine di copertina del pulsante (decorativa).
  - **`url`** + **`#view`**: Immagine reale che si aprirà nel visualizzatore (funzionale).

**Casi d'uso:**

  - QR di Binance Pay, Zelle, Bitcoin.
  - Certificati o diplomi.
  - Volantini di eventi.
  - Menu di ristoranti.

-----

### **8. Video da Google Drive**

Usa video salvati su Google Drive direttamente.

```json
{
  "id": "video-demo",
  "type": "rectangular",
  "title": "📹 Video Demo del Progetto",
  "url": "#",
  "imageUrl": "[https://drive.google.com/file/d/ID_DEL_VIDEO/view?usp=sharing#video](https://drive.google.com/file/d/ID_DEL_VIDEO/view?usp=sharing#video)",
  "visible": true
}
```

**Importante:** Aggiungi `#video` alla fine dell'URL di Google Drive per forzare la modalità player.

-----

### **9. Embed di TikTok**

Incorpora video di TikTok con player nativo.

```json
{
  "id": "tiktok-viral",
  "type": "embed",
  "provider": "tiktok",
  "url": "[https://tiktok.com/@utente/video/1234567890](https://tiktok.com/@utente/video/1234567890)",
  "shape": "square",
  "visible": true
}
```

-----

### **10. Embed di Google Maps**

Mostra la tua posizione o luoghi importanti.

```json
{
  "id": "mio-ufficio",
  "type": "embed",
  "provider": "googlemaps",
  "url": "[https://maps.google.com/?q=Latitude,Longitude](https://maps.google.com/?q=Latitude,Longitude)",
  "shape": "rectangular",
  "visible": true
}
```

-----

### **11. Embed di CodePen**

Perfetto per sviluppatori: mostra il tuo codice dal vivo.

```json
{
  "id": "demo-code",
  "type": "embed",
  "provider": "codepen",
  "url": "[https://codepen.io/utente/pen/PEN_ID](https://codepen.io/utente/pen/PEN_ID)",
  "shape": "rectangular",
  "visible": true
}
```

-----

### **12. Smart Cards (Instagram, LinkedIn, Twitter, GitHub)**

Per le piattaforme che bloccano gli iframe, viene generata una scheda elegante con anteprima.

```json
{
  "id": "linkedin-profile",
  "type": "embed",
  "provider": "linkedin",
  "url": "[https://linkedin.com/in/tuo-profilo](https://linkedin.com/in/tuo-profilo)",
  "shape": "normal",
  "visible": true
}
```

**Piattaforme con Smart Cards:**

  - Instagram
  - LinkedIn
  - Twitter (X)
  - GitHub (repository)
  - Letterboxd

-----

## 🎨 Sistema di Temi

### **Temi Inclusi**

| Tema | ID | Descrizione |
|------|-----|-------------|
| **Default** | `default` | Tema base moderno e pulito |
| **Pepsi** | `pepsi` | Blu e rosso, ispirato al marchio |
| **7UP** | `7up` | Verde limone fresco e vibrante |
| **Polar** | `polar` | Toni artici freddi |
| **Malta Polar** | `malta-polar` | Calore dorato nostalgico |
| **Solera** | `solera` | Eleganza dorata premium |
| **Carorena** | `carorena` | Design tropicale da spiaggia |

### **Applicare un Tema**

Nel tuo file JSON del profilo:

```json
{
  "profile": {
    "theme": "pepsi"
  }
}
```

### **Creare il tuo Tema**

Crea un file in `public/data/themes/mio-tema.json`:

```json
{
  "id": "mio-tema-personalizzato",
  "name": "Il Mio Tema Personalizzato",
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

## 📍 Configurazione Social Media

Le icone dei social media vengono generate automaticamente dalla tua lista principale di `links` quando l'`icon` corrisponde a un social network noto (instagram, twitter, github, etc.) e hai `socialButtons.enabled: true`.

```json
"profile": {
  "socialButtons": {
    "enabled": true,
    "draggable": true
  }
}
```

**Opzioni di `style`:**

  - **`circles`**: Icone circolari (default).
  - **`squares`**: Icone quadrate.
  - **`rounded`**: Icone con bordi arrotondati.

**Opzioni di `position`:**

  - **`top`**: Appaiono nella scheda del profilo, sotto la bio.
  - **`bottom`**: Alla fine di tutti i link, con separatore.
  - **`both`**: In entrambe le posizioni (utile per profili lunghi).

**`draggable`:**

  - **`true`**: Permette di riordinare le icone con drag & drop.
  - **`false`**: Ordine fisso.

### **Carosello Automatico**

Quando configuri **più di 4 icone social**, la barra si trasforma automaticamente in un **nastro scorrevole** con scroll orizzontale fluido.

-----

## 📂 Struttura del Progetto

```bash
link.me/
│
├── public/
│   ├── data/
│   │   ├── themes/       # Temi JSON (default, etc.)
│   │   ├── yordisc.json         # Profili utente
│   │   ├── jose.json
│   │   └── maria.json
│   └── backgrounds/             # Risorse multimediali
│
├── src/
│   ├── components/
│   │   ├── ads/              # Sistema di monetizzazione
│   │   │   ├── AdSenseUnit.tsx
│   │   │   ├── ContentGuard.tsx # Sistema Anti-AdBlock
│   │   │   └── FloatingAdSidebars.tsx
│   │   ├── avatar/              # Avatar e visualizzatore
│   │   │   ├── AvatarViewer.tsx
│   │   │   └── EnhancedAvatar.tsx
│   │   ├── buttons/             # Componenti pulsanti
│   │   │   ├── NormalButton.tsx
│   │   │   ├── SquareButton.tsx
│   │   │   ├── RectangularButton.tsx
│   │   │   ├── SocialButtons.tsx
│   │   │   ├── ...
│   │   │   └── Terminal/        # Console interattiva
│   │   ├── widgets/             # Widget esterni
│   │   │   └── SpotifyWidget.tsx
│   │   └── Layout/              # Struttura base
│   │
│   ├── contexts/   # Gestione stato (ThemeContext)
│   ├── hooks/      # Custom Hooks (useLanyard, etc)
│   ├── utils/      # Utility (crypto.ts)
│   └── types/      # Definizioni TypeScript
│
├── package.json
├── vite.config.ts
└── tailwind.config.js
```

-----

## 🚀 Rilascio (Deployment)

### **GitHub Pages (Automatizzato)**

Il progetto è preconfigurato per il rilascio su GitHub Pages con un solo comando:

```bash
npm run deploy
```

**Processo automatico:**

1.  Compila il progetto (`npm run build`).
2.  Carica la cartella `dist/` sul ramo `gh-pages`.
3.  GitHub Pages pubblica automaticamente.

**Il tuo sito sarà disponibile su:**

```
[https://yordisc.github.io/link.me/](https://yordisc.github.io/link.me/)
```

**Configurazione in `package.json`:**

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

## 🛡️ Garanzia di qualità e test

Questo progetto ha una pipeline di Integrazione Continua (CI) automatizzata che utilizza GitHub Actions. Ad ogni aggiornamento, vengono eseguiti audit delle prestazioni, test logici e simulazioni utente.

Report dettagliati dell'ultima distribuzione sono disponibili al pubblico:

| Audit | Strumento | Report in tempo reale |

:--- |:---: |:--- |

**Prestazioni e SEO** | ![Lighthouse](https://img.shields.io/badge/-Lighthouse-F44B21?style=flat-square&logo=lighthouse&logoColor=white) | [🚀 **Visualizza report HTML**](https://yordisc.github.io/link.me/reports/performance/index.html) |

**Test unitari** | ![Vitest](https://img.shields.io/badge/-Vitest-729B1B?style=flat-square&logo=vitest&logoColor=white) | [🧪 **Visualizza risultati JSON**](https://yordisc.github.io/link.me/reports/unit/vitest-results.json) |
| **Test E2E** | ![Cypress](https://img.shields.io/badge/-Cypress-17202C?style=flat-square&logo=cypress&logoColor=white) | [🤖 **Visualizza dati grezzi**](https://yordisc.github.io/link.me/reports/e2e/cypress-summary.json) |

> ℹ️ *Nota: questi report vengono rigenerati automaticamente nella cartella `/reports` del ramo `gh-pages` a ogni distribuzione riuscita.*

### **Linting e Formattazione**

```bash
# Eseguire ESLint
npm run lint

# Formattare il codice con Prettier
npm run format
```

-----

### **Guide di Stile**

  - ✅ Usa **TypeScript** per tutto il nuovo codice.
  - ✅ Segui le regole di **ESLint** configurate.
  - ✅ Scrivi **test unitari** per funzionalità critiche.
  - ✅ Documenta funzioni complesse con **JSDoc**.
  - ✅ Usa **commit semantici**:
      - `feat:` Nuova funzionalità
      - `fix:` Correzione di bug
      - `docs:` Modifiche alla documentazione
      - `style:` Formattazione, punti e virgola mancanti, ecc.
      - `refactor:` Refactoring del codice
      - `test:` Aggiunta di test
      - `chore:` Aggiornamento dipendenze, ecc.

### **Segnalare Bug**

Se trovi un bug, per favore [apri una issue](https://github.com/yordisc/link.me/issues) con:

  - Descrizione chiara del problema.
  - Passaggi per riprodurlo.
  - Comportamento atteso vs. attuale.
  - Screenshot se possibile.
  - Informazioni su browser/OS.

-----

## 📄 Licenza

Distribuito sotto la **Licenza MIT**. Vedi il file `LICENSE` per maggiori informazioni.

Questo significa che puoi:

  - ✅ Usare commercialmente
  - ✅ Modificare il codice
  - ✅ Distribuire
  - ✅ Uso privato

Alle condizioni di:

  - 📋 Includere l'avviso di copyright
  - 📋 Includere la licenza MIT

-----

## 🙏 Ringraziamenti

Questo progetto non sarebbe possibile senza questi incredibili strumenti e community:

  - **[React Team](https://react.dev/)** - Per la migliore libreria UI.
  - **[Vite](https://vitejs.dev/)** - Build tool ultra-rapido.
  - **[Tailwind CSS](https://tailwindcss.com/)** - Framework CSS che accelera lo sviluppo.
  - **[React Icons](https://react-icons.github.io/)** - Migliaia di icone pronte all'uso.
  - **[Framer Motion](https://www.framer.com/motion/)** - Animazioni fluide e facili.
  - **[Lanyard API](https://github.com/Phineas/lanyard)** - Stato Discord in tempo reale.
  - **[Unsplash](https://unsplash.com/)** - Immagini di alta qualità gratuite.
  - **Open Source Community** - Per la condivisione della conoscenza.

-----

## 📞 Contatto e Supporto

### **Creatore**

👨‍💻 **Yordisc**

  - GitHub: [@yordisc](https://github.com/yordisc)
  - Progetto: [link.me](https://github.com/yordisc/link.me)

### **Ottenere Aiuto**

  - 📖 [Documentazione Completa](https://www.google.com/search?q=%23)
  - 💬 [Discussions](https://github.com/yordisc/link.me/discussions)
  - 🐛 [Segnala Bug](https://github.com/yordisc/link.me/issues)
  - 💡 [Richiedi Funzionalità](https://github.com/yordisc/link.me/issues/new?labels=enhancement)

-----

\<div align="center"\>

## ⭐ Se ti piace il progetto, non dimenticare di lasciare una stella ⭐

[](https://github.com/yordisc/link.me/stargazers)
[](https://github.com/yordisc/link.me/network/members)

-----

**Fatto con ☕ da [Yordisc](https://github.com/yordisc)**

*"Un link alla volta, costruendo la tua presenza digitale perfetta"*

\</div\>