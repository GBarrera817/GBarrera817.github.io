---
version: 1
slug: "index-html"
primary_target: "index.html"
related_targets: []
---

Scope: index.html, portafolio de una página. Mode: experience.
Audience/job: reclutadores y colegas; entender quién es Gabriela, explorar sus proyectos y contactarla (email, LinkedIn, GitHub; nunca teléfono).
Constraints: GitHub Pages estático; proyectos privados sin enlace; sin datos inventados.

## Direction contract
THESIS: El portafolio es una terminal: se explora escribiendo comandos (help, ls, cat <proyecto>, open <proyecto>, exp, contacto). Rechaza la landing de hero + tarjetas; la única interfaz es la sesión.
OWN-WORLD: Sesión de terminal a pantalla completa sobre negro verdoso, texto fósforo verde, ámbar para nombres/comandos resaltados, rojo solo para errores; JetBrains Mono en todo; barra de estado estilo tmux al pie (sesión, ventana, hora de La Serena); salidas con tablas de caracteres de caja; neofetch con logo ASCII "GB". Sin glow de neón ni bordes brillantes.
STORY: Al cargar se "escribe" neofetch (quién es), luego la pista "escribe help". El visitante lista proyectos, los abre con cat/open o clic, ve experiencia y termina en contacto.
FIRST VIEWPORT: Terminal de alto completo: neofetch (logo GB + ficha) arriba, prompt activo con cursor parpadeando, fila de comandos sugeridos clicables sobre la barra tmux.
FORM: seed: none (pinned) — "algo como una terminal de hacker, en donde los proyectos se puedan acceder desde un comando de terminal"
Signature interaction: autocompletado con Tab e historial con ↑/↓; cada nombre de proyecto en una salida es clicable y ejecuta `cat <proyecto>`.
FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance
