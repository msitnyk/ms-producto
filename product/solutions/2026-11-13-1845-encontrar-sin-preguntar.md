---
opportunity: encontrar-sin-preguntar
status: testing-several
chosen: planilla-compartida, contactos-a-la-agenda
tests:
---

# Solutions for: Lo que el grupo ya recomendó no se encuentra, y se vuelve a preguntar

## What the evidence says now

- **[opportunity: encontrar-sin-preguntar] [value]** (creencia 6): `weakened`.
  En 2025 hubo 13 pedidos en el grupo (~1,1 por mes), contra los 2 por mes
  que pedía (conteo heurístico revisado a mano; es un piso).
  (`product/insights/2026-11-13-1817-sintesis-entrevistas-noviembre.md`, real)
- Contratar es frecuente (13 de 15 casas en el año, survey), pero casi todo
  se resuelve **fuera del grupo**: agenda propia o historial (5 de 10, real).
- Se confía en quien recomienda (7 de 10 llaman sin trabajo extra) y lo
  negativo no se escribe (5 de 10 descartan en silencio). Real.
- **[product] [value] C1** (el grupo redirige a Ofidi): `weakened`.
  **C3** (los vecinos alimentan la base): abierta. V5 se ofrece a cargar, pero
  nadie armó nunca una lista.
- Restricciones: contactos no públicos (Ley 25.326), 38 de 41 profesionales
  sin consentimiento, piloto gratuito y acotado a 44 casas, profesionales que
  no usan la herramienta.

## Baseline: what people do today

Guardan el contacto en la agenda del teléfono cuando pasa por el chat, o lo
buscan en el historial (V1, V2, V6, V8 y V9; real). Si no lo encuentran,
preguntan en el grupo o por privado y les contestan en minutos (mediana de 3
minutos en el chat; real). En la encuesta, la última vez 4 de 13 ya lo
tenían, 6 de 13 lo consiguieron en el grupo, 2 de 13 por privado y 0 por
Google (survey, n=15). Es rápido, gratis y se apoya en la confianza en quien
recomienda. **Falla** cuando el contacto no aparece, cuando da vergüenza
preguntar (V4) y cuando lo que se sabe del profesional (precio, puntualidad)
circula sólo por privado (V3 y V7).

## Alternatives

### A1. Web Ofidi con recomendaciones firmadas (`web-recomendaciones-firmadas`)
La idea original, ajustada a la evidencia. Perfiles por rubro y zona, con
"recomendado por [vecino]" y su comentario, sin estrellas. Links directos a
cada perfil para compartir, y el contacto visible sólo después del login.
Ataca encontrar sin preguntar, con el contexto de quién recomienda. Para
Laura y Daniel (primary), que buscan, y Ricardo (primary), que carga.
Reemplaza la agenda propia y preguntar en el grupo. Absorbe las ideas sin
evaluar de "recomendado por…", la señal privada en lugar de estrellas y la
vista sin login.

### A2. Planilla compartida (`planilla-compartida`)
Una Google Sheet que unifica la información: rubro, nombre, zona, quién
recomienda, su comentario y teléfono. **Versión elegida (2026-11-13):** se
comparte con las cuentas de Google de cada vecino, no por link abierto; sólo
incluye profesionales que dieron su consentimiento; la editan 2 o 3 personas
con nombre (Martín y los que responden siempre, como V5), y el resto la ve y
sugiere por un formulario o escribiéndole a un editor. No es software nuevo:
es lo más chico que podría funcionar y lo que pidieron los entrevistados. Es
A1 sin desarrollo. Para Daniel y Laura (primary), que buscan, y Ricardo
(primary), que carga. Reemplaza buscar en el historial y preguntar en el
grupo.

