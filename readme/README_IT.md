<div align="center">
  <p>
    <a href="../README.md">🇺🇸 English</a> |
    <a href="./README_ES.md">🇪🇸 Español</a> |
    <strong>🇮🇹 Italiano</strong>
  </p>
</div>

# 🌲 Link.Me Clone - Piattaforma Avanzata Link in Bio

[![React](https://img.shields.io/badge/React-19.1-61dafb?logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178c6?logo=typescript)](https://www.typescriptlang.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](../LICENSE)

Un'applicazione web "Link in Bio" altamente personalizzabile, veloce e moderna. Permette agli utenti di creare profili con link multipli, temi dinamici, integrazione di video di sfondo, embed multimediali e monetizzazione, il tutto gestito tramite semplici file JSON.

🔗 **Demo:** [https://yordisc.github.io/link.me/](https://yordisc.github.io/link.me/)

---

## 🚀 Caratteristiche Principali

### ⚡ **Prestazioni Estreme**
- **Lazy Loading + Code Splitting:** I componenti pesanti vengono caricati solo quando necessario.
- **Architettura Ottimizzata:** Caricamento iniziale ultra rapido.
- **PWA Enabled:** Funziona offline con Service Workers.
- **Lighthouse Perfect:** Punteggio 100/100 nelle prestazioni.

### 🎨 **Sistema di Temi Dinamici**
Potente sistema basato su JSON con 7 temi precostruiti:
- **default** - Tema base moderno e pulito
- **pepsi** - Ispirato al marchio Pepsi
- **7up** - Colori freschi e vibranti
- **polar** - Toni artici freddi
- **solera** - Eleganza dorata
- **carorena** - Design tropicale

**Funzionalità:**
- Modalità Chiaro/Scuro automatica
- Sfondi con gradienti CSS personalizzati
- Creazione di temi propri senza toccare il codice

### 🎬 **Sfondi Multimediali**
Supporto nativo per molteplici formati come sfondo:
- **Immagini:** JPG, PNG, WebP
- **GIF Animate:** Per sfondi dinamici
- **Video MP4:** Con riproduzione in loop automatico

### 🧩 **Layout Flessibili**

#### **📋 Layout Lista**
Design classico verticale.

#### **🎯 Layout Grid Intelligente**
Sistema a griglia avanzato con auto-organizzazione:
- **Pulsanti Rettangolari:** Occupano l'intera larghezza.
- **Pulsanti Quadrati:** Occupano 1 colonna singola.
- **Responsive Design:** Si adatta perfettamente a qualsiasi schermo.

### 🌟 **Embed Intelligenti**
Sistema automatico di rilevamento della piattaforma:

#### **📺 Embed Nativi (Iframe)**
Riproduzione diretta all'interno del profilo:
- **YouTube, Spotify, TikTok, Google Maps, CodePen.**

#### **🎴 Smart Cards (Schede Sicure)**
Per piattaforme che bloccano gli iframe (Instagram, LinkedIn, Twitter/X, GitHub), genera schede eleganti con lo stile nativo.

### 🎵 **Widget "Spotify Live" (Tempo Reale)**
Integrazione con l'API di **Lanyard** per mostrare cosa stai ascoltando su Spotify IN DIRETTA tramite il tuo stato di Discord.

### 🖼️ **Visualizzatore Immagini (Smart Viewer)**
I pulsanti possono aprire immagini a schermo intero. Ideale per codici QR di pagamento (Binance, Zelle) o certificati.
- Attivazione semplice: aggiungi `#view` alla fine dell'URL dell'immagine.

### 🛡️ **ContentGuard™ - Sistema Anti-AdBlock**
Sistema di protezione della monetizzazione che rileva i blocchi pubblicitari e protegge gli spazi Google AdSense.

---

## 🛠️ Tecnologie Utilizzate

- **React 19.1.1**
- **TypeScript 5.9.3**
- **Vite 7.1.7**
- **Tailwind CSS 3.4.18**
- **Framer Motion 12.23.24**

---

## 📦 Installazione e Uso Locale

### **Requisiti**
- **Node.js:** v18.0.0 o superiore
- **npm:** v9.0.0 o superiore

### **Passaggi**

1. **Clonare il Repository**
   ```bash
   git clone [https://github.com/yordisc/link.me-source.git](https://github.com/yordisc/link.me-source.git)
   cd link.me
`````

2.  **Installare Dipendenze**

    ```bash
    npm install
    ```

3.  **Avviare Server di Sviluppo**

    ```bash
    npm run dev
    ```

---

## ⚙️ Configurazione Profilo (JSON)

Tutto il contenuto è gestito tramite file JSON nella cartella `public/data/`.

### **Struttura JSON (Esempio)**

```json
{
  "profile": {
    "username": "mario",
    "displayName": "Mario Rossi",
    "bio": "Sviluppatore Web | Creator 🚀",
    "theme": "pepsi"
  },
  "links": [
    {
      "id": "portfolio",
      "type": "rectangular",
      "title": "🎨 Il Mio Portfolio",
      "url": "[https://miosito.it](https://miosito.it)",
      "visible": true
    }
  ]
}
```

---

## 📄 Licenza

Distribuito sotto la **Licenza MIT**. Vedi il file `LICENSE` per maggiori informazioni.

---

\<div align="center"\>
\<b\>Creato con ☕ da \<a href="https://github.com/yordisc"\>Yordisc\</a\>\</b\>
\</div\>