# Test DGT · Permiso B

Simulador del examen teórico de la DGT para el permiso de conducir clase B (España), pensado para estudiar: cada respuesta, acertada o fallada, viene explicada.

## Cómo usarlo
Abre `index.html` en el navegador (doble clic) o usa el acceso directo **Test DGT** del escritorio. No necesita instalar nada ni conexión a internet (solo las tipografías cargan de Google Fonts si hay red).

## Qué incluye
- **Examen simulado:** 30 preguntas, 30 minutos, 3 opciones, máximo 3 fallos, sin volver atrás.
- **Modo estudio:** explicación inmediata al contestar, por tema o mezclado.
- **Repasar mis fallos:** solo las preguntas falladas y aún no dominadas.
- **Progreso** guardado en el navegador (`localStorage`): aciertos, preguntas dominadas por tema e historial de exámenes.
- **Banco:** 108 preguntas originales en 13 temas, con figuras (señales, semáforos, líneas, cruces).

## Estructura
- `index.html`: toda la aplicación (HTML, CSS y JS) en un solo archivo. El banco de preguntas está al principio del `<script>`, en llamadas `Q(tema, figura, enunciado, [correcta, falsa1, falsa2], explicación, [porqué falsa1, porqué falsa2], regla)`.
- `contexto.md`: estado y próximos pasos.

## Aviso
Las preguntas son originales (el banco oficial de la DGT no es público) y siguen la normativa vigente en octubre de 2026. Contrasta cualquier duda con el manual de la autoescuela.
