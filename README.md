# NexusCode Systems — Solución web para ferreterías

Demos de NexusCode Systems para presentar a ferreterías y distribuidoras de materiales de construcción.

| Ruta | Contenido |
|------|-----------|
| `/` | **Página web de la ferretería** con diagnóstico del sector, recorrido guiado por 8 problemas y personalización en vivo (nombre, ciudad, WhatsApp, color). |
| `/sistema/` | **FerroNexus**: demo del sistema de ventas e inventario (usuario `demo`, clave `1234`). |

Son páginas HTML estáticas, sin dependencias ni proceso de compilación. Los datos de las demos se guardan solo en el navegador (localStorage).

## Probar en local

Abre `public/index.html` en el navegador, o:

```bash
firebase emulators:start --only hosting
```

## Publicar en Firebase Hosting

```bash
npm install -g firebase-tools
firebase login
firebase use --add            # elige tu proyecto de Firebase
firebase deploy --only hosting
```

## Deploy automático desde GitHub (opcional)

```bash
firebase init hosting:github
```

Esto crea la acción de GitHub y el secreto necesario, y cada `git push` a `main` publica la página.

## Personalizar para un cliente

- Rápido: en la demo usa el botón **Personalizar** de la barra NexusCode.
- Permanente: en `public/index.html`, edita `DEFAULT_CFG`, `ZONAS`, `HORARIO` y la lista de productos `P` al inicio del `<script>`.

---
© 2026 NexusCode Systems · Arequipa, Perú
