# LIBIAN TV — kit inicial de construcción

Este proyecto es un **punto de partida**, no una ISO ya compilada. Usa Debian Live `live-build` y un flujo de GitHub Actions para intentar construir una ISO x86-64 en la nube.

## Qué incluye
- Debian 13 (trixie), arquitectura `amd64`.
- Sesión gráfica ligera con XFCE y LightDM.
- Lanzador de pantalla completa llamado LIBIAN TV, con fondo oscuro y tarjetas.
- Firefox ESR, VLC, MPV, Kodi, terminal, gestor de archivos y juegos sencillos.
- Accesos a YouTube y servicios web compatibles; no instala una aplicación oficial de YouTube TV.
- Flujo de compilación en `.github/workflows/build.yml`.

## Límites importantes
- **No se ha compilado ni probado la ISO todavía.**
- El objetivo de 512 MB de RAM no es realista para navegación moderna y streaming. Con 3 GB hay más margen, pero el rendimiento depende del procesador, gráficos y servicios.
- La compatibilidad con DRM, resolución de video y cada plataforma de streaming varía.
- La ISO Live puede permitir probar el sistema; el instalador depende de que la configuración y los paquetes de Debian Live funcionen correctamente.
- Este proyecto no borra ni modifica tu PC por sí solo. Primero prueba la ISO en una máquina virtual o desde USB sin instalar.

## Cómo compilar en la nube
1. Crea una cuenta de GitHub si no tienes una y un repositorio nuevo llamado `libian-tv`.
2. Sube **todo el contenido de este ZIP** al repositorio.
3. Abre la pestaña **Actions** y habilita los flujos de trabajo si GitHub te lo pide.
4. Ejecuta **Build LIBIAN TV ISO** con **Run workflow**.
5. Cuando termine, abre la ejecución y descarga el artefacto `libian-tv-iso`.
6. Si el flujo falla, abre los registros del paso que falló; no des por hecho que existe una ISO.

La compilación necesita bastante espacio, tiempo y acceso a los repositorios de Debian. GitHub Actions puede cambiar sus límites y la compilación puede fallar si la configuración requiere ajustes.

## Probar con seguridad
Prueba primero en una máquina virtual. Si usas USB, haz copia de seguridad y comprueba cuidadosamente el dispositivo seleccionado antes de escribir una imagen: grabar una ISO puede borrar los datos de la unidad elegida.
