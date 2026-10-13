# Clocktower Studio

Versión inicial de prueba 0.1.0 para Windows y Android.

- [Descargar instalador para Windows](https://github.com/segundocires/clocktower-studio-downloads/releases/latest/download/Clocktower-Studio-Windows-Setup.exe)
- [Descargar APK para Android](https://github.com/segundocires/clocktower-studio-downloads/releases/latest/download/Clocktower-Studio.apk)
- [Paquete MSI para Windows](https://github.com/segundocires/clocktower-studio-downloads/releases/latest/download/Clocktower-Studio-Windows-x64.msi)

El servidor está incluido en Windows y se inicia automáticamente. No necesitás instalar Python ni herramientas de desarrollo.

## Conectar la PC y el teléfono

1. Instalá y abrí Clocktower Studio en Windows 10/11 de 64 bits.
2. Instalá el APK en Android 7.0 o posterior. Si Android lo solicita, permití a tu navegador instalar esta aplicación y confirmá la instalación.
3. Con ambos equipos en la misma red local, abrí **Dispositivos → Activar red local y mostrar QR** en Windows.
4. En Android, elegí escanear el QR de la PC. El código vence a los cinco minutos y sirve una sola vez.

Mantené la aplicación de Windows abierta para sincronizar proyectos y referencias. Los originales se guardan en la PC. Si Windows solicita permiso de firewall, la conexión del teléfono necesita acceso en tu red privada.

## Actualizaciones de Android

La app consulta las nuevas versiones al abrirse y mediante tareas periódicas de Android. Descarga automáticamente por Wi-Fi sin límite de datos. Cuando una actualización esté lista, pulsá **Instalar actualización** y confirmá en Android. Las restricciones de batería o una detención forzada pueden aplazar las consultas en segundo plano.

Cada actualización comprueba tamaño, SHA-256, versión, identificador de aplicación y la misma firma que la app instalada. La publicación incluye `latest.json`, `apk.sha256` y `apk-metadata.json`.

## Estado de esta versión

Instalación de Windows, servidor incluido, persistencia al reabrir y activación de red local verificados. La compilación y firma de Android están verificadas; cámara, galería, conexión completa y actualización entre versiones en un teléfono físico quedan pendientes.

Windows todavía no tiene certificado comercial de firma. Sus archivos `windows.sha256` y `windows-metadata.json` describen la integridad y procedencia del instalador.

Este repositorio distribuye instaladores y metadatos. No contiene proyectos, fotografías, credenciales ni la clave privada de firma.
