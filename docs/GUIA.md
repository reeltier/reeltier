# ReelTier: guía de 5 minutos

ReelTier ordena tu colección de videos: le ponés una nota a cada uno, se mueve solo a su carpeta, se renombra con sus datos (actriz, estudio, fecha) y te muestra estadísticas de lo que te gusta. Todo corre en tu PC.

## 1. Instalar y elegir carpetas

1. Ejecutá `ReelTier-Setup.exe`. No pide permisos de administrador.
2. Se abre la ventana de ReelTier con un asistente de cuatro pasos:
   - **Descargas:** donde caen los videos nuevos.
   - **Videoteca:** donde van a vivir los videos ya calificados.
   - **ThePornDB:** la clave gratis para que reconozca cada escena (se puede saltear y cargar después).
3. Listo. ReelTier queda junto al reloj; todo lo demás (orden de carpetas, formato del nombre, escala de notas) está en **Configurar**, abajo en el menú.

## 2. El día a día

- **Hoy:** qué conviene hacer ahora (repetidos, videos sin nivel, coincidencias para mirar) y las novedades de tus actrices favoritas.
- **Revisar → Poner nota:** el video en grande. Nota del 1 al 10, como en IMDb: tecla `1` a `9`, y `1` `0` seguidos para el 10. Del 6 al 10 el video se queda, cada nota en su carpeta (9 y 10 en la de los mejores); del 1 al 5 va a la papelera con esa nota. Al dejar de reproducir, el archivo se mueve.
- **Revisar → Coincidencias:** ReelTier buscó la escena en ThePornDB, StashDB y FansDB. `S` si es esa, `N` si no. Al aceptar, el archivo se renombra con los datos correctos.
- **Revisar → Sin resolver:** lo que todavía nadie confirmó, con el motivo en palabras y botones para resolverlo en lote.
- **Biblioteca:** todo, con filtros, vista previa al pasar el mouse y selección múltiple (Ctrl+clic).
- **Estadísticas:** clic en cualquier barra filtra todo, como en Power BI. "Tu gusto en el tiempo" compara períodos y exporta a CSV. "Tus etiquetas contra el general" muestra qué tenés mucho más (o menos) que el resto de las escenas de StashDB.
- **Recomendaciones:** escenas que no tenés, elegidas por esas etiquetas y tus estudios y actrices mejor calificados.
- **Configurar → Orden y nombres:** cómo se llaman los archivos (el formato de siempre, estudio primero, título y actrices, fecha primero o uno propio). La nota (`n8`) va siempre. Los que ya tenés se pueden pasar al formato nuevo: primero ves qué cambiaría.
- **Deshacer:** `Ctrl Z` o el botón "Deshacer último" vuelven atrás el último movimiento.
- `?` muestra todos los atajos; `Ctrl K` abre el buscador rápido.

## 3. Desde el visor (Meta Quest y similares)

Con la PC y el visor en el mismo WiFi:

- **HereSphere:** agregá la biblioteca `http://<IP de tu PC>:8770/heresphere`. Cada media estrella es un punto de la nota: 5 estrellas = 10, 4,5 = 9, 4 = 8, y 2,5 o menos va a la papelera con esa nota. Los marcadores de la línea de tiempo y las etiquetas `Lista:Nombre` se sincronizan con la app.
- **DeoVR:** misma dirección con `/deovr`.
- **Navegador del visor:** `http://<IP de tu PC>:8770/` es la página para calificar con el dedo.

La dirección y su código QR aparecen en **Conectar el visor** (abajo a la izquierda en la app, o clic derecho en el ícono junto al reloj).

## 4. Subtítulos automáticos

ReelTier escucha el audio de lo que conservás (las notas más altas, se puede cambiar) y guarda su subtítulo en el idioma original y traducido (`video.es.srt`, `video.en.srt`) en una subcarpeta `Subs` oculta junto al video, para no llenar la carpeta (se cambia en Configurar). Lo hace solo, cuando no estás mirando nada. En el reproductor los prendés y elegís el idioma.

## 5. Varias personas y seguridad

En **Configurar → Acceso** elegí un PIN o creá usuarios con tres roles: todo, calificar o solo mirar. Sin PIN, cualquier aparato de tu WiFi entra como dueño. La app solo responde a tu red de casa y rechaza pedidos de otras páginas web.

## Preguntas frecuentes

**¿Borra algo?** No. La papelera es una carpeta (`_papelera`) que vaciás vos.

**¿Sube mi colección a algún lado?** No. Solo salen el título, las actrices, el estudio o la huella del archivo (un código, no el video) para identificar escenas. Detalle completo en la Ayuda (`?`) → Privacidad.

**¿Y si un renombre quedó mal?** En la ficha del video, "Editar nombre". Si fue un lote, `python renombrar.py --deshacer`.

**¿Puedo traer lo que tenía en Stash?** Sí: `Ctrl K` → "Importar desde Stash" lee su base sin modificarla.

**¿Funciona con Plex, Jellyfin o Kodi?** Sí: `Ctrl K` → "Exportar fichas .nfo" deja la ficha de cada video al lado del archivo, en el formato que leen esas apps.

**Se cortó la luz en medio de una copia, ¿perdí el video?** No: el original se borra recién cuando la copia está grabada en el disco y verificada.
