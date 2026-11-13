# La idea, a fondo

Documento de trabajo del equipo. Estado a viernes 13 de noviembre de 2026. Sirve de base para construir el MVP.

La idea todavía no tiene nombre. En otras notas de esta carpeta aparece como "Tú primero", que es solo una etiqueta de trabajo.

Cada punto lleva una de estas marcas:

- **[Decidido]** lo ha dicho el equipo.
- **[Propuesto]** salió en el brainstorming o en la maqueta y nadie lo ha rechazado, pero falta que el equipo lo confirme.
- **[Abierto]** sin decidir.

## 1. La idea en corto

Una web para móvil que, antes de enseñarte una cifra de tu plan financiero, te pide que la adivines. Mueves un deslizador con lo que crees, la app te enseña lo que dice tu plan de Sherpas y, justo después, te da la solución que el plan propone para ese punto. Son tres o cuatro preguntas. Al final eliges una sola cosa que hacer y le pones día y hora. Lo que creías queda guardado para que tu asesor prepare la reunión contigo.

## 2. Qué problema resuelve

El reto pide que una familia entienda su plan y actúe. Hoy el plan llega como un informe con muchas cifras, y pasa esto:

- Las cifras grandes no dicen nada si no sabes con qué compararlas. "Tienes 30.000 $ en efectivo" suena bien hasta que ves que son 3,2 meses de gastos.
- Se lee por encima y se olvida. Lo que has intentado adivinar y has fallado se te queda.
- Las malas noticias llegan sin salida, y la gente deja de mirar.
- Un plan con muchas recomendaciones acaba en ninguna acción.
- El asesor no sabe qué pensaba la familia antes de ver el plan. En los cuatro casos del repo el campo de preocupaciones subjetivas dice "None detected".

## 3. Para quién y con qué caso

- **[Decidido]** Caso de la demo: Michael Carter, 37 años, soltero, 180.000 $ de sueldo, nota 26 ("crítico").
- **[Decidido]** Pensado primero para móvil.
- **[Decidido]** Vídeo y pitch en español.
- **[Decidido]** Las preguntas salen de los datos de cada cliente, así que el mismo sistema tiene que valer para los otros casos aunque la demo sea Michael.

## 4. El recorrido completo

1. **Entrada.** Una pantalla que explica qué va a pasar: unas pocas preguntas, primero tu intuición y luego tu plan. Avisa de que el asesor verá las respuestas. **[Propuesto]**
2. **Bloque de pregunta**, repetido tres o cuatro veces. Cada bloque tiene cuatro momentos: pregunta, estimación, revelación y solución. **[Decidido]**
3. **Resumen final.** Lista corta con lo que has visto y un único paso recomendado. **[Decidido]**
4. **Día y hora.** Eliges cuándo vas a hacer ese paso y se guarda como recordatorio. **[Decidido]**
5. **Ficha para el asesor.** Lo que creías, lo que dice el plan y el paso elegido. **[Decidido]**

Barra de progreso visible todo el rato para que se vea que es corto. **[Propuesto]**

## 5. El bloque de pregunta, paso a paso

### 5.1 La pregunta

- **[Decidido]** Se basa en un dato real del cliente y lo nombra: "Tienes 30.000 $ en efectivo. ¿Cuántos meses de gastos crees que te cubren?".
- **[Decidido]** La IA elige qué preguntas hacer y las redacta, partiendo de unas plantillas fijas. No escribe ninguna cifra por su cuenta.
- **[Propuesto]** Solo se pregunta por temas en los que el plan tiene una recomendación, para que cada pregunta pueda acabar en una solución.
- **[Propuesto]** Sin jerga. Si hace falta una palabra técnica, se explica en la misma frase.

### 5.2 La estimación