### A3. Paquete de contactos para la agenda (`contactos-a-la-agenda`)
No reemplaza la agenda: la alimenta. Un set de tarjetas de contacto ya
verificadas, con rubro y quién lo recomienda en el nombre ("Sauces · Plomero
Rubén (rec. Ricardo)"), que cada casa importa. Se actualiza por temporada.
Ataca el insight 1 de la síntesis (el competidor real es la agenda) y entra
por el hábito que ya existe. Para Daniel (primary) y Laura (primary).

### A4. Número de WhatsApp a pedido (`whatsapp-a-pedido`)
Un número aparte del grupo. Le escribís "plomero" y te devuelve los contactos
recomendados por vecinos, con quién los recomendó. Al principio lo atiende
una persona (Martín, a mano). Ataca preguntar sin exponerse en el grupo (V4),
dentro del canal que todos usan y sin login. Para Laura y Daniel (primary).
Reemplaza preguntar en el grupo o por privado.

### A5. Convención de etiquetas en el grupo (`etiquetas-en-el-grupo`)
Una regla del grupo acordada con los admins (Gabriela, tertiary): toda
recomendación lleva una etiqueta, como "#plomero", y la frase de quien
recomienda, para que la lupa de WhatsApp la encuentre. No es software.
Ataca que el historial no se puede buscar (V1, V9).

## Comparison

| Alternative | Desirable | Feasible | Viable | Riskiest belief |
|---|---|---|---|---|
| Baseline: agenda, historial y preguntar | Funciona: respuesta en minutos y confianza en quien recomienda (real) | — | — | — |
| A1 web-recomendaciones-firmadas | `mixed`: pain evidenced, relief not tested. La prueba de usabilidad de 2021 (n=5) muestra que se encuentra y contacta fácil, pero eso es usabilidad, no deseo (real, `materiales/Reporte Ux_Sitnyk.pptx`). Ricardo duda (synthetic) | `mixed`: hay una demo con 3 profesionales (overview). El resto, `to check with tech`. Consentimiento pendiente de 38 de 41 | `mixed` (assumption): es el producto, es medible y es donde iría un sponsor | Un vecino que necesita un profesional abre la web antes que su agenda o el grupo; con uso tan poco frecuente, login más código puede matarla |
| A2 planilla-compartida | `mixed`: 10 de 10 dicen querer una lista (real, opinión, posible inducción). "Lo fijado no lo mira nadie" (synthetic) | `strong` en lo técnico. Con link abierto choca con la Ley 25.326; en la versión elegida (acceso restringido, sólo profesionales con consentimiento) queda dentro de la restricción | `weak` como está (no genera audiencia ni un modelo replicable); `mixed` como prueba de A1: si la usan, confirma el valor de la web | Los vecinos la abren cuando necesitan un profesional, en vez de ir a la agenda o al grupo, y se mantiene viva con editores además de Martín. 0 de 10 sostuvieron una lista (real) |
| A3 contactos-a-la-agenda | `mixed`: va sobre el hábito real (5 de 10 guardan en la agenda); nadie reaccionó a esta solución | `strong` en lo técnico: 202 tarjetas de contacto en `materiales/`. Necesita consentimiento | `weak`: después de mandar el paquete, Ofidi desaparece | Los vecinos importan el paquete y lo usan la próxima vez que contratan |
| A4 whatsapp-a-pedido | `mixed`: ataca la vergüenza de preguntar (V4, real), en su canal y sin login; nadie lo probó | `strong` en la versión manual (Martín a mano). La automatización, `to check with tech` | `mixed`: canal propio y medible; es la versión manual de A1 | Los vecinos le escriben a un número que no es el grupo |
| A5 etiquetas-en-el-grupo | `weak`: con ~13 pedidos al año hay pocas recomendaciones nuevas para etiquetar, y lo viejo queda sin etiqueta | `strong`: no hay que construir nada; depende de los admins | `weak` | Los que recomiendan adoptan la norma, y aun así el volumen no alcanza |

Control: ninguna alternativa tiene deseabilidad `strong`, porque toda la
evidencia es sobre el problema y no sobre una solución. La favorita de
origen (A1) no sale mejor que el resto.

## Decision

**testing-several: A2 y A3**, elegidas por el PM el 2026-11-13.

- **A2 es la principal.** Prueba lo que importa, la unificación de la
  información en un solo lugar, sin desarrollo y sin depender de una persona
  para responder. Si la usan, A1 es su versión a escala.
- **A3 es el contraste.** Si el competidor real es la agenda propia, A3
  prueba si alcanza con alimentarla. Las dos juntas responden la pregunta de
  fondo: ¿el vecino prefiere ir a buscar a un lugar común o tener los
  contactos en su teléfono?
- **Decide Daniel Ocampo** (primary, derivado): el observador que hoy se
  arregla con su agenda.

**Difiere de la recomendación de la IA**, que era A4 (número de WhatsApp) más
A3 y descartaba A2. El PM eligió A2 porque A4 depende de una sola persona, y
porque una planilla compartida prueba la unificación de la información. Las
objeciones a A2 (exposición de teléfonos y mantenimiento) se resuelven en el
diseño: acceso restringido, consentimiento y editores con nombre. Registrado
en `product/corrections.md` (2026-11-13).

Lo que cambiaría la decisión: si en las primeras semanas casi nadie abre la
planilla, A4 (un canal donde se pregunta en vez de buscar) vuelve a ser
candidata, con un número compartido entre varios editores.

## To test

- **A2 — "Cuando un vecino necesita un profesional, abre la planilla en vez
  de ir a su agenda o al grupo, y la planilla se mantiene viva con editores
  además de Martín"**: es la que la mata. Es un lugar nuevo que hay que
  recordar para una necesidad que aparece pocas veces al año ("lo fijado no
  lo mira nadie", synthetic), y nunca nadie sostuvo una lista (0 de 10, real).
  Designed in /design-solution-tests.
- **A3 — "Las casas que reciben el paquete lo importan a la agenda y usan
  esos contactos la próxima vez que contratan"**: es la que la mata.
  Importar contactos es un paso que mucha gente no hace, y el uso puede
  ocurrir meses después del envío. Designed in /design-solution-tests.
- **Común a las dos:** consentimiento de los profesionales antes de compartir
  cualquier contacto (Ley 25.326) y contactos para los rubros de mayor
  demanda (piletero, plomero, gasista, atmosférico, cerrajero), que hoy la
  base no tiene.

## Value proposition: planilla-compartida (A2)

- **Pain relieved:** no encontrar lo ya recomendado en el historial (V1 y
  V9, real) y tener que volver a preguntar en el grupo, con la vergüenza que
  eso trae (V4, real).
- **Gain created:** todo lo que el barrio ya recomendó, en un solo lugar, por
  rubro y zona, con quién lo recomendó y qué dijo, sin preguntarle a nadie.
- **Replaces:** buscar a ciegas en el historial y preguntar en el grupo. Se
  cambiaría porque está todo junto y ordenado, y no expone al que busca.
- **Deliberately does not:** no intermedia ni garantiza trabajos (eso queda
  para Marcela, negative), no tiene calificaciones ni estrellas, no es
  pública (sólo vecinos con acceso) y no incluye profesionales sin su
  consentimiento.

## Value proposition: contactos-a-la-agenda (A3)

- **Pain relieved:** buscar en el historial un contacto que alguien pasó y no
  encontrarlo (V1, V9; Daniel).
- **Gain created:** los profesionales de confianza del barrio, ya en tu
  agenda, con rubro y quién los recomendó, para cuando los necesites.
- **Replaces:** guardar uno por uno los contactos que pasan por el chat. Se
  cambiaría porque llega completo y ordenado, sin tener que estar atento al
  grupo.
- **Deliberately does not:** no es una web ni un canal nuevo, no tiene
  calificaciones ni búsqueda (la búsqueda es la de la agenda) y no se
  actualiza solo (se manda una nueva versión por temporada).

## Beliefs

- [opportunity: encontrar-sin-preguntar] [value] Volver a preguntar en el grupo les cuesta a los vecinos lo suficiente como para buscar en otro lado cuando lo tienen a mano (registrada en `product/overview.md`, creencia 6, `weakened`).
- [feature: planilla-compartida] [value] Unificar la información en una planilla compartida sirve: en 8 semanas de prueba, durante la temporada de noviembre a enero, al menos 15 de las 44 casas la abren, y al menos 3 personas además de Martín agregan o corrigen un profesional. *(registrada en `product/overview.md`, creencia 7)*
- [feature: contactos-a-la-agenda] [value] Las casas que reciben el paquete lo importan y lo usan: al menos la mitad de las casas que lo reciben lo importan, y al menos 1 de cada 3 de las que contratan en las 8 semanas siguientes usa un contacto del paquete. *(registrada en `product/overview.md`, creencia 8)*

Los umbrales finales los fija `/design-solution-tests`.

## Discarded or parked

<<<<<<< HEAD
- **A1 web-recomendaciones-firmadas — parked:** vuelve si la planilla muestra
  uso (la web es su versión a escala) o si la demo permite entrar sin código.
- **A4 whatsapp-a-pedido — parked:** depende de una sola persona para
  responder (decisión del PM, 2026-11-13). Vuelve si casi nadie abre la
  planilla, con un número compartido entre varios editores.
- **A5 etiquetas-en-el-grupo — discarded:** con 8 pedidos al año, la etiqueta
=======
- **A1 web-recomendaciones-firmadas — parked:** vuelve si A4 muestra demanda
  (si los vecinos le escriben al número, la web es su versión a escala) o si
  la demo permite entrar sin código.
- **A2 planilla-compartida — discarded:** expone los teléfonos a cualquiera
  con el link (Ley 25.326), y nadie sostuvo nunca una lista (0 de 10).
- **A5 etiquetas-en-el-grupo — discarded:** con ~13 pedidos al año, la etiqueta
>>>>>>> 2f810d97e6c52835bd109aaad2a1bcdde3d443d8
  apenas tendría contenido nuevo, y lo ya recomendado sigue sin encontrarse.
- **Carga inicial con los 3 o 4 que responden siempre — parked:** no es una
  alternativa, es la fuente de contenido de cualquiera de ellas. Entra como
  condición en los tests (V5 se ofreció).

## Outcome

*(Lo agrega /analyze-solution-tests.)*
