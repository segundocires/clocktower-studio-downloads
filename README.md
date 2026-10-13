# Clocktower Studio

Estudio audiovisual para Windows y Android. Este repositorio distribuye instaladores y metadatos; no contiene proyectos, fotos, credenciales ni la clave privada de firma.

**Versión 0.2.0 publicada y descargas verificadas.** Windows se instaló y abrió conservando los datos anteriores; el APK universal está firmado con la misma identidad de 0.1.0. Las descargas anónimas de NSIS, MSI y APK coinciden con sus SHA-256. El acceso por Internet todavía requiere completar Tailscale en la PC; las pruebas físicas Android siguen pendientes.

- [Instalador Windows](https://github.com/segundocires/clocktower-studio-downloads/releases/latest/download/Clocktower-Studio-Windows-Setup.exe)
- [APK Android](https://github.com/segundocires/clocktower-studio-downloads/releases/latest/download/Clocktower-Studio.apk)
- [Paquete MSI Windows](https://github.com/segundocires/clocktower-studio-downloads/releases/latest/download/Clocktower-Studio-Windows-x64.msi)

El servidor viene incluido en Windows; no requiere Python ni herramientas de desarrollo. La aplicación necesita Windows 10/11 x64 y WebView2. Android requiere Android 7 o posterior; los requisitos finales se validan en cada publicación.

## Cuentas y teléfono en 0.2.0

1. Abrir Clocktower en Windows y crear una cuenta en **Cuentas**.
2. Seleccionar esa cuenta para trabajar en su biblioteca independiente. El administrador puede gestionar todas.
3. Para acceso desde otras redes, activar Acceso remoto y completar la vinculación de Tailscale en la PC. El responsable publica la dirección HTTPS verificada mediante `studio.json`; no contiene contraseñas ni tokens.
4. En Android 0.2, entrar con usuario y contraseña. La sesión se conserva; no hace falta escanear QR. El teléfono puede usar Wi-Fi o datos móviles.

La PC debe permanecer encendida, conectada y con Clocktower abierto. El gateway público sólo admite cuentas; la administración permanece local. Si Tailscale o `studio.json` aún no están preparados, la app indica que el estudio todavía no está disponible. En este momento falta completar la vinculación y verificar Internet.

Los proyectos y dispositivos anteriores se conservan en **Biblioteca anterior**, cuenta `legacy`. Asignarle una contraseña desde Windows para usar el nuevo login. Las nuevas cuentas no comparten sus archivos. Cambiar contraseña o desactivar una cuenta cierra sus sesiones sin borrar los datos.

## Actualizaciones Android

La consulta y descarga de APK sólo usa Wi-Fi sin medición, aunque la biblioteca permita datos móviles. Android puede aplazar las tareas periódicas por batería o detención forzada.

Desde 0.2.0, Android 12 o posterior intenta instalar automáticamente cuando tiene permiso y el sistema lo permite; puede pedir confirmación. Android anterior requiere instalación manual. La transición 0.1.0 → 0.2.0 debe confirmarse con el actualizador anterior. No se promete instalación totalmente silenciosa.

Cada APK se verifica por tamaño, SHA-256, package, versión mayor y firma igual a la instalada. La release incluye `latest.json`, `apk.sha256` y `apk-metadata.json`. Windows ofrece hashes y metadatos; todavía no tiene certificado comercial de firma.

## Estado de pruebas

El código 0.2.0 pasa 34 pruebas backend, ocho Rust, 23 móviles y 30 comprobaciones JVM del actualizador. Windows se instaló y abrió con el panel Cuentas y la biblioteca anterior conservada, incluidos hash del original y preview. APK y descargas públicas están verificados. Siguen pendientes la vinculación de Tailscale, publicar `studio.json`, la conexión externa y cámara/actualización en teléfono físico.
