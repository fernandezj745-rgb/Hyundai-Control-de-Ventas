HYUNDAI CONTROL DE VENTAS — PROYECTO ANDROID

Este es el proyecto Android para generar la APK. La aplicación abre el sitio HTTPS de Firebase Hosting
para que Firebase Authentication y Firestore funcionen en un origen web seguro.

URL configurada:
https://seguimiento-de-ventas-1f818.web.app

IMPORTANTE:
1. Primero debes publicar la web en Firebase Hosting. Si aún no está publicada, la APK mostrará que no se puede acceder.
2. Comprueba que Authentication tenga habilitado Correo electrónico/Contraseña.
3. Las reglas de Firestore deben limitar lectura y escritura a los tres correos autorizados.
4. La APK que genera el flujo es una APK DEBUG firmada automáticamente para pruebas e instalación directa.
   No es una APK release firmada para Google Play.

COMPILAR EN ANDROID STUDIO:
- Abre la carpeta HyundaiControlAndroid.
- Espera la sincronización de Gradle.
- Selecciona Build > Build Bundle(s) / APK(s) > Build APK(s).
- La APK debug queda en app/build/outputs/apk/debug/app-debug.apk.

También se incluye un workflow de GitHub Actions para compilarla en la nube.
