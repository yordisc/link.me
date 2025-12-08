<div align="center">
  <p>
    <a href="../README.md">🇺🇸 English</a> |
    <strong>🇪🇸 Español</strong> |
    <a href="./README_IT.md">🇮🇹 Italiano</a>
  </p>
</div>

# 🌲 Link.Me Clone - Plataforma Avanzada de Enlaces en Bio

[![React](https://img.shields.io/badge/React-19.1-61dafb?logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178c6?logo=typescript)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-7.1-646cff?logo=vite)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4-38bdf8?logo=tailwindcss)](https://tailwindcss.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](../LICENSE)

Una aplicación web de "Enlace en Bio" altamente personalizable, rápida y moderna. Permite a los usuarios crear perfiles con múltiples enlaces, temas dinámicos, integración de videos de fondo, embeds multimedia y monetización, todo gestionado a través de archivos JSON simples.

🔗 **Demo:** [https://yordisc.github.io/link.me/](https://yordisc.github.io/link.me/)

---

## 🚀 Características Principales

### ⚡ **Rendimiento Extremo**
- **Lazy Loading + Code Splitting:** Los componentes pesados (QR, Ads, Redes Sociales) solo se cargan cuando se necesitan
- **Arquitectura Optimizada:** Carga inicial ultra rápida
- **PWA Enabled:** Funciona offline con Service Workers
- **Lighthouse Perfect:** Score 100/100 en rendimiento

### 🎨 **Sistema de Temas Dinámicos**
Potente sistema basado en JSON con 7 temas preconstruidos:
- **default** - Tema base moderno y limpio
- **pepsi** - Inspirado en la marca Pepsi
- **7up** - Colores frescos y vibrantes
- **polar** - Tonos árticos fríos
- **malta-polar** - Calidez nostálgica
- **solera** - Elegancia dorada
- **carorena** - Diseño tropical

**Funcionalidades:**
- Modo Claro/Oscuro automático
- Colores personalizados, sombras y bordes
- Fondos con gradientes CSS personalizados
- Creación de temas propios sin tocar código

### 🎬 **Fondos Multimedia**
Soporte nativo para múltiples formatos como fondo de pantalla:
- **Imágenes:** JPG, PNG, WebP
- **GIFs Animados:** Para fondos dinámicos
- **Videos MP4:** Con reproducción en loop automático
- **Gradientes CSS:** Fondos degradados personalizados

### 🧩 **Layouts Flexibles**

#### **📋 Layout Lista**
Diseño clásico vertical para navegación tradicional

#### **🎯 Layout Grid Inteligente**
Sistema de cuadrícula avanzado con auto-organización:
- **Botones Rectangulares:** Ocupan ancho completo (2 columnas)
- **Botones Cuadrados:** Ocupan 1 columna individual
- **Botones Normales (Agrupación Inteligente):** Si hay dos botones normales consecutivos, se apilan verticalmente en una columna para mantener simetría con los cuadrados
- **Responsive Design:** Se adapta perfectamente a cualquier tamaño de pantalla

### 🌟 **Embeds Inteligentes**
Sistema automático de detección de plataforma que decide la mejor forma de mostrar contenido:

#### **📺 Embeds Nativos (Iframe)**
Reproducción directa dentro del perfil:
- **YouTube:** Videos estándar, Shorts y transmisiones en vivo
- **Spotify:** Canciones, álbumes y playlists completas
- **TikTok:** Videos incrustados con reproductor nativo
- **Google Maps:** Mapas interactivos embebidos
- **CodePen:** Previsualizaciones de código en vivo (ideal para portfolios)
- **Google Drive:** Documentos PDF con visor integrado

#### **🎴 Smart Cards (Tarjetas Seguras)**
Para plataformas que bloquean iframes (CORS/X-Frame-Options), genera tarjetas elegantes con estilo nativo de cada marca:
- **Instagram, LinkedIn, Twitter/X, GitHub (Repositorios), Letterboxd, Spotify (Perfiles)**

### 🎵 **Widget "Spotify Live" (Tiempo Real)**
Integración con la API de **Lanyard** para mostrar lo que estás escuchando en Spotify EN VIVO a través de tu estado de Discord:

**Estado Activo (reproduciendo música):**
- Carátula del álbum animada
- Nombre de canción y artista en tiempo real
- Barra de progreso sincronizada
- Visualizador de audio animado

**Estado Inactivo (sin reproducción):**
- Se transforma automáticamente en un botón estándar de "Sígueme en Spotify"

**Configuración requerida:**
- Cuenta de Discord conectada con Spotify
- Perfil de Discord público
- Discord User ID

### 🖼️ **Visor de Imágenes Inteligente (Smart Viewer)**
Los botones pueden abrir imágenes en pantalla completa sin salir del perfil. Ideal para:
- **Códigos QR de Pagos:** Binance Pay, Zelle, Bitcoin, PayPal
- **Certificados/Diplomas:** Mostrar logros en alta resolución
- **Flyers/Promociones:** Información visual rápida
- **Galerías:** Muestra trabajos o productos

**Características:**
- Zoom y navegación fluida
- Botón de descarga incluido (excepto para foto de perfil por privacidad)
- Activación simple: agrega `#view` al final de cualquier URL de imagen

### ☁️ **Smart Media Resolver (Gestor de Nube)**
Motor de resolución de enlaces que permite usar servicios de almacenamiento en nube directamente como Avatar, Fondo o Imágenes de Botones sin buscar enlaces directos:

**Plataformas soportadas:**
- **Google Drive:** - **Imágenes:** Usa automáticamente el CDN de miniaturas HD (`lh3`) para carga instantánea y evitar bloqueos
  - **Videos:** Usa el parámetro `#video` al final de la URL para forzar modo reproductor
- **pCloud, Dropbox, Reddit:** Extracción directa de medios

### 🎭 **Animaciones y Efectos UI/UX**

#### **📜 Marquesina de Texto (Auto-Scroll)**
Si el texto de un botón es demasiado largo para caber en el espacio disponible, se activa automáticamente una animación de desplazamiento infinito suave para hacerlo completamente legible.

#### **🎠 Carrusel de Redes Sociales**
Cuando hay más de 4 iconos sociales, la barra se convierte automáticamente en una cinta deslizante con scroll horizontal fluido.

#### **✨ Transiciones Fluidas**
- Animaciones optimizadas con Framer Motion
- Hover effects elegantes
- Micro-interacciones que mejoran la experiencia

### 🛡️ **ContentGuard™ - Sistema Anti-AdBlock**
Sistema de protección de monetización avanzado que detecta bloqueadores de publicidad (uBlock Origin, AdGuard, AdBlock Plus) mediante múltiples técnicas.

### 💰 **Sistema de Monetización**
- Integración con Google AdSense
- Espacios publicitarios optimizados
- Protección anti-bloqueo incluida
- Sidebars flotantes para anuncios

### 📱 **Mobile First Design**
- Diseño responsive que **oculta automáticamente las "cajas/tarjetas" en móviles** para una experiencia inmersiva de pantalla completa
- Optimización táctil para navegación móvil
- Interfaz adaptativa según el dispositivo
- Transiciones suaves entre breakpoints

### 🔐 **Seguridad y Privacidad**
- **Encriptación AES:** Los datos del perfil guardados en `sessionStorage` están cifrados con CryptoJS para evitar lecturas casuales o modificaciones desde la consola
- **Sin Tracking Invasivo:** No recopilamos datos personales sin consentimiento
- **Protección de Datos Sensibles:** Sistema de tipos TypeScript para información delicada

### 📍 **Posicionamiento Flexible de Redes Sociales**
Control total sobre dónde aparecen tus iconos sociales:
- **`top`**: En la tarjeta de perfil, debajo de la biografía
- **`bottom`**: Al final de la lista de enlaces, con separador visual
- **`both`**: En ambos lugares (útil para perfiles muy largos)

### 🔗 **Botones Interactivos Inteligentes**
Tres tipos de botones con características únicas:
- **Normal:** Botón estándar con icono y texto
- **Square:** Botón cuadrado con imagen de fondo
- **Rectangular:** Botón tipo banner ancho con imagen destacada

---

## 🛠️ Tecnologías Utilizadas

### **Core Framework**
- **React 19.1.1** - Biblioteca de UI con últimas características
- **TypeScript 5.9.3** - Tipado estático robusto
- **Vite 7.1.7** - Build tool de nueva generación
- **React Router DOM 7.9.5** - Enrutamiento dinámico (`/:username`)

### **Estilos y Animaciones**
- **Tailwind CSS 3.4.18** - Framework utility-first CSS
- **Styled Components 6.1.19** - CSS-in-JS para tematización
- **Framer Motion 12.23.24** - Librería de animaciones fluidas
- **PostCSS 8.5.6** + **Autoprefixer 10.4.21** - Procesamiento CSS

### 🕹️ Gamificación y Easter Eggs
La plataforma incluye experiencias interactivas ocultas o activables:

#### **🏃 Pepsiman Runner**
Un juego estilo "Endless Runner" integrado directamente en la aplicación.

#### **💻 Modo Terminal**
Una consola de línea de comandos interactiva (`src/components/Games/Terminal`) para usuarios avanzados o como portafolio para desarrolladores backend.

### **Utilidades Core**
- **@dnd-kit (core 6.3.1 + sortable 10.0.0)** - Sistema completo Drag & Drop
- **React Hook Form 7.66.0** + **Yup 1.7.1** - Validación de formularios
- **Zustand 5.0.8** - Gestión de estado ligera
- **date-fns 4.1.0** - Manipulación de fechas moderna

### **Funcionalidades Especiales**
- **react-qr-code 2.0.18** - Generación de códigos QR
- **crypto-js 4.2.0** - Encriptación AES para datos locales
- **idb 8.0.3** - Wrapper moderno de IndexedDB
- **react-icons 5.5.0** - Biblioteca extensiva de iconos
- **lucide-react 0.552.0** - Iconos optimizados adicionales

### **Analytics y Tracking**
- **react-ga4 2.1.0** - Google Analytics 4 integration

---

## 📦 Instalación y Uso Local

### **Requisitos Previos**
- **Node.js:** v18.0.0 o superior
- **npm:** v9.0.0 o superior (o yarn/pnpm equivalente)
- **Git:** Para clonar el repositorio

### **Pasos de Instalación**

#### **1. Clonar el Repositorio (Privado)**
```bash
git clone [https://github.com/yordisc/link.me-source.git](https://github.com/yordisc/link.me-source.git)
cd link.me
`````

#### **2. Instalar Dependencias**

```bash
npm install
```

#### **3. Iniciar Servidor de Desarrollo**

```bash
npm run dev
```

Visita **`http://localhost:5173/`** en tu navegador

#### **4. Compilar para Producción**

```bash
npm run build
```

Los archivos compilados estarán en la carpeta `dist/`

---

## ⚙️ Configuración de Perfil (JSON)

Todo el contenido se gestiona mediante archivos JSON en la carpeta `public/data/`.

### **Crear tu Perfil**

Crea un archivo con tu nombre de usuario: `public/data/jose.json`

### **Estructura Completa del JSON**

```json
{
  "profile": {
    "username": "jose",
    "displayName": "José Developer",
    "bio": "Frontend Dev | Creator | Tech Enthusiast 🚀",
    "avatarUrl": "[https://tu-cdn.com/avatar.jpg](https://tu-cdn.com/avatar.jpg)",
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
      "title": "🎨 Mi Portafolio",
      "url": "[https://miweb.com](https://miweb.com)",
      "visible": true,
      "icon": "linkcustom"
    }
  ]
}
```

_Para ver la lista completa de tipos de enlaces y ejemplos detallados, consulta el código fuente o la documentación extendida._

---

## 🚀 Despliegue

### **GitHub Pages (Automatizado)**

El proyecto está preconfigurado para desplegar en GitHub Pages con un solo comando:

```bash
npm run deploy
```

---

## 📄 Licencia

Distribuido bajo la **Licencia MIT**. Ver archivo `LICENSE` para más información.

---

\<div align="center"\>

## ⭐ Si te gusta el proyecto, no olvides darle una estrella ⭐

[](https://github.com/yordisc/link.me/stargazers)
[](https://github.com/yordisc/link.me/network/members)

---

**Creado con ☕ por [Yordisc](https://github.com/yordisc)**

_"Un enlace a la vez, construyendo tu presencia digital perfecta"_

\</div\>