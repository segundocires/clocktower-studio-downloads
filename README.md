# ClockWorkStudio

Estudio audiovisual para Windows y Android. Este repositorio distribuye instaladores y metadatos; no contiene proyectos, fotos, credenciales ni la clave privada de firma.

**Android 0.3.0 está publicado.** La pestaña **Videos** integra el estudio de cortos en la app: idea, guion, fichas de personaje y escenario, storyboard, generación con movimiento y audio, retomas, reproducción y descarga del MP4. Usa la sesión existente. Conserva Proyectos, Rodaje, Biblioteca y Trabajos.

Las nueve descargas de la entrega se verificaron sin autenticación contra tamaño y SHA-256. El APK conserva package y firma, usa `versionCode=5`, cuatro arquitecturas y Android 7/API24 como mínimo. **Los instaladores Windows siguen en 0.2.2**, con los mismos archivos y hashes.

- [APK Android 0.3.0](https://github.com/segundocires/clocktower-studio-downloads/releases/latest/download/Clocktower-Studio.apk)
- [Instalador Windows 0.2.2](https://github.com/segundocires/clocktower-studio-downloads/releases/latest/download/Clocktower-Studio-Windows-Setup.exe)
- [Paquete MSI Windows 0.2.2](https://github.com/segundocires/clocktower-studio-downloads/releases/latest/download/Clocktower-Studio-Windows-x64.msi)
- [Notas y hashes de la entrega](https://github.com/segundocires/clocktower-studio-downloads/releases/tag/v0.3.0)

Los archivos de descarga mantienen `Clocktower-Studio` en el nombre por compatibilidad; la aplicación instalada se llama **ClockWorkStudio**. Windows necesita Windows 10/11 x64 y WebView2.

## Crear y ver videos desde Android

1. Actualizar la APK sobre la versión anterior, sin desinstalar, para conservar la sesión y los borradores.
2. Entrar con la cuenta habitual y abrir **Videos**.
3. Elegir un proyecto y crear una película: preparar guion, revisar fichas y storyboard, y crear la película con audio. El recorrido actual genera cortos de 15 segundos.
4. Reproducir el resultado o tocar **Descargar MP4** para guardarlo en una carpeta del teléfono o compartirlo. Guardar en carpeta admite hasta 128 MiB; los archivos mayores pueden compartirse.

La PC debe permanecer encendida, conectada y ejecutando el supervisor y los motores del estudio de cortos. El teléfono puede usar Wi-Fi o datos móviles; el procesamiento se realiza en la PC. Los trabajos guardados continúan allí aunque se cierre la app. Los motores y sus modelos no se incluyen en la APK ni en los instaladores Windows 0.2.2; este recorrido requiere la PC configurada para cortos.

## Cuentas y acceso

Las cuentas se crean desde Windows. Cada cuenta conserva su biblioteca independiente; el administrador puede gestionar todas. Android guarda la sesión y no requiere QR. Cambiar la contraseña o desactivar una cuenta revoca sus sesiones sin borrar proyectos.

El descriptor público `studio.json` ya está publicado y contiene únicamente la dirección HTTPS del estudio. Tailscale Funnel publica el acceso de cuentas; la administración permanece local. El acceso HTTPS y la entrega del puente integrado se verificaron. El [estudio web](https://desktop-bpgk6br.tail61f93b.ts.net/studio) también sigue disponible.

Los proyectos y dispositivos anteriores permanecen en **Biblioteca anterior**, cuenta `legacy`. Se puede asignar una contraseña desde Windows para utilizar el acceso con usuario y contraseña.

## Actualizaciones Android

La consulta y descarga de APK usa Wi-Fi sin medición. Android puede aplazar las tareas periódicas por batería o detención forzada. Desde 0.2.0, Android 12 o posterior intenta instalar cuando tiene permiso y el sistema lo permite; puede pedir confirmación. Android anterior requiere instalación manual.

Cada APK se verifica por tamaño, SHA-256, package, versión mayor y firma igual a la instalada. La entrega incluye `latest.json`, `apk.sha256`, `apk-metadata.json` y `studio.json`. Windows conserva sus hashes y metadatos.

## Verificación

Pasaron la comprobación de tipos, 43 pruebas móviles, 10 del puente y 68 del servidor. La APK Release incluye su bundle JavaScript y se verificó con la misma firma de 0.2.2. En navegador con ancho de celular se comprobaron el acceso integrado, creación y cancelación, restauración, reproducción de 15 segundos con audio, descarga por el puente y cierre de sesión.

Las pruebas del selector de carpeta y de compartir usan APIs nativas simuladas. La instalación, actualización y revisión completa en un teléfono Android físico siguen pendientes.
