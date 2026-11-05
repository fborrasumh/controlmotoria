# ControlMotorIA

Laboratorio y práctica adaptativa de Control Motor (UMH 949). Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/controlmotoria/

**Idiomas:** español (por defecto), inglés y portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

Construida a partir de la Guía Docente 2026-2027 de la asignatura 949 Control Motor (Grado en Ciencias de la Actividad Física y del Deporte, Facultad de Ciencias Sociosanitarias, Universidad Miguel Hernández de Elche).

## Qué hace

- **Práctica adaptativa** por los 11 resultados de aprendizaje (RA) de la guía: 42 preguntas en tres idiomas y 3 generadores de problemas con solución calculada por código (ley de Hick-Hyman, ley de Fitts, error constante y absoluto). Diagnóstico inicial que recorre los 11 RA, repetición espaciada (10 min, 1, 3, 7, 16 y 35 días), intercalado, prioridad a la unidad de la semana según el cronograma de la guía y a los errores cometidos con seguridad. Cada pregunta explica por qué se ha elegido.
- **Pregunta de seguridad** antes de comprobar (seguro / dudo / adivino) y tabla de calibración.
- **Modelo de dominio por RA** tipo Elo, con olvido por el tiempo, determinista y explicable (mismos eventos → mismo estado).
- **Laboratorio en el navegador** con predicción previa, medición, resultados calculados por código y reflexión: tiempo de reacción simple y de elección (Donders, recta de Hick-Hyman), ley de Fitts (tapping recíproco, recta TM-ID y rendimiento en bits/s), anticipación-coincidencia (EC, EA, EV y E total), sincronización-continuación (CV, deriva, autocorrelación lag-1 de Wing y Kristofferson, asincronía), fatiga (30 s de tapping por bloques de 5 s) y fotogrametría 2D (ángulos articulares con ratón o teclado; la foto no sale del navegador ni se guarda).
- **Clínica de corrección**: tres casos prácticos (anticipación, variabilidad, fatiga) con cuatro criterios. Sin IA, el código detecta los conceptos de cada criterio en la respuesta. Con la clave de cada persona, la IA comenta cada criterio citando literalmente la respuesta; el código verifica cada cita, rebaja a «sin evidencia» lo que la IA da por logrado sin cita real y elimina cualquier nota o calificación.
- **Simulacro** tipo test con la regla de la guía (cada fallo resta 1/(n−1)), nota con y sin penalización, detalle por RA y valor esperado de contestar al azar.
- **Progreso**: dominio por RA, calibración, cronograma, informe Word, copia de seguridad y fichero anónimo (seudónimo) para el profesorado.
- **Panel del profesorado**: carga los ficheros del alumnado y calcula el dominio medio por RA, la analítica de ítems (dificultad, discriminación punto-biserial corregida, distractores que nadie elige) con propuestas de revisión que decide el profesorado, y los resultados de laboratorio del grupo. Exporta el banco a Moodle XML (una categoría por RA, −33,33 % por fallo) y la analítica a CSV.
- Ejemplo completo sin clave (estudiante ficticio y grupo de demostración).

## Cómo se usa la IA

Solo para el feedback de los casos, con la propia clave de OpenAI, Google Gemini o Anthropic Claude. La clave se guarda solo en el navegador. No hace falta servidor. Todo lo demás funciona sin clave y sin conexión.

## Privacidad

Todo se guarda en el navegador (IndexedDB). Solo si se pide feedback de IA sale hacia el proveedor el caso y la respuesta, con correos, DNI/NIE y teléfonos enmascarados y tras un aviso con la muestra exacta. Las fotos no se guardan ni se envían. El fichero para el profesorado lleva un seudónimo y, salvo que se marque, no incluye textos libres; entregarlo es voluntario.

## Límites

- El banco de preguntas y los casos se han redactado para esta app a partir de los temas de la guía y la bibliografía clásica del área: **están pendientes de revisión por el profesorado** antes de usarlos para evaluar.
- Los tiempos del laboratorio dependen del navegador, el teclado y la pantalla (decenas de milisegundos): sirven para comparar condiciones en el mismo dispositivo, no valores absolutos entre personas. No es un equipo de laboratorio.
- La estimación de dominio es inestable con pocas respuestas y no es una calificación.
- La IA puede equivocarse: el código comprueba sus citas, no su criterio pedagógico.
- Probado con IA simulada y pruebas automáticas (lógica en Node, flujo completo en Chromium, accesibilidad con axe-core sin infracciones WCAG 2.2 A/AA en todas las pantallas y los tres idiomas, sin conexión, móvil y CPU ×4). **No se ha probado con una clave real ni con estudiantes reales.**
- Investigar con la app (publicar resultados) requiere aprobación del comité de ética (en la UMH, la Oficina de Evaluación de Proyectos), consentimiento informado, RGPD e, idealmente, un diseño preregistrado con grupo de comparación.

## Evidencia de los mecanismos

Práctica de recuperación (Roediger y Karpicke, 2006, doi:10.1111/j.1467-9280.2006.01693.x), espaciado (Cepeda et al., 2006, doi:10.1037/0033-2909.132.3.354), intercalado (Rohrer y Taylor, 2007, doi:10.1007/s11251-007-9015-8), hipercorrección (Butterfield y Metcalfe, 2001, doi:10.1037/0278-7393.27.6.1491), feedback formativo (Shute, 2008, doi:10.3102/0034654307313795). Laboratorio: Hick (1952, doi:10.1080/17470215208416600), Hyman (1953, doi:10.1037/h0056940), Fitts (1954, doi:10.1037/h0055392), Wing y Kristofferson (1973, doi:10.3758/BF03198607). Estos estudios respaldan los mecanismos, no esta app: su efecto está por medir.

## Adoptarla en otra asignatura o universidad

La asignatura vive en `curriculum.js` (ficha, RA con su texto literal, unidades, cronograma, evaluación y banco de ítems): basta con cambiar ese fichero, traducirlo y publicar.

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y Francisco Javier Moreno Hernández (Universidad Miguel Hernández de Elche).

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573) · Francisco Javier Moreno Hernández [0000-0002-2520-892X](https://orcid.org/0000-0002-2520-892X)


## Cómo citar

Borrás Rocher, F. y Moreno Hernández, F. J. (2026). *ControlMotorIA* (v1.0.0) [Software]. (DOI en trámite)

## Licencia

MIT. Véase [LICENSE](LICENSE).
