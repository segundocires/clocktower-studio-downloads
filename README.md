# ClockWorkStudio

Estudio audiovisual para Windows y Android. Este repositorio distribuye instaladores y metadatos; no contiene proyectos, fotos, credenciales ni la clave privada de firma.

**Versión 0.2.1 publicada y descargas verificadas.** Windows muestra el nombre ClockWorkStudio y se instaló conservando cuentas, proyectos, originales, previews y configuración. El APK universal conserva la firma y el package anteriores con `versionCode=3`. Las ocho descargas anónimas de la release coinciden con sus tamaños y SHA-256; `latest.json` anuncia esa versión. El acceso por Internet todavía requiere completar Tailscale y publicar `studio.json`, que devuelve 404; las pruebas físicas Android siguen pendientes.

- [Instalador Windows](https://github.com/segundocires/clocktower-studio-downloads/releases/latest/download/Clocktower-Studio-Windows-Setup.exe)
- [APK Android](https://github.com/segundocires/clocktower-studio-downloads/releases/latest/download/Clocktower-Studio.apk)
- [Paquete MSI Windows](https://github.com/segundocires/clocktower-studio-downloads/releases/latest/download/Clocktower-Studio-Windows-x64.msi)

El servidor viene incluido en Windows; no requiere Python ni herramientas de desarrollo. La aplicación necesita Windows 10/11 x64 y WebView2. Android requiere Android 7 o posterior; los requisitos finales se validan en cada publicación.

Los archivos de descarga mantienen `Clocktower-Studio` en el nombre por compatibilidad; la aplicación instalada se llama **ClockWorkStudio**. Tamaños y hashes: [notas de 0.2.1](https://github.com/segundocires/clocktower-studio-downloads/releases/tag/v0.2.1).

## Cuentas y teléfono en 0.2.1

1. Abrir el estudio en Windows y crear una cuenta en **Cuentas**.
2. Seleccionar esa cuenta para trabajar en su biblioteca independiente. El administrador puede gestionar todas.
3. Para acceso desde otras redes, activar Acceso remoto y completar la vinculación de Tailscale en la PC. Después se publica la dirección HTTPS verificada mediante `studio.json`; no contiene contraseñas ni tokens.
4. En Android 0.2, entrar con usuario y contraseña. La sesión se conserva; no hace falta escanear QR. El teléfono puede usar Wi-Fi o datos móviles.

La PC debe permanecer encendida, conectada y con el estudio abierto. El gateway público sólo admite cuentas; la administración permanece local. `studio.json` todavía devuelve 404, así que la app indica que el estudio no está disponible y ofrece configuración avanzada. Falta completar la vinculación y verificar Internet.

Los proyectos y dispositivos anteriores se conservan en **Biblioteca anterior**, cuenta `legacy`. Asignarle una contraseña desde Windows para usar el nuevo login. Las nuevas cuentas no comparten sus archivos. Cambiar contraseña o desactivar una cuenta cierra sus sesiones sin borrar los datos.

## Actualizaciones Android

La consulta y descarga de APK sólo usa Wi-Fi sin medición, aunque la biblioteca permita datos móviles. Android puede aplazar las tareas periódicas por batería o detención forzada.

Desde 0.2.0, Android 12 o posterior intenta instalar automáticamente cuando tiene permiso y el sistema lo permite; puede pedir confirmación. Android anterior requiere instalación manual. La transición 0.1.0 → 0.2.0 debe confirmarse con el actualizador anterior. No se promete instalación totalmente silenciosa.

Cada APK se verifica por tamaño, SHA-256, package, versión mayor y firma igual a la instalada. La release incluye `latest.json`, `apk.sha256` y `apk-metadata.json`. Windows ofrece hashes y metadatos; todavía no tiene certificado comercial de firma.

## Estado de pruebas

El código 0.2.1 pasa 45 pruebas backend, ocho Rust y 23 móviles. Los smoke de actualización NSIS y MSI desde 0.2.0 pasaron en CI. El NSIS final se instaló en este PC: datos conservados y original y preview servidos sin cambios. APK y ocho descargas públicas están verificados. Siguen pendientes la vinculación de Tailscale, publicar `studio.json`, la conexión externa y cámara/actualización en teléfono físico.