- **[Decidido]** Las respuestas numéricas se dan con un deslizador.
- **[Propuesto]** El deslizador empieza sin valor (se ve un "?") hasta que lo tocas, para no dar pistas con la posición inicial.
- **[Propuesto]** Debajo del número aparece una frase que lo traduce mientras lo mueves ("eso sería aguantar 4 meses sin sueldo"). Ojo: esa frase es un cálculo nuestro, no una cifra del plan. Ver fuga 5.
- **[Propuesto]** Se puede saltar la pregunta. Nunca es obligatorio adivinar.

### 5.3 La revelación

- **[Decidido]** Se enseña la cifra del plan al lado de la tuya. "Tú pensabas 6 meses. Tu plan dice 3,2."
- **[Propuesto]** Es visual: tu marca y la del plan sobre la misma barra, con un segundo de suspense y el número subiendo. La investigación dice que adivinar ayuda a recordar cuando la comparación se ve, no cuando solo se lee.
- **[Propuesto]** La diferencia se pinta con un color neutro. Nada de rojo y verde ni de "has fallado". El tono es "intuición frente a plan", no examen.
- **[Propuesto]** Hay dos textos preparados por pregunta: uno si el plan sale peor de lo que creías y otro si sale mejor.
- **[Propuesto]** Si la noticia es dura (el dinero se acaba a los 85), antes se pide permiso: "Este dato no es fácil. ¿Quieres verlo ahora?".

### 5.4 La solución

- **[Decidido]** Justo después de la revelación sale la solución del plan para esa pregunta concreta.
- **[Decidido]** Se ve una sola línea. El resto queda plegado en "ver más".
- **[Propuesto]** Un enlace "¿de dónde sale?" enseña el apartado del plan del que viene la cifra.
- **[Propuesto]** Un botón "guardar esta duda para mi asesor" apunta la pregunta en la ficha sin obligar a resolverla en el momento.

## 6. Las preguntas de Michael (como están en la maqueta)

Todas las cifras de esta tabla están en `cases/michael-carter/financial-health.json`, salvo el 23,9 % de ahorro, que viene de `persona.md` e `investment-analysis.json`.

| # | Pregunta | Deslizador | Lo que dice el plan | Solución que se enseña |
|---|---|---|---|---|
| 1 | De cada 100 $ que ganas, ¿cuántos crees que ahorras? | 0 a 50 $ | 23,9 $ (43.000 $ al año) | Ninguna: es una buena noticia. Ver fuga 3 |
| 2 | Tienes 30.000 $ en efectivo. ¿Cuántos meses de gastos crees que te cubren? | 0 a 12 meses | 3,2 meses. Lo recomendado son 5 o 6 (46.530 $ a 55.836 $) | Decidir cómo encajan la casa y el colchón, y tener ese dinero aparte de las inversiones a largo plazo |
| 3 | Hoy tienes 178.717 $ invertidos. Tras comprar la casa en enero de 2027, ¿cuánto crees que quedará? | 0 a 180.000 $ | 81.172 $ | Antes de firmar, revisar de dónde sale la entrada de 113.300 $ |
| 4 | Si te jubilas a los 58, ¿hasta qué edad crees que te llega el dinero? | 60 a 100 años | Hasta los 85. El plan llega a los 91 | Decidir cuánto más va a la jubilación, sabiendo que el dinero del mes va justo |

Las cuatro preguntas están ordenadas de buena noticia a mala noticia, para no empezar asustando. **[Propuesto]**

El plan de Michael trae cinco recomendaciones y son las únicas soluciones que podemos enseñar:

1. Decidir cómo encajan la compra de la casa y el colchón, y separar ese dinero de las inversiones a largo plazo.
2. Valorar cuánto más destinar a la jubilación con un mes a mes tan justo.
3. Revisar el seguro de vida y el seguro de responsabilidad (umbrella) y ver si caben en el presupuesto.
4. Seguir pagando la tarjeta de crédito al 20 %.
5. Comparar la mezcla actual de inversiones con el perfil Growth que eligió.

