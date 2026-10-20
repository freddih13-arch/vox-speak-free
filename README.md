# VOX Speak · Islands v2

**Entrenador personal de inglés práctico (A2 → B1/B2), totalmente sin cuotas de suscripción**. Diseñado para practicar comprensión auditiva de preguntas inesperadas, respuestas orales, ventas B2B, inglés para entrevistas, fintech y networking.

## Qué está incluido

- 10 islas temáticas originales con 100 frases gratuitas, sin lecciones bloqueadas.
- Crea tus propias islas (2 a 40 frases por isla) y guárdalas en tu navegador.
- Tres modos: shadowing/repetición, recuperación activa del español al inglés y dictado a ciegas.
- Lectura en voz alta TTS, selector de voz inglesa US/UK (si el dispositivo ofrece las voces), velocidad ajustable.
- Evaluación comparando **secuencialmente** palabras esperadas con la transcripción del motor de reconocimiento de voz del navegador; marca omisiones/sustituciones y permite oír palabras aisladas.
- Graba y escucha tu propia voz. La grabación temporal permanece en la pestaña y se descarta al cambiar de frase.
- Historial y etapas de repaso espaciado por frase, revisión de progreso y exportación/importación de copia JSON.
- **Mi camino con el inglés:** bitácora fechada de avances y dificultades con exportación a Markdown para documentar cómo aprendiste inglés.
- Training existente: listening con opción múltiple, pronunciación y entrevistas simuladas.
- Progressive Web App (PWA) con manifest e interfaz en caché para acceso sin conexión. **La voz sintética y el reconocimiento pueden requerir conexión** según el navegador.

## Uso Android

1. Abre https://freddih13-arch.github.io/vox-speak-free/ en Chrome actualizado.
2. Abre la pestaña **Islas** y escoge un escenario.
3. Pulsa **Escuchar**, luego **Hablar** y permite el micrófono.
4. En **Traduce sin mirar** responde la frase en inglés desde el español. En **Dictado a ciegas** escribe lo que oíste.
5. En Chrome, menú > **Agregar a pantalla principal / Instalar aplicación**, si aparece.

## Límites técnicos, honestidad y privacidad

**No se usa el motor ELSA ni se garantiza una corrección perfecta de fonemas, entonación o acento.** Web Speech Recognition genera texto, no puntuaciones fonéticas. VOX utiliza una métrica denominada *coincidencia de palabras reconocidas* — proxy útil de inteligibilidad, pero no una medida precisa de pronunciación. Las voces disponibles dependen del dispositivo y navegador. El sistema de reconocimiento de Chrome puede enviar audio a un servicio externo gestionado por el navegador. La aplicación no dispone de backend, base de datos externa ni cuentas de usuario. Estadísticas e islas personalizadas se guardan en `localStorage` del navegador: pueden perderse al borrar datos, cambiar dispositivo o usar modo incógnito. Usa **Copia de islas** para preservar tu progreso.

## Código / arquitectura

- `index.html` — versión inicial y navegación.
- `islands-data.js` — banco editorial original (100 frases).
- `islands.js` — islas, comparador de transcripción de voz mediante alineamiento de tokens, prácticas y estadísticas.
- `islands.css` — diseño móvil.
- `manifest.webmanifest`, `sw.js`, `icon-*.png` — instalación y caché PWA.

## Próxima iteración

Evaluación fonética con modelo acústico local u hospedado, dependiendo de la fiabilidad y el costo real; calibración contra grabaciones humanas; diálogos adaptativos con transcripción auditada; cuentas opcionales y sincronización segura multi-dispositivo. Sin reclamar nivel CEFR ni evaluación acústica antes de validarlas.

Proyecto educativo independiente, inspirado por prácticas populares como shadowing e islas lingüísticas, sin código, frases ni interfaz copiados de ELSA o HyperLingua.