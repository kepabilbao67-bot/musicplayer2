# 🎧 NEON DJ — Mesa de mezclas en el navegador

Una mesa de DJ completa que funciona **directamente en el navegador**, sin instalar nada.
Pensada para aprender a mezclar música como hobby. Todo el código está en un solo archivo: **`index.html`**.

## ▶️ Cómo usarla

1. Descarga el archivo **`index.html`**.
2. Haz **doble clic** en él: se abrirá en tu navegador.
3. Espera unos segundos mientras se generan los ritmos y... ¡a mezclar!

> Recomendado: **Chrome, Edge o Firefox**, con auriculares o altavoces.

## ✨ Características

- 🎛️ **Dos platos (decks)** con vinilos que giran al reproducir.
- 🎵 **11 ritmos originales** generados por código (sin copyright): House, Hip-Hop, Techno, Synthwave, Reggaeton, Drum & Bass, Trap, Funk, Rock Español 80/90, Heavy Metal 80/90 y Pop Español 80/90.
- 📁 También puedes **cargar tus propias canciones** (MP3, WAV...).
- 🎚️ **EQ de 3 bandas** (graves/medios/agudos), **filtro**, **eco/delay** y **reverb** por deck.
- 🎚️ **Crossfader**, faders de canal y volumen general.
- ⏩ **Pitch ±50%** y **SYNC** que iguala el BPM **y cuadra el compás** automáticamente.
- 🔁 **Loop** de 4 tiempos, **CUE** y **3 hot cues** por deck (puntos de salto).
- 💿 **Modo scratch / jog**: arrastra el vinilo con el ratón.
- 📊 **Onda (waveform)** con cabezal y **medidores VU** animados.
- 💥 **Pads de efectos**: Riser, Airhorn, Impact y Zap.
- 🎙️ **Graba tu mezcla** y descárgala como **WAV** (reproducible en cualquier sitio).

## ⌨️ Atajos de teclado

| Tecla | Acción |
|-------|--------|
| `Q` / `P` | Play-Pausa Deck A / B |
| `A` / `L` | Cue Deck A / B |
| `Z` / `M` | Loop Deck A / B |
| `S` / `K` | Sync Deck A / B |
| `←` / `→` | Mover crossfader |
| `1` `2` `3` `4` | Riser / Airhorn / Impact / Zap |

## 🧠 Cómo funciona (para aprender)

- Usa la **Web Audio API** del navegador.
- Los ritmos se sintetizan nota a nota (bombo, caja, charles, bajo, sintes) con un `OfflineAudioContext`.
- Cada deck enruta el audio así: `fuente → EQ → filtro → volumen → crossfader → master`, con un envío de **delay** para el eco.
- La grabación usa `MediaRecorder` sobre la salida master.

---

Hecho con la ayuda de Kiro. ¡Disfruta aprendiendo a pinchar! 🎶


## 📱 Versión para Android (APK)

Este proyecto puede generar una app `.apk` para móvil Android **automáticamente**, sin instalar nada en tu ordenador.

Cómo conseguir el APK:

1. Ve a la pestaña **Actions** del repositorio y abre el flujo **"Construir APK"** (o se ejecuta solo al actualizar `index.html` en `main`).
2. Cuando termine (sale un ✅ verde), tienes el APK de dos formas:
   - En la sección **Releases** del repo, en la versión **"NEON DJ - APK para Android"**.
   - O dentro del propio run de Actions, en **Artifacts → NEON-DJ-apk**.
3. Descarga `NEON-DJ.apk`, ábrelo en el móvil y permite la instalación de orígenes desconocidos si lo pide.

> Es un APK de depuración (debug), perfecto para uso personal. La carpeta `apk-build/` contiene el proyecto Cordova que usa el flujo de GitHub Actions.
