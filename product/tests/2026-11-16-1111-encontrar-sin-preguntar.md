---
opportunity: encontrar-sin-preguntar
solutions: product/solutions/2026-11-13-1845-encontrar-sin-preguntar.md
status: ready
---

# Solution tests for: Lo que el grupo ya recomendó no se encuentra, y se vuelve a preguntar

## Why test
Están en prueba A2 (planilla compartida, la principal) y A3 (paquete de
contactos para la agenda, el contraste). En las dos el dolor está evidenciado
(10 entrevistas reales), pero nadie reaccionó todavía a ninguna de las dos
soluciones: que a 10 de 10 "les vendría bien una lista" es opinión, y 0 de 10
sostuvieron una lista. No sabemos si alguien además de Martín carga la
planilla, si los vecinos piden acceso, ni si importan un paquete de contactos.

Orden de corrida: **T1 → T3 → T2.** T1 produce el contenido con
consentimiento que usan T3 y T2. T3 va antes de T2 para que tener la planilla
no les saque a las casas el motivo para importar el paquete.

## T1. planilla-compartida: los que responden cargan la planilla
- **Test status:** analyzed
- **Belief under test:** "La planilla se mantiene viva con editores además de Martín: al menos 3 personas además de Martín agregan o corrigen un profesional." (`product/overview.md`, creencia 7b)
- **Risk:** [value]
- **Test type:** concierge
- **What we do:** Martín arma la planilla vacía, sólo con la estructura, y la
  comparte como editores con 4 o 5 vecinos de los que siempre responden.
  Les pide lo mismo a todos: "cargá los profesionales que recomendás", con
  el pedido de que cada uno le pida el consentimiento al profesional que carga
  (es quien tiene la relación con él). Hasta tener el "sí", la fila queda como
  `pendiente`. Martín manda a lo sumo un recordatorio y no carga por ellos.
- **With whom:** 4 o 5 de los que siempre responden en el grupo: V5 (se
  ofreció) y los que se identifiquen en el chat como quienes más pasan
  contactos. Martín los invita por privado. Corrida real: 6 editores; Roberto
  se sumó el mismo día por ser el que más contactos pasa en el grupo (decisión
  del PM, ver `product/corrections.md`). El umbral no cambia.
- **Material needed:** una Google Sheet de trabajo, compartida sólo con los
  editores, con las columnas rubro, nombre, zona, quién recomienda,
  comentario, teléfono y consentimiento (`sí` / `pendiente`). Un texto fijo
  de invitación que incluya el pedido de consentimiento y cómo pedirlo. La
  hoja de captura, por editor: profesionales agregados, correcciones, fecha
  de cada carga, si cargó solo o con Martín, cuántos con consentimiento `sí`.
  Queda afuera: formulario de sugerencias para no editores, filtros, formato,
  cualquier acceso de otros vecinos.
- **Material:** `product/tests/materials/t1-planilla-compartida/` (guion, mensajes, planilla de trabajo, hoja de captura)
- **Duration:** 2 días por editor (48 h desde que recibe el acceso), con un
  recordatorio a las 24 h. Cambiado de 14 días por el PM el 2026-11-16, antes
  de correr, para que la prueba no se haga larga (ver `product/corrections.md`).
  Límite: si falla, puede ser por falta de tiempo y no de ganas; cargar 2
  profesionales lleva minutos, así que la ventana alcanza para la señal.
- **Signal and threshold:** editores, sin contar a Martín, que agregan 2
  profesionales o más cada uno, según el historial de versiones. Pasa con al
  menos 3 editores. Falla con 1 editor o ninguno. Cuántos profesionales tienen
  consentimiento se registra aparte y no cuenta para el umbral.
- **Decision rule:** continue si 3 o más editores cargan 2 profesionales o más
  cada uno · change si cargan sólo 2, o si cargan sólo cuando Martín se sienta
  con ellos (la versión pasa a "ellos dictan, Martín carga" y necesita su
  propia prueba) · discard si carga 1 editor o ninguno: A2 depende de Martín
  tanto como A4, y vuelve A4 con un número compartido entre varios editores.
- **Expected provenance:** real
- **Next step if it passes:** T2 (creencia 7a). El mantenimiento sostenido
  (correcciones a lo largo del tiempo) se mide en el piloto de 8 semanas.

