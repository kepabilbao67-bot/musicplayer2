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
- 🎵 **6 ritmos originales** generados por código (sin copyright): House, Hip-Hop, Techno, Synthwave, Reggaeton y Drum & Bass.
- 📁 También puedes **cargar tus propias canciones** (MP3, WAV...).
- 🎚️ **EQ de 3 bandas** (graves/medios/agudos), **filtro** y **eco/delay** por deck.
- 🎚️ **Crossfader**, faders de canal y volumen general.
- ⏩ **Pitch ±50%** y **SYNC** para igualar el BPM de los dos platos.
- 🔁 **Loop** de 4 tiempos y **CUE**.
- 📊 **Onda (waveform)** con cabezal y **medidores VU** animados.
- 💥 **Pads de efectos**: Riser, Airhorn, Impact y Zap.
- 🎙️ **Graba tu mezcla** y descárgala como archivo de audio.

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
