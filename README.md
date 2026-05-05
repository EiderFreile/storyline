# 📖 Storyline

Tu universo narrativo. App PWA para iPhone de gestión de proyectos de escritura.

---

## 🚀 Configuración

### Firebase ya configurado ✅
La app ya tiene los datos de Firebase integrados en `index.html`.

Las reglas de Realtime Database deben incluir:

```json
{
  "rules": {
    "nailstock": { ".read": true, ".write": true },
    "projects":  { ".read": true, ".write": true },
    "characters":{ ".read": true, ".write": true },
    "relations": { ".read": true, ".write": true },
    "plots":     { ".read": true, ".write": true },
    "timelines": { ".read": true, ".write": true },
    "scenes":    { ".read": true, ".write": true }
  }
}
```

---

## 📱 Instalar en iPhone como app nativa

1. Abre **Safari** en tu iPhone
2. Ve a la URL de GitHub Pages
3. Pulsa el botón **Compartir** (📤)
4. Toca **"Añadir a pantalla de inicio"**
5. Dale el nombre *Storyline* y pulsa **Añadir**

¡Aparecerá en tu pantalla de inicio con el icono del libro dorado!

---

## 🔐 Contraseña

La primera vez que abras la app te pedirá que **crees una contraseña**.
Se guarda localmente en tu dispositivo. Solo tú puedes acceder.

> Para resetearla: Safari → Ajustes → Avanzado → Datos de sitios web → elimina el sitio.

---

## 📂 Estructura de archivos

```
storyline/
├── index.html          ← Toda la app (HTML + CSS + JS + Firebase)
├── manifest.json       ← Configuración PWA para iPhone
├── service-worker.js   ← Cache offline
├── icon.svg            ← Icono fuente (editable)
├── icon-192.png        ← Icono para pantalla de inicio iPhone
├── icon-512.png        ← Icono grande PWA
└── README.md           ← Este archivo
```

---

## ✨ Funcionalidades

- **Proyectos**: Crea y gestiona múltiples proyectos de escritura
- **Personajes**: Fichas completas con atributos físicos, background, motivaciones y objetivos
- **Relaciones**: Mapa de relaciones entre personajes (amigos, enemigos, romance, familia...)
- **Trama**: Tramas por personaje y tramas generales de la historia
- **Cronología**: Líneas de tiempo con hitos (soporta múltiples líneas para flashbacks, etc.)
- **Escenas**: Escenas escritas con posición en la cronología y personajes involucrados
- **Escena Express**: Dictado por voz → transcripción automática → guardado como escena
- **Offline**: Funciona sin conexión gracias al Service Worker
- **Sincronización**: Todos los datos en Firebase Realtime Database

---

## 🎙 Nota sobre el micrófono

El reconocimiento de voz usa la **Web Speech API**.
En iPhone solo funciona en **Safari**. La primera vez pedirá permiso para el micrófono.