## T2. planilla-compartida: pedido de acceso en el grupo
- **Test status:** ready
- **Belief under test:** "Cuando un vecino necesita un profesional, abre la planilla en vez de ir a su agenda o al grupo. En 8 semanas, durante la temporada de noviembre a enero, al menos 15 de las 44 casas la abren." (`product/overview.md`, creencia 7a)
- **Risk:** [value]
- **Test type:** access-request
- **What we do:** con T1 pasado y al menos 10 profesionales con
  consentimiento que cubran al menos 3 de los 5 rubros más pedidos
  (piletero, plomero, gasista, atmosférico, cerrajero), Martín manda un
  solo mensaje en el grupo con el link a la planilla de vecinos (acceso
  restringido): "acá están los profesionales que el barrio recomienda; pedí
  acceso con tu Gmail". Si Gabriela está de acuerdo, lo fija. Sin
  recordatorios por privado.
- **With whom:** las 44 casas, a través del grupo de WhatsApp.
- **Material needed:** una Google Sheet de vecinos, separada de la de
  trabajo, sólo con las filas con consentimiento `sí`, acceso restringido y
  sin permiso de edición para los vecinos. El texto fijo del mensaje del
  grupo. La hoja de captura: cada pedido de acceso con fecha y la casa a la
  que corresponde (dos personas de la misma casa cuentan una vez), y cuántos
  leyeron el mensaje en el grupo. Queda afuera: formulario de sugerencias,
  links por rubro, cualquier recordatorio.
- **Material:** `product/tests/materials/t2-planilla-compartida/` (guion, mensajes, planilla de vecinos, hoja de captura, resumen)
- **Duration:** 7 días.
- **Signal and threshold:** casas distintas que piden acceso. Pasa con 20 o
  más. Falla con menos de 15: con menos de 15 casas con acceso, la 7a no puede
  cumplirse.
- **Decision rule:** continue con 20 casas o más · change con 15 a 19: el
  interés existe pero la entrada frena; se prueba otra versión (links directos
  por rubro, o mandar la planilla cada vez que alguien pide en el grupo) ·
  discard con menos de 15: vuelve A4. Si falla, separar "no lo vieron" de "no
  les interesa" con el número de lectores del mensaje (Daniel y otros como él
  silencian el grupo).
- **Expected provenance:** real
- **Next step if it passes:** piloto de 8 semanas durante la temporada,
  midiendo aperturas reales con la actividad de Drive (la 7a completa: al
  menos 15 de las 44 casas la abren) y correcciones de editores (7b
  sostenida).

## T3. contactos-a-la-agenda: paquete por privado
- **Test status:** analyzed
- **Belief under test:** "Las casas que reciben el paquete de contactos lo importan a la agenda: al menos la mitad de las casas que lo reciben." (`product/overview.md`, creencia 8a)
- **Risk:** [value]
- **Test type:** concierge
- **What we do:** con los profesionales con consentimiento de T1, Martín le
  manda el paquete por privado a 12 casas, con un texto fijo: "te paso los
  profesionales que recomienda el barrio, para que los tengas en la agenda".
  Un solo mensaje, sin recordatorios. A los 7 días pregunta: "¿buscás
  'Sauces' en tu agenda? ¿cuántos te aparecen?".
- **Corrida real (decisión del PM, 2026-11-17):** arranca en paralelo con T4,
  con un paquete de 3 contactos (los únicos con consentimiento: jardinero,
  bombas, plomería y piletas). Ver `product/corrections.md`.
- **With whom:** 12 casas que no hayan sido editoras en T1, mezclando casas
  que piden en el grupo con casas que sólo leen (como Daniel). Las elige
  Martín.
- **Material needed:** los contactos con consentimiento `sí` como tarjetas de
  contacto de WhatsApp (se agregan con un toque), no como archivo .vcf, con el
  nombre en el formato "Sauces · {Rubro} {Nombre} (rec. {quién recomienda})".
  El texto fijo del envío y la pregunta del día 7. La hoja de captura, por
  casa: si pide en el grupo o sólo lee, fecha de envío, cuántos contactos
  "Sauces" tiene en la agenda al día 7 y comentarios espontáneos. Queda
  afuera: la planilla, explicaciones de cómo importar y cualquier recordatorio.
- **Material:** `product/tests/materials/t3-contactos-a-la-agenda/` (guion, mensajes, contactos, hoja de captura). `contactos.csv` se completa al cierre de T1 con los profesionales con consentimiento "sí".
- **Duration:** 7 días.
- **Signal and threshold:** casas que tienen los contactos en la agenda al día
  7 (al menos uno "Sauces" en su agenda, verificado en la consulta). Pasa con
  6 de 12 o más. Falla con menos de 4 de 12.
