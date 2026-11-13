# Estado actual

> **Actualización 13 nov, 19:45.** Para la entrega del viernes el equipo ha decidido: la idea aún no tiene nombre ("Tú primero" es solo una etiqueta de estas notas), se quita la apertura "¿qué te quita el sueño?" y se quita el modo pareja por ahora. Lo que sigue en pie es el bucle de adivinar, revelar y solución con Michael, y un único paso con día y hora. El resto de este archivo es anterior a esa decisión.


Última actualización: viernes 13 nov 2026, 20:05.

## En una frase
Todavía no hay idea final. Hay dos candidatas y cinco piezas que se mantienen en cualquiera de las dos. Hoy no se construye nada: solo se elige idea.

## Fechas
- **Vie 13 nov, 22:00:** entrega de la idea en Discord con `/entrega` (una página en viñetas: qué, por qué y qué se descarta). Se puede cambiar de idea después.
- **Mié 18 nov, 23:59:** repo público, MVP, vídeo de 2 minutos y media página.
- **Jue 19 nov, 12:45:** pitch de 2 minutos. Es lo que puntúa el jurado; el vídeo no cuenta en la nota.

## Piezas que se mantienen sea cual sea la idea
1. **El plan llega cuando hay que decidir.** Michael Carter firma una casa de 550.000 $ en enero de 2027.
2. **"¿Qué te quita el sueño?"** La app empieza preguntando. En los cuatro casos el campo de preocupaciones subjetivas pone "None detected".
3. **Cifras traducidas a vida diaria**, con un verificador: las cifras salen de los datos por código y la IA solo redacta.
4. **Un solo primer paso**, que la familia confirma, con recordatorio real. Nada mueve dinero.
5. **Ficha para el asesor** con lo que la familia siente, entendió y se comprometió a hacer. El cliente de Sherpas es el asesor.

## Idea A: "La llamada" (también llamada "Sobremesa")
A Michael le llama su yo de 58 años, el día que se jubila y en su mejor momento económico según el plan. Le explica el plan antes de firmar la casa y le vuelve a escribir el día 3 y el día 30.

Dudas del equipo (13 nov): puede no funcionar con parejas y familias, y puede molestar a algunas personas.

## Idea B: "Tú primero"
Antes de enseñar cada dato, la app pide a la familia que lo adivine y luego revela lo que dice su plan.
- Michael: "¿Hasta qué edad crees que te llega el dinero?" El plan dice 85.
- Samantha: tiene un 82, "fuerte", pero sus ahorros se acaban a los 73.
- Los Weah: cada uno responde por separado en su móvil y luego comparan.
- La diferencia entre lo que creían y lo que dice el plan va a la ficha del asesor.
- El pitch se abre haciendo adivinar al jurado en directo.

## Idea C: la combinación que recomienda Claude tras la investigación (13 nov, 18:50)
Nombre provisional: "Tú primero". Junta la idea B con lo mejor de lo investigado ([investigacion-profunda.md](investigacion-profunda.md)).

1. **Cartas antes que cifras.** Cada persona elige en privado, en su móvil, qué le quita el sueño y qué quiere proteger. En pareja, ninguno ve lo del otro hasta que los dos contestan.
2. **Adivina y revela, en visual.** Tres a cinco datos del plan, con un deslizador. Se revela el dato, la distancia con su intuición y una frase que lo traduce a su vida. Sin "correcto" ni "incorrecto", y siempre con el botón "prefiero verlo directamente".
3. **Malas noticias con permiso.** Primero "¿quieres verlo ahora?", luego una frase, y la salida en la misma pantalla.
4. **Un solo paso, con día y hora**, que va al calendario. Nada mueve dinero.
5. **Aparcar preguntas.** Un toque guarda la duda para el asesor.
6. **Ficha para el asesor**: qué le preocupa a cada uno, qué creían frente a lo que dice el plan, en qué no coinciden, sus preguntas y el paso elegido.
7. **Si hay voz, nunca dice cifras.** Las cifras van escritas en pantalla y salen de los datos por código.

Nota estimada: 92. Fugas: mejora el recuerdo pero no hay prueba de que mueva a actuar (por eso el paso con fecha); con una sola persona pierde la parte de pareja; un desacuerdo sin moderador puede acabar en discusión.

## Objeciones del equipo a la idea A (13 nov)
- A Dani no le convence que le hable un yo del futuro: puede resultar raro de ver.
- Hugo duda de la fiabilidad de las cifras dichas en una llamada.
- La investigación lo apoya: el efecto medido del yo futuro es pequeño y BBVA ya lo hizo en España.

## Flujo elegido para probar: híbrido (13 nov, 20:00)
El equipo construyó el ciclo **pregunta, estimación con deslizador, revelación y solución**. La IA elige qué preguntar según el análisis de cada familia; las cifras son siempre las del plan de Sherpas.

Se compararon dos flujos: bloques con la solución al momento, o formulario con un mapa mental al final. Claude recomienda un híbrido:
- Tres o cuatro preguntas con barra de progreso. La primera, con buena noticia.
- Tras cada revelación, una sola frase de solución. El resto, plegado.
- Pantalla final con una lista corta: un paso marcado como "empieza por aquí" y selector de día y hora.
- El mapa completo queda como vista secundaria.
- La ficha del asesor recoge lo que la persona creía, sus dudas y el paso elegido.

Hay una maqueta para tocar con el caso de Michael Carter (pedid el enlace a Hugo, es privado).

Fugas nuevas vistas al montarla:
1. El plan repite soluciones: colchón y casa llevan a la misma recomendación. Elegir preguntas con soluciones distintas.
2. El rango y la posición inicial del deslizador dan pistas.
3. La pregunta de buena noticia no tiene solución: va como "esto ya lo haces bien".
4. Quien acierta no tiene sorpresa: hace falta un guion para ese caso.
5. Las frases en vivo bajo el deslizador son cálculos nuestros: hay que marcarlas.
6. El paso de la casa depende de tener asesor: hace falta versión sin asesor.
7. Al asesor le llega "creía 95, el plan dice 85": avisar bien y dejar no compartirlo.
8. El recorrido dura unos tres minutos y el pitch dos.
9. Con Michael solo no se ve la parte de pareja.

## Preguntas abiertas para el equipo (actualizadas)
1. ¿Aceptáis la idea C como base para la entrega de hoy?
2. ¿Caso principal: los Weah (pareja) con 20 segundos de Michael, o al revés?
3. ¿Con voz que narra sin decir cifras, o sin voz?
4. ¿Qué nombre le ponemos?
