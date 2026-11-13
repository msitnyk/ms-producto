---
opportunity: encontrar-sin-preguntar
status: testing-several
chosen: whatsapp-a-pedido, contactos-a-la-agenda
tests:
---

# Solutions for: Lo que el grupo ya recomendó no se encuentra, y se vuelve a preguntar

## What the evidence says now

- **[opportunity: encontrar-sin-preguntar] [value]** (creencia 6): `weakened`.
  En 2025 hubo 8 pedidos en el grupo, contra los 2 por mes que pedía
  (conteo heurístico; es un piso).
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

### A2. Planilla compartida fijada en el grupo (`planilla-compartida`)
Una Google Sheet con rubro, nombre, zona, quién recomienda y teléfono,
visible para quien tenga el link. No es software nuevo, es lo más chico que
podría funcionar y es lo que pidieron los entrevistados. Reemplaza buscar en
el historial.

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
| A2 planilla-compartida | `mixed`: 10 de 10 dicen querer una lista (real, opinión, posible inducción). "Lo fijado no lo mira nadie" (synthetic) | `mixed`: técnicamente trivial, pero cualquiera con el link ve los teléfonos (choca con la Ley 25.326) | `weak`: no genera audiencia ni un modelo replicable | Se mantiene viva sin un responsable. 0 de 10 armaron o sostuvieron una lista (real) |
| A3 contactos-a-la-agenda | `mixed`: va sobre el hábito real (5 de 10 guardan en la agenda); nadie reaccionó a esta solución | `strong` en lo técnico: 202 tarjetas de contacto en `materiales/`. Necesita consentimiento | `weak`: después de mandar el paquete, Ofidi desaparece | Los vecinos importan el paquete y lo usan la próxima vez que contratan |
| A4 whatsapp-a-pedido | `mixed`: ataca la vergüenza de preguntar (V4, real), en su canal y sin login; nadie lo probó | `strong` en la versión manual (Martín a mano). La automatización, `to check with tech` | `mixed`: canal propio y medible; es la versión manual de A1 | Los vecinos le escriben a un número que no es el grupo |
| A5 etiquetas-en-el-grupo | `weak`: con 8 pedidos al año hay pocas recomendaciones nuevas para etiquetar, y lo viejo queda sin etiqueta | `strong`: no hay que construir nada; depende de los admins | `weak` | Los que recomiendan adoptan la norma, y aun así el volumen no alcanza |

Control: ninguna alternativa tiene deseabilidad `strong`, porque toda la
evidencia es sobre el problema y no sobre una solución. La favorita de
origen (A1) no sale mejor que el resto.

## Decision

**testing-several: A4 y A3**, elegidas por el PM el 2026-11-13. Coincide con
la recomendación.

- **A4 es la principal.** Es la prueba más barata del valor central de Ofidi
  (encontrar sin exponerse en el grupo), sin la fricción del login, y su
  registro de pedidos mide cuántas casas, qué rubros y cuándo. Si funciona,
  A1 es su versión a escala. Si nadie le escribe, A1 tampoco tiene a quién
  servir.
- **A3 es el contraste.** Si el competidor real es la agenda propia, A3
  prueba si alcanza con alimentarla. Si A3 le gana a A4, el rol de Ofidi
  pasa a ser el de quien arma y actualiza contactos de confianza, no el de un
  destino.
- **Decide Daniel Ocampo** (primary, derivado): el observador que hoy se
  arregla con su agenda.

Lo que cambiaría la decisión: si la demo de A1 está casi lista y se puede
entrar sin código (código dentro del link y sesión que no vence), A1 se
vuelve barata y conviene probarla junto a A4. Si los admins se oponen a un
número aparte del grupo, A4 pierde fuerza.

## To test

- **A4 — "Cuando un vecino necesita un profesional, le escribe a un número
  del barrio que no es el grupo"**: es la que la mata. Todo el hábito actual
  pasa por la agenda, el grupo o el privado, y un número nuevo es un canal
  más que hay que recordar para una necesidad que aparece pocas veces al
  año. Designed in /design-solution-tests.
- **A3 — "Las casas que reciben el paquete lo importan a la agenda y usan
  esos contactos la próxima vez que contratan"**: es la que la mata.
  Importar contactos es un paso que mucha gente no hace, y el uso puede
  ocurrir meses después del envío. Designed in /design-solution-tests.
- **Común a las dos:** consentimiento de los profesionales antes de compartir
  cualquier contacto (Ley 25.326) y contactos para los rubros de mayor
  demanda (piletero, plomero, gasista, atmosférico, cerrajero), que hoy la
  base no tiene.

## Value proposition: whatsapp-a-pedido (A4)

- **Pain relieved:** la vergüenza y la exposición de preguntar en el grupo
  (V4, real) y no encontrar lo ya recomendado en el historial (V1 y V9,
  real).
- **Gain created:** pedís en privado, a un solo número, y recibís los
  contactos que ya usaron tus vecinos, con quién los recomendó, sin que lo lea
  todo el barrio.
- **Replaces:** preguntar en el grupo o por privado a un vecino. Se cambiaría
  porque no expone al que pregunta, no suma ruido al grupo y no depende de
  que el vecino que sabe esté conectado.
- **Deliberately does not:** no intermedia ni garantiza trabajos (eso queda
  para Marcela, negative), no publica calificaciones, no pide login ni app y
  no reemplaza al grupo para lo urgente.

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
- [feature: whatsapp-a-pedido] [value] Los vecinos que necesitan un profesional le escriben a un número del barrio en vez de preguntar en el grupo: en 8 semanas de prueba, durante la temporada de noviembre a enero, al menos 8 de 44 casas distintas hacen al menos un pedido. *(propuesta; pendiente de registro)*
- [feature: contactos-a-la-agenda] [value] Las casas que reciben el paquete lo importan y lo usan: al menos la mitad de las casas que lo reciben lo importan, y al menos 1 de cada 3 de las que contratan en las 8 semanas siguientes usa un contacto del paquete. *(propuesta; pendiente de registro)*

Los umbrales finales los fija `/design-solution-tests`.

## Discarded or parked

- **A1 web-recomendaciones-firmadas — parked:** vuelve si A4 muestra demanda
  (si los vecinos le escriben al número, la web es su versión a escala) o si
  la demo permite entrar sin código.
- **A2 planilla-compartida — discarded:** expone los teléfonos a cualquiera
  con el link (Ley 25.326), y nadie sostuvo nunca una lista (0 de 10).
- **A5 etiquetas-en-el-grupo — discarded:** con 8 pedidos al año, la etiqueta
  apenas tendría contenido nuevo, y lo ya recomendado sigue sin encontrarse.
- **Carga inicial con los 3 o 4 que responden siempre — parked:** no es una
  alternativa, es la fuente de contenido de cualquiera de ellas. Entra como
  condición en los tests (V5 se ofreció).

## Outcome

*(Lo agrega /analyze-solution-tests.)*