- **Decision rule:** continue con 6 o más · change con 4 o 5: el interés
  existe pero importar frena; se prueba otra versión (por ejemplo, cada
  contacto por separado) · discard con menos de 4: tener los contactos en
  el teléfono no alcanza para que la gente haga el paso de importarlos.
- **Expected provenance:** real
- **Next step if it passes:** 8b: a las 8 semanas, consultar a las casas que
  importaron y contrataron en el período si usaron un contacto del paquete
  (al menos 1 de cada 3).

## T4. planilla-compartida: planilla precargada (rediseño de T1)
- **Test status:** analyzed
- **Belief under test:** "La planilla se mantiene viva con editores además de Martín: al menos 3 personas además de Martín agregan o corrigen un profesional." (`product/overview.md`, creencia 7b)
- **Risk:** [value]
- **Test type:** concierge
- **What we do:** Martín precarga la planilla de trabajo con los 41
  candidatos de `materiales/candidatos-profesionales-interno.csv` (rubro,
  nombre, teléfono; "Quién recomienda" y "Comentario" vacíos) y les avisa a
  los editores: "ya está cargado lo que teníamos; ¿ponés tu nombre en los que
  recomendás, corregís lo que esté mal y sumás los que falten?". La planilla
  de los editores no tiene columna de consentimiento: lo gestiona Martín
  internamente en el CSV de candidatos (decisión del PM, ver
  `product/corrections.md`). Un recordatorio a las 24 h. Después de la
  precarga, Martín no toca la planilla.
- **With whom:** los mismos 6 editores de T1. Ya conocen la prueba, pero 3
  de ellos pidieron esta versión: mide si ese pedido era en serio. No hay
  otro grupo comparable (los que pasan contactos seguido son pocos).
- **Material needed:** la precarga (41 filas, sin columna de consentimiento), el texto del
  aviso, el recordatorio y la hoja de captura por editor (acciones por tipo,
  cómo actuó, rubros de lo agregado). Queda afuera: planilla de vecinos,
  formularios, formato.
- **Material:** `product/tests/materials/t4-planilla-compartida/` (guion, mensajes, precarga, hoja de captura)
- **Duration:** 48 h por editor desde el aviso. Se cierra recién cuando se
  cumplen las 48 h del último editor (T1 quedó inconclusive por cerrarse
  antes).
- **Signal and threshold:** editores, sin contar a Martín, con 2 acciones o
  más. Acción = firmar una fila ("Quién recomienda"), corregir un dato o
  agregar un profesional. Pasa con al menos 3 editores. Falla con 1
  editor o ninguno. Lo agregado en rubros que faltan (plomero, gasista,
  piletero) se registra aparte y no cuenta para el umbral.
