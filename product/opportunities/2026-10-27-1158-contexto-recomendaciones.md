---
status: framed
segment: Vecinos de Los Sauces (44 casas, City Bell) que piden o responden recomendaciones de profesionales en el grupo de WhatsApp del barrio
personas: laura-benitez, ricardo-ferraro, hector-ramirez, teofilo-modesto, gabriela-montero, marcela-sosa, jorge-pereyra
---

# Opportunity: Recomendaciones sin contexto que el grupo rehace cada vez

Cuando un vecino de Los Sauces necesita un profesional, el grupo vuelve a
recomendar desde cero lo que ya se recomendó antes, y el que pregunta recibe
contactos sueltos —a veces de varios vecinos— sin el contexto que necesita
para elegir; ahora, porque el piloto de Ofidi arranca y necesita saber qué
puede ofrecer que el grupo no da (el grupo ya responde en minutos).

## Segment and personas

- Laura Benítez (primary) — lo sufre: recibe varios contactos con un "este es bueno" y no sabe a cuál llamar
- Ricardo Ferraro (primary) — lo sufre, como parte del grupo: vuelve a contestar lo mismo, y su recomendación llega sin el contexto que él sí tiene
- Héctor Ramírez (secondary) — no lo sufre; lo afecta indirectamente: le llegan llamados sin contexto
- Teófilo "Modesto" (secondary) — no lo sufre
- Gabriela Montero (tertiary) — no lo sufre; puede respaldar o frenar lo que se haga en el grupo
- Marcela Sosa (negative) — sufre la falta de contexto, pero lo que pide (garantía, pagos) está fuera del alcance
- Jorge Pereyra (negative) — no lo sufre: no está en el grupo
- Missing: none

## Signals

| Signal | Provenance | Source |
|---|---|---|
| 87 pedidos de recomendación en 2019–2025; rubros que se repiten y vecinos que vuelven a preguntar lo mismo años después | real | `materiales/Chat de WhatsApp con Los Sauces 🍃/` (búsqueda heurística) |
| 45 de 87 pedidos reciben un contacto en el grupo en 48 h; mediana 3 minutos | real | ídem (heurístico) |
| En 20 de esos 45 llegan contactos de 2 o más vecinos distintos | real | ídem (heurístico) |
| 30 vecinos distintos responden; los 5 más activos suman el 30%: la carga está repartida, el costo es colectivo | real | ídem (heurístico) |
| 19 de 19 eligen profesionales por recomendaciones; 6 de 17 comentarios piden reputación, calificaciones o referencias | survey (n=19, 2021, muestra no acotada a Los Sauces) | `materiales/Encuesta sobre Oficios (Responses).xlsx` |
| Laura duda entre contactos sueltos; Ricardo responde de nuevo | synthetic | `product/personas/` |

## Business outcome

Adopción del piloto en Los Sauces: que el barrio use y alimente la base. Es la
condición para lo que viene después: una audiencia de vecinos que haga atractivo
el sponsoreo de comercios locales y un modelo replicable en otro barrio.

## Constraints

- Los datos de contacto de los profesionales no son públicos (Ley 25.326).
- Piloto acotado a las 44 casas de Los Sauces y gratuito.
- Los profesionales no usan la herramienta: su presencia depende de lo que carguen los vecinos.
- Sin restricciones de presupuesto ni de fecha declaradas.

## Beliefs

Registradas en `product/overview.md`.

- [opportunity: contexto-recomendaciones] [value] Elegir entre contactos sueltos les cuesta a los vecinos lo suficiente como para hacer algo al respecto hoy: en entrevistas, al menos 5 de 8 vecinos que pidieron un profesional en el último año cuentan un caso concreto en que hicieron trabajo extra para elegir (preguntaron por privado, pidieron opiniones, buscaron en Google) o eligieron mal por falta de contexto (precio, para qué trabajo sirve, cómo le fue a otro vecino).
- Viabilidad: referenciada a [product] [value] creencias 1 y 3 del overview (adopción del piloto: el grupo redirige a Ofidi; los vecinos alimentan la base). Como el grupo responde en 3 minutos, Ofidi sólo puede competir con contexto, no con velocidad.

## Research agenda

| Belief | Instrument | Decision it unlocks | By when |
|---|---|---|---|
| [opportunity: contexto-recomendaciones] [value] | 1) Ya hecho: análisis del chat (20 de 45 con varios contactos). 2) `/research-market`: cómo resuelven el contexto ClasApps, Timbrit y los grupos de barrio. 3) Entrevistas a 8 vecinos que pidieron en el último año, identificados en el chat | Si el problema se sostiene → `/explore-solutions` sobre esta oportunidad; si no → el valor de Ofidi no está en el contexto y hay que reencuadrar | Fin de noviembre de 2026, para poder llegar a la temporada alta |
| [product] [value] C1: el grupo redirige a Ofidi | Antes del piloto: entrevistas a 5–7 vecinos que suelen responder y a los admins del grupo (¿qué les impediría responder con un link?). Durante: conteo en el chat + analytics | Construir y lanzar el piloto, o cambiar la forma de entrar al grupo | Entrevistas junto con las de arriba; medición: 12 semanas de piloto |
| [product] [value] C3: los vecinos alimentan la base | Eventos de sugerencia y calificación durante el piloto | Si no alimentan, repensar quién carga la base | 12 semanas de piloto |

## Candidate ideas (not evaluated)

- Web con perfiles de profesionales y reseñas de vecinos (la idea original de Ofidi)
- Login con Google y código de invitación del barrio
- Vista sin login con nombre, rubro y reseñas; contacto sólo después del login
- 2–3 vecinos "champions" que respondan en el grupo con el link
