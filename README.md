# Test DGT · Permiso B

Simulador del examen teórico de la DGT para el permiso de conducir clase B (España), pensado para estudiar: cada respuesta, acertada o fallada, viene explicada.

## Cómo usarlo
Abre `index.html` en el navegador (doble clic) o usa el acceso directo **Test DGT** del escritorio. No necesita instalar nada ni conexión a internet (solo las tipografías cargan de Google Fonts si hay red).

## Qué incluye
- **Examen simulado:** 30 preguntas, 30 minutos, 3 opciones, máximo 3 fallos, sin volver atrás.
- **Modo estudio:** explicación inmediata al contestar, por tema o mezclado.
- **Repasar mis fallos:** solo las preguntas falladas y aún no dominadas.
- **Progreso** guardado en el navegador (`localStorage`): aciertos, preguntas dominadas por tema e historial de exámenes.
- **Banco:** 143 preguntas originales en 13 temas (48 de señales).
- **Gráficos:** señales oficiales españolas (`img/senales/`), semáforos, líneas, cruces con vehículos y esquemas propios (distancia de detención, regla de los 2 segundos, aquaplaning, posición lateral de seguridad, reposacabezas) que aparecen en la explicación tras contestar.

## Estructura
- `index.html`: toda la aplicación (HTML, CSS y JS) en un solo archivo. El banco de preguntas está al principio del `<script>`, en llamadas `Q(tema, figura, enunciado, [correcta, falsa1, falsa2], explicación, [porqué falsa1, porqué falsa2], regla)`.
- `img/senales/`: señales de tráfico en SVG, una por archivo, con el código oficial de la señal como nombre (`r2.svg` = STOP, `p13a.svg` = curva peligrosa a la derecha…).
- `contexto.md`: estado y próximos pasos.

## Aviso
Las preguntas son originales (el banco oficial de la DGT no es público) y siguen la normativa vigente en octubre de 2026. Contrasta cualquier duda con el manual de la autoescuela.

## Créditos de las imágenes
Las señales de `img/senales/` proceden de [Wikimedia Commons](https://commons.wikimedia.org/) (archivos `Spain traffic signal …`). La mayoría son de dominio público. Se han añadido únicamente atributos `viewBox` a los SVG para que escalen bien, sin cambiar el dibujo. Estas señales son CC BY-SA y requieren atribución:

| Archivos | Autor | Licencia |
|---|---|---|
| `r400a`, `r400b`, `r400c`, `r500`, `r501`, `r502` | Gigillo83 | [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) |
| `r402` | Majafego | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) |