- **Decision rule:** continue si 3 o más editores tienen 2 acciones o más
  (sigue T3, y T2 si se llega a 10 profesionales con consentimiento) ·
  change si son 2, o si actúan sólo con Martín al lado (versión "ellos
  dictan, Martín carga", con su propia prueba) · discard si es 1 o ninguno:
  ni precargada la mantienen otros; A2 descartada y vuelve A4 con un número
  compartido entre varios editores.
- **Expected provenance:** real
- **Next step if it passes:** T3, con los profesionales que queden en `sí`.

## Results

### T1. planilla-compartida: los que responden cargan la planilla
- **Observado:** 6 editores invitados, de los que siempre pasan contactos en
  el grupo, todos el 2026-11-16 (Roberto, el último, se sumó ese día y
  recibió el acceso el 2026-11-17). Los 6 aceptaron. La
  prueba se cerró el 2026-11-17, antes de completar las 48 h por editor
  (decisión del PM; ver `product/corrections.md`). Según Martín, ningún
  editor cargó profesionales; el historial de versiones no se verificó.
  - 3 de 6 pidieron que la planilla venga cargada o que cargue Martín
    (Valentina: "¿no podés cargar la info de antemano?"; vecino 5: "¿no se
    puede cargar la info que ya tenemos?"; vecino 4 mandó un atmosférico para
    que lo cargue Martín).
  - 2 de 6 lo dejaron para "después" (José María: "¡la planilla está
    vacía!"; vecino 3).
  - Tras el recordatorio de las 24 h: uno "me olvidé", otro "no tengo
    tiempo".
  - Roberto recibió el acceso el día del cierre; en la semana previa pasó 2
    contactos por el grupo.
- **Con quién y cuántos:** 6 vecinos del segmento (los que responden en el
  grupo).
- **Provenance:** real
- **Result:** inconclusive. La prueba se cerró antes de la duración diseñada
  (48 h por editor) y el historial de versiones no se verificó.
- **Decision:** ninguna sobre A2. Ver Decision.

### T3. contactos-a-la-agenda: paquete por privado
- **Observado:** paquete de 3 contactos (jardinero Teófilo, bombas Leo
  Gisbert, plomería y piletas Fernando) enviado por privado a 12 casas (UF 1
  a UF 12) el 2026-11-17. Las 12 acusaron recibo ("ok, gracias", "dale",
  👍…); 3 de 12 dijeron preferir la planilla ("me gustaba más el Excel",
  "la planilla me gusta más", "el Excel está más lindo"), 1 pidió "un lugar
  donde queden guardados", 1 preguntó por la web. La pregunta del día 7 se
  adelantó al mismo día del envío (decisión del PM de cerrar hoy; ver
  `product/corrections.md`). Respondieron 7: 3 con 0 contactos ("nada",
  "nada", "Sauces, no tengo nada") y 4 no medibles ("tengo agendados a los
  vecinos" y 3 personas con "todos los vecinos se llaman Sauces al final").
  5 sin respuesta. Ninguna casa confirmó tener un contacto del paquete.
- **Desvíos del diseño:** (1) consulta el día 0 en vez del día 7; (2) 3 de
  las 12 casas son editoras de T4 (el diseño pedía casas que no lo fueran);
  (3) el marcador "Sauces" de la consulta choca con cómo los vecinos se
  agendan entre sí, así que la búsqueda no distingue los contactos del
  paquete.
- **Con quién y cuántos:** 12 casas del barrio, elegidas por Martín.
- **Provenance:** real
- **Result:** inconclusive. La señal no se pudo capturar como estaba diseñada
  (marcador ambiguo) y la consulta se hizo el día del envío. No es `failed`:
  que nadie confirmara no prueba que nadie importó.
- **Decision:** ninguna sobre A3. Si se rehace: preguntar por el nombre del
  profesional ("¿te aparece Teófilo, Gisbert o Fernando?") o usar un
  marcador que nadie use ya, y respetar los 7 días.

### T4. planilla-compartida: planilla precargada
- **Observado:** planilla precargada con los 41 candidatos; aviso a los 6
  editores el 2026-11-17. Respuestas entusiastas ("¡Piola, che!", "Esto nos
  ahorra la búsqueda", "Muy bueno... después lo miro bien"), 3 menciones de
  una web y una advertencia de Valentina ("todos pueden modificar los
  datos"). Según el historial de versiones, ningún editor editó la planilla:
  0 filas firmadas, 0 correcciones, 0 profesionales agregados. Se cerró el
  mismo día del aviso, antes de las 48 h por editor (decisión del PM; ver
  `product/corrections.md`).
- **Con quién y cuántos:** los mismos 6 editores de T1.
- **Provenance:** real
- **Result:** inconclusive. Cerrada antes de la duración diseñada; con 0
  acciones no hay pass anticipado posible.
- **Decision:** ninguna sobre A2.

### T2
- **Result:** not run. Requiere T4 pasada y al menos 10 profesionales con
  consentimiento.

## Decision

Sin decisión sobre A2 ni sobre A3: T1, T3 y T4 quedaron inconclusive (las
tres cerradas antes de la duración diseñada) y T2 no se corrió. Las
creencias 7a, 7b y 8a siguen abiertas.

Patrón cualitativo, sin mover creencias: en dos versiones de la planilla
(vacía y precargada), 0 de 6 editores hicieron una acción, aunque todos
reaccionaron con entusiasmo. Es el mismo patrón de las entrevistas (a todos
les gusta la lista, 0 de 10 la sostuvieron). En T3, 3 de 12 casas dijeron
preferir la planilla, pero ninguna confirmó haber importado un contacto.

Lo que se vio, como dato cualitativo y sin mover creencias: nadie cargó
espontáneamente, y la mitad de los editores espera que la planilla llegue
cargada. Es el mismo patrón de las entrevistas (a todos les gusta la lista,
0 de 10 la sostuvieron).

Próximo paso (decisión del PM, 2026-11-17): rediseñar T1 con la planilla
precargada, la versión que pidieron 3 de 6 editores, con
`/design-solution-tests`.