Además están los tres movimientos que suben la nota: añadir el seguro umbrella (26 a 31, esfuerzo bajo), subir la parte de crecimiento de las inversiones (26 a 31) y bajar las retiradas (26 a 62). El tercero no lo usamos, ver apartado 10.

## 7. El resumen final y el paso con día y hora

- **[Decidido]** Lista corta, no un mapa mental. Una línea por pregunta: lo que creías y lo que dice el plan.
- **[Decidido]** Un único paso marcado como "empieza por aquí". Los demás se ven, pero el recomendado viene ya seleccionado.
- **[Decidido]** Eliges día y hora para hacerlo. La investigación da que quien fija día y hora cumple más que quien solo dice "lo haré".
- **[Propuesto]** El recordatorio se guarda de verdad en el calendario del móvil (archivo .ics) y nombra el objetivo del cliente, no un texto genérico.
- **[Propuesto]** Para Michael, el paso recomendado es el de menos esfuerzo según su plan: pedir presupuesto del seguro umbrella. Sube la nota de 26 a 31.
- **[Decidido]** La app no mueve dinero. Solo sugiere y pide confirmación.
- **[Abierto]** Un "ver todo el plan" secundario para quien quiera más. No hace falta para el MVP.

## 8. La ficha para el asesor

- **[Decidido]** Guarda lo que el cliente creía en cada pregunta junto a la cifra del plan. Sirve para preparar la reunión uno a uno.
- **[Propuesto]** También guarda las dudas aparcadas y el paso elegido con su fecha.
- **[Propuesto]** El cliente sabe desde la primera pantalla que el asesor lo verá.
- Es la parte más original de la idea de cara al jurado: rellena un hueco que el plan de Sherpas tiene hoy vacío.

## 9. Reglas que no se rompen

1. **[Decidido]** Las cifras son siempre las del plan de Sherpas. Las pone el código leyendo el JSON, no la IA.
2. **[Decidido]** La IA solo elige preguntas y redacta frases a partir de plantillas.
3. **[Decidido]** Un verificador comprueba que cada número que aparece en pantalla está en los datos del caso. Si no está, no se enseña.
4. **[Decidido]** No se inventan escenarios. El plan trae uno solo (con casa en 2027), así que no hay "¿y si no la compro?".
5. **[Decidido]** Nada mueve dinero.
6. **[Propuesto]** Si se usa voz, la voz nunca dice cifras. Las cifras se leen en pantalla.

Cuidado al leer los datos. El JSON trae en `key_metrics.facts` las cifras oficiales con su etiqueta y avisa de con qué no confundirlas. Dos ejemplos que ya nos han salido:

- Efectivo: 30.000 $ es el efectivo accesible (banco más fondo monetario) y da 3,2 meses. En otro apartado aparece 27.000 $ y 2,9 meses, que es solo el banco. Usamos el de `key_metrics`.
- Invertido: el resumen del plan habla de 145.000 $ invertibles y la proyección anual da 178.717 $ en 2026. Hay que confirmar con los mentores cuál toca enseñar en la pregunta 3.

## 10. Lo que hemos descartado dentro de esta idea

| Qué | Por qué | Estado |
|---|---|---|
| Hacer todas las preguntas seguidas como un formulario y dar las soluciones al final en un mapa mental | La solución pierde fuerza si llega minutos después de la pregunta, y un mapa mental en el móvil se lee mal. Queda la versión por bloques con lista corta al final | Descartado |
| Cinco preguntas con cinco soluciones | Vuelven a ser demasiadas opciones. Tres o cuatro preguntas y un solo paso recomendado | Descartado |
| Empezar con "¿qué te quita el sueño?" | No vemos claro poder montar ese cuestionario. Está en la maqueta, pero no en la entrega | Fuera por ahora |
| Modo pareja (cada uno contesta en su móvil y luego se compara) | No lo tenemos claro y Michael vive solo | Fuera por ahora |
| Que la IA calcule o diga las cifras | No nos fiamos y el reto pide no inventar. La IA elige y redacta, el código pone el número | Descartado |
| Simular "¿y si no compro la casa?" | El plan solo trae el escenario con casa. Habría que inventar números | Descartado |
| Usar el movimiento que sube la nota de 26 a 62 | Habla de bajar retiradas a 10.300 $ al año y confunde más que ayuda | Descartado |
| Puntos, medallas, rachas | Quitan seriedad a decisiones importantes y dan aspecto de juego | Descartado |
| Abrir enseñando la nota 26 "crítico" | Asusta y hace que la gente no siga | Descartado |
| Marcar la diferencia en rojo o decir "has fallado" | Se siente como un examen y a nadie le gusta suspender | Descartado |
| Diseño muy colorido | En finanzas resta confianza. Buscamos algo sobrio, tipo banco, con la emoción puesta en la revelación | Descartado |
| Ponerle nombre ya | No está decidido | Pendiente |

