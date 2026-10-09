# Illbleed — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Traducción al **español de España** de *Illbleed* (Dreamcast, 2001), el survival horror de
Crazy Games (Climax Graphics) publicado por Jaleco en Norteamérica, que nunca salió en español.

La versión americana cuenta la historia con escenas habladas en inglés **sin subtítulos**.
Este parche traduce los textos del juego y además **activa subtítulos en castellano** en las
escenas habladas, para que la historia se entienda de principio a fin.

La traducción se reparte como **parche**: no incluye el juego. Necesitas tu propia copia para
aplicarlo.

## Estado

Última versión: **[v1.0 — Primera versión](../../releases/tag/v1.0)**. Estado: **en revisión**.

| Parte | Estado |
|---|---|
| Subtítulos de las escenas habladas | **Añadidos**: 1.517 subtítulos en 183 escenas, sincronizados con la voz |
| Mensajes, objetos y sus descripciones, tienda, quirófano, diarios, recortes y notas | Traducidos (477 textos) |
| Textos que aparecen durante las escenas | Traducidos (57) |
| Menús, marcador, avisos y rótulos de la interfaz en imagen | Traducidos (183 texturas: título, opciones, estado, objetos, Monitor del Terror, tarjeta de memoria, fichas de atracción…) |
| Narraciones de los prólogos y rótulos de escena en imagen | Traducidos |
| Caracteres españoles | **á é í ó ú ü ñ Á É Í Ó Ú Ü Ñ ¡ ¿ « »** |
| Partida completa de principio a fin | **No realizada** |

La versión americana tiene en el disco el guion japonés original y un sistema de subtítulos que
solo usaba la edición japonesa. Los subtítulos castellanos usan ese sistema con los tiempos
originales, que siguen al doblaje inglés. Se han traducido desde **lo que se oye en inglés**
(transcrito automáticamente), con el guion japonés como apoyo; los textos del juego, desde la
versión americana. Traducción y revisión asistidas por IA, sin revisión humana independiente.

La opción **SUBTÍTULOS** del menú de opciones (en el original, «MOVIE MESSAGE») los activa o
desactiva; viene activada.

### Cómo se ha comprobado

Todo en emulador (Flycast), no en una Dreamcast real:

- **Jugado desde partida nueva**: arranque sin tarjeta de memoria, título y opciones, ajuste de
  imagen, introducción completa con subtítulos, el parque, el menú de estado (objetos, personaje,
  mapa), la pantalla de carga y la primera atracción («The Homerun of Death») hasta pasado el
  primer evento de shock: ficha, requisitos, elección de personaje, narración y briefing.
- **Escenas forzadas**: las 13 escenas de historia que se pueden lanzar directamente (prólogos de
  atracción, finales, introducción), con los subtítulos comparados con la voz grabada.
- El resto de subtítulos se ha revisado sobre láminas dibujadas con la fuente del juego y la
  misma maquetación que el motor.
- Una auditoría automática comprueba en cada imagen los límites de memoria conocidos y la
  integridad del disco. El parche se ha aplicado sobre el original y el resultado se ha comparado
  byte a byte.

### Limitaciones conocidas

- No se ha jugado de principio a fin: la mayoría de escenas se han comprobado de forma estática,
  no en el juego.
- **No se ha podido probar el guardado** en la tarjeta de memoria (no hay punto de guardado
  accesible al principio); sí la pantalla de carga y sus mensajes.
- No se ha probado en hardware real.
- Se mantienen en inglés los logotipos, los títulos de las atracciones, algunos carteles del
  decorado y las tarjetas de identificación de los personajes.
- Los créditos finales no se han traducido.
- Algunas frases del doblaje son muy breves y su subtítulo pasa rápido.

## Cómo aplicar el parche

El parche modifica **solo la pista 3** de la imagen Redump del juego.

1. Descarga el parche `.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia del juego en formato **Redump BIN/CUE** de la versión **USA**
   (`Illbleed (USA).cue` con tres pistas).
3. **Comprueba que tu pista 3 es la correcta**:

   | | |
   |---|---|
   | Archivo | `Illbleed (USA) (Track 3).bin` |
   | Tamaño | 1.185.760.800 bytes |
   | MD5 | `6be1a24b034e8aabc2665aa38b9a0a8a` |

   ```bash
   md5sum "Illbleed (USA) (Track 3).bin"                    # Linux
   md5 "Illbleed (USA) (Track 3).bin"                       # macOS
   CertUtil -hashfile "Illbleed (USA) (Track 3).bin" MD5    # Windows
   ```

   Si no coincide, el parche fallará o dará un resultado corrupto.
4. Aplica el parche a la pista 3:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**:
     `xdelta3 -d -s "Illbleed (USA) (Track 3).bin" Illbleed.ES.v1.0.xdelta "Track 3 traducida.bin"`
5. Sustituye la pista 3 por la traducida **con el mismo nombre de archivo**
   (`Illbleed (USA) (Track 3).bin`). Las pistas 1 y 2 y el `.cue` no cambian.
6. Para **v1.0**, la pista 3 resultante tiene MD5 **`da0bfbb494823072b81ff501771ad205`**
   y el mismo tamaño que la original.
7. Carga el `.cue` en tu emulador (probado en Flycast).

Aplica cada versión sobre la **pista 3 original**, no sobre una ya traducida.

## Cambios

### v1.0 — 9 de octubre de 2026
- Primera versión: Illbleed en castellano, con subtítulos en todas las escenas habladas.
- Traducidos mensajes, objetos, diarios y notas, menús, marcador, avisos y rótulos de imagen.
- Tildes, eñes y signos de apertura en la fuente del juego, con el mismo color y contorno.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin relación alguna con
Crazy Games, Climax Graphics, SEGA ni Jaleco. Aquí no se distribuye el juego ni ninguna parte de él:
solo un parche que modifica una copia que ya tengas.

Si eres el titular de los derechos y quieres que retire esto, abre una incidencia y lo hago.
