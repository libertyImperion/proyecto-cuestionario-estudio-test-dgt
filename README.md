# Test DGT · Permiso B

Simulador del examen teórico de la DGT para el permiso de conducir clase B (España), pensado para estudiar: cada respuesta, acertada o fallada, viene explicada.

## Cómo usarlo
Abre `index.html` en el navegador (doble clic) o usa el acceso directo **Test DGT** del escritorio. No necesita instalar nada ni conexión a internet (solo las tipografías cargan de Google Fonts si hay red).

## Qué incluye
- **Examen simulado:** 30 preguntas, 30 minutos, 3 opciones, máximo 3 fallos, sin volver atrás. Opcionalmente incluye **una pregunta con vídeo de percepción del riesgo**, como anunció la DGT: se ve hasta 3 veces antes de ver la pregunta y el tiempo se amplía según la duración del vídeo.
- **Modo estudio:** explicación inmediata al contestar, por tema o mezclado.
- **Repasar mis fallos:** solo las preguntas falladas y aún no dominadas.
- **Progreso** guardado en el navegador (`localStorage`): aciertos, preguntas dominadas por tema, historial de exámenes y preferencias.
- **Banco:** 182 preguntas originales en 15 temas: 48 de señales, 33 de novedades 2026 (usuarios vulnerables) y 6 de percepción del riesgo con escena animada.
- **Gráficos:** señales oficiales españolas (`img/senales/`), semáforos, líneas, cruces con vehículos, esquemas propios (distancia de detención, regla de los 2 segundos, aquaplaning, posición lateral de seguridad, reposacabezas) y escenas animadas de tráfico. Salen en la explicación tras contestar.
- **Panel «Novedades y datos oficiales del examen»** en la pantalla de inicio, con enlaces al BOE y a la DGT.

## Actualización de octubre de 2026
- **Real Decreto 518/2026** (BOE-A-2026-13889), en vigor desde el 1 de octubre de 2026: usuarios vulnerables, adelantamiento a ciclistas (1,5 m, 20 km/h menos que el límite, cambio completo de carril), 5 m con el ciclista de delante, casco de ciclistas, patinetes (15 años, casco, luz o reflectante a 150 m), guantes y calzado en moto, arcén en retenciones, carril de emergencia, nieve, cinturón sin exenciones, peatones en plataforma única, caminos escolares y circulación urbana. Aplazado a 1-oct-2027: alumbrado diurno permanente en VMP y casco homologado en ciclomotores.
- **Real Decreto 52/2026** (BOE-A-2026-2140): Registro de Vehículos Personales Ligeros y seguro obligatorio de patinetes.
- **Examen:** la DGT anunció una pregunta basada en un vídeo de situaciones de riesgo (30 preguntas y 3 opciones se mantienen). La DGT lo presenta como previsión, así que conviene confirmar con la autoescuela si la convocatoria ya la incluye. Las escenas del simulador son esquemas animados, no vídeos reales de la DGT.
- Los puntos de cada infracción salen del cuadro de la Ley de Tráfico, no del reglamento. Hay prensa que da cifras distintas (por ejemplo 4 o 6 puntos por no respetar el 1,5 m); aquí se usa el cuadro del texto consolidado (6 puntos).

## Estructura
- `index.html`: toda la aplicación (HTML, CSS y JS) en un solo archivo. El banco de preguntas está al principio del `<script>`, en llamadas `Q(tema, figura, enunciado, [correcta, falsa1, falsa2], explicación, [porqué falsa1, porqué falsa2], regla)`.
- `img/senales/`: señales de tráfico en SVG, una por archivo, con el código oficial de la señal como nombre (`r2.svg` = STOP, `p13a.svg` = curva peligrosa a la derecha…).
- `contexto.md`: estado y próximos pasos.

## Aviso
Las preguntas son originales (el banco oficial de la DGT no es público) y siguen la normativa vigente a 29 de octubre de 2026. Contrasta cualquier duda con el manual de la autoescuela.

## Créditos de las imágenes
Las señales de `img/senales/` proceden de [Wikimedia Commons](https://commons.wikimedia.org/) (archivos `Spain traffic signal …`). La mayoría son de dominio público. Se han añadido únicamente atributos `viewBox` a los SVG para que escalen bien, sin cambiar el dibujo. Estas señales son CC BY-SA y requieren atribución:

| Archivos | Autor | Licencia |
|---|---|---|
| `r400a`, `r400b`, `r400c`, `r500`, `r501`, `r502` | Gigillo83 | [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) |
| `r402` | Majafego | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) |
