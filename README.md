# 🏍️ MotoTrack GPS — Guía de instalación

## ¿Qué es MotoTrack?
MotoTrack es una **Progressive Web App (PWA)** que funciona como una app nativa en cualquier Android.
No necesita Google Play. Se instala directamente desde un enlace.

---

## 📲 Cómo instalar en Android (cualquier dispositivo)

### Opción A — Desde Google Drive (recomendada para pruebas)
1. Sube la carpeta al servidor o usa GitHub Pages (ver abajo)
2. Comparte el enlace con los probadores
3. El probador abre el enlace en **Chrome para Android**
4. Chrome mostrará automáticamente un banner "**Añadir a pantalla de inicio**"
5. Toca **Instalar** → la app aparece como icono en el escritorio

### Opción B — GitHub Pages (gratis, permanente)
1. Crea una cuenta en [github.com](https://github.com)
2. Crea un repositorio nuevo llamado `mototrack`
3. Sube todos los archivos de esta carpeta
4. Ve a Settings → Pages → Source: main
5. Tu app estará en: `https://TU_USUARIO.github.io/mototrack`

### Opción C — Netlify Drop (más fácil, gratis)
1. Ve a [netlify.com/drop](https://app.netlify.com/drop)
2. Arrastra la carpeta completa al navegador
3. Netlify te dará un enlace público en segundos

---

## ✅ Funcionalidades incluidas

| # | Función | Estado |
|---|---------|--------|
| 1 | Guardar ruta al finalizar | ✅ |
| 2 | Cargar ruta desde archivo GPX/GeoJSON | ✅ |
| 3 | Crear rutas punto a punto tocando el mapa | ✅ |
| 4 | Mapa en tiempo real con posición GPS | ✅ |
| 5 | Instalable en cualquier Android | ✅ PWA |
| 6 | Gasolineras, bares, restaurantes, miradores, turismo (0-50 km) | ✅ |
| 7 | Calificar ruta 1-5 estrellas + texto + fotos | ✅ |
| 8 | Instalable sin Play Store desde enlace | ✅ |

---

## 🗂️ Archivos del proyecto

```
mototrack/
├── index.html      → App principal (toda la lógica y UI)
├── manifest.json   → Config PWA (nombre, icono, colores)
├── sw.js           → Service Worker (caché offline)
├── icon-192.png    → Icono app
├── icon-512.png    → Icono app (alta res)
└── README.md       → Esta guía
```

---

## 🔧 Permisos necesarios en Android
- **Ubicación (GPS)** → Para rastrear la ruta en tiempo real
- **Almacenamiento** → Para guardar fotos en las rutas

---

## 🌐 Compatibilidad
- ✅ Chrome Android 80+
- ✅ Samsung Internet 12+
- ✅ Edge Android
- ✅ Firefox Android (sin instalación PWA, funciona como web)
- ✅ iOS Safari (instalable via "Añadir a inicio")

---

## 💡 Notas técnicas
- Los datos (rutas guardadas) se almacenan en el **localStorage** del dispositivo
- Los mapas usan **OpenStreetMap** (gratuito, sin API key)
- Los POI usan la **API de Overpass** (OpenStreetMap, gratuito)
- Funciona **offline** para la app; los mapas requieren haber sido visitados antes