## 11. Fugas que conocemos

1. **Soluciones repetidas.** El plan solo tiene cinco recomendaciones. El colchón y la casa comparten la misma, así que dos bloques seguidos pueden sonar igual.
2. **El deslizador da pistas.** El rango y el punto medio orientan la respuesta. Empezar en "?" ayuda, pero el rango sigue ahí.
3. **La pregunta con buena noticia no tiene solución.** La del ahorro acaba en "esto ya lo haces bien". Hay que decidir si se queda como arranque amable o se cambia.
4. **Quien acierta no se sorprende.** Hace falta un texto para ese caso que no sea un simple "correcto".
5. **Las frases en vivo son cálculos nuestros.** "Eso serían X $ al año" no sale del plan. O se etiqueta como cuenta nuestra, o se limita a operaciones evidentes, o se quita.
6. **El paso de la casa depende del asesor.** "Revisa de dónde sale la entrada" no se hace solo en dos minutos.
7. **Vergüenza.** Saber que el asesor ve lo que has fallado puede hacer que la gente conteste con cuidado o no conteste.
8. **Tiempo.** El recorrido dura unos tres minutos y el pitch son dos. En la demo hay que enseñar una o dos preguntas, no las cuatro.
9. **Recordar no es actuar.** La investigación apoya que adivinar mejora el recuerdo, no que mueva a hacer algo. Por eso el paso con día y hora no es opcional.
10. **Buenas sorpresas.** Si el plan sale mejor de lo que creías, la gente se relaja. Ese texto tiene que seguir llevando a un paso.

## 12. Sin decidir

- Nombre.
- Si al final entra la pregunta inicial de preocupaciones, en versión de una sola pantalla.
- Si se enseña modo pareja como ampliación con otro caso.
- Si hay voz y para qué.
- Cuántas preguntas en la demo: tres o cuatro.
- Qué se hace con la pregunta de buena noticia (fuga 3) y con las frases en vivo (fuga 5).
- Qué cifra de "invertido" se usa en la pregunta 3.
- Si las preguntas se generan en directo con la IA en la demo o se dejan generadas de antemano y revisadas.

## 13. Piezas que salen de aquí para el MVP

Esto no es el plan de trabajo, solo la lista de lo que la idea obliga a construir.

- Lector del caso: saca del JSON las cifras oficiales con su etiqueta y su apartado de origen.
- Plantillas de pregunta: texto con huecos, rango del deslizador, cifra del plan, los dos textos de revelación, la solución asociada y la fuente.
- Selector de preguntas: la IA elige tres o cuatro plantillas según los datos del cliente y ajusta la redacción.
- Verificador: rechaza cualquier número en pantalla que no esté en los datos.
- Pantallas: entrada, pregunta con deslizador, revelación con solución, resumen con día y hora, ficha del asesor.
- Recordatorio: archivo de calendario con el paso y el objetivo del cliente.

Material relacionado: maqueta navegable de Michael (enlace privado, lo comparte Hugo), [investigacion-profunda.md](investigacion-profunda.md) para las fuentes y [decisiones.md](decisiones.md) para el resto de ideas descartadas.
