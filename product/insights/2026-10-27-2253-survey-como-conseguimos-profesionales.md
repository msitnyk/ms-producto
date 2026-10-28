---
source: survey
n: 15
date: 2026-10-27
survey: product/surveys/2026-10-27-1523-como-conseguimos-profesionales.md
data: product/surveys/informe_de_resultados.md (informe agregado; sin exportación cruda)
opportunity: contexto-recomendaciones
---

# Análisis de encuesta: Cómo conseguimos profesionales en Los Sauces

## Denominador y límites

- **n = 15 casas** de 44 (17 respuestas, 2 descartadas por filtro: 1 no
  residente, 1 casa duplicada). Meta de diseño: 15.
- **Reclutamiento:** mensaje personal del PM a ~10 casas de su red cercana +
  reenvío entre vecinos. Sobrerrepresenta a vecinos cercanos al PM y
  socialmente activos; sesgo de cortesía posible.
- **Datos:** sólo el informe agregado. No hay exportación cruda: **no se puede
  cortar por canal (link A vs. B) ni por antigüedad**, ni cruzar preguntas por
  persona. El origen real de los datos lo confirmó el PM; la primera versión
  del informe estaba titulada "Simulación de Encuesta".
- **Todo es direccional.** Con n = 15 se reportan conteos ("7 de 15"), no
  porcentajes con confianza, y nada se proyecta a las 44 casas.

## Objetivo 1 — Frecuencia y canal (creencia 1)

**Creíamos:** que en 12 semanas de piloto en verano habría pedidos suficientes
en el grupo para medir si se responden con Ofidi.

**Mostró la encuesta:**
- 13 de 15 casas contrataron a alguien de un oficio en los últimos 12 meses;
  10 de 15, dos veces o más.
- Rubros: jardinería 9 de 13, plomería o gas 7, electricidad o aire 5,
  piletas 4.
- La última vez, el contacto vino del **grupo de WhatsApp en 6 de 13** casos;
  4 ya lo tenían, 2 preguntaron por privado, 1 afuera del barrio, **0 por
  Google o apps**.

**Cruzado con el chat** (`materiales/Chat de WhatsApp con Los Sauces 🍃/`,
búsqueda heurística, provenance `real`): el grupo recibe **~10 a 14 pedidos de
recomendación por año**, y entre diciembre y febrero hubo **entre 1 y 4 por
verano** (18 de 76 en todo el histórico, ~24%: proporcional a 3 meses, **sin
pico de verano visible en el grupo**).

**Decisión:** la contratación es alta, pero la mayor parte **no pasa por el
grupo visible**. La métrica principal de la creencia 1 ("al menos la mitad de
los pedidos del grupo se responden con Ofidi") se mediría sobre **2 a 4
pedidos** en 12 semanas: es demasiado poco para refutarla o confirmarla. La
señal de casas que buscan en la web y el clic en "contactar" pasan a ser las
medidas que pueden leerse. Se propone revisar la métrica de la creencia 1 (vía
`/review-evidence`). El supuesto "el verano da más volumen en el grupo" no se
ve en el chat; en la encuesta, jardinería y piletas sí son los rubros más
contratados.

## Objetivo 2 — El costo de elegir (creencia 2)

**Creíamos:** que el costo es elegir entre varios contactos sueltos sin contexto.

**Mostró la encuesta:**
- La última vez, **8 de 13 tuvieron una sola opción**; 3 tuvieron dos y 1,
  tres o más.
- Aun así, **10 de 13 hicieron trabajo extra antes de llamar**: 7 le
  preguntaron más detalles a quien les pasó el contacto, 4 pidieron opiniones
  a otros vecinos, 3 pidieron más de un presupuesto, 1 buscó en Google. Sólo 3
  llamaron directo.
- **7 de 15** tuvieron en el año un trabajador que no vino, dejó el trabajo a
  medias o cobró mucho más de lo esperado. La pregunta no indaga la causa:
  **no se puede atribuir a falta de contexto**.

Temas de la Q9 ("lo más difícil", respuestas representativas del informe; sin
el total de respuestas no se puede contar menciones por tema):
- **Confianza** para dejarlo entrar: *"Saber si el tipo es de confianza para
  dejarlo entrar y si no me va a arrancar la cabeza con el precio."*
- **Precio** sin comparar a mano: *"Comparar precios sin tener que mandar 5
  mensajes distintos. Te pasan un número pero no sabés si trabaja bien."*
- **Que responda y cumpla**: *"Conseguir a alguien que responda rápido para
  limpiar la pileta antes del fin de semana y que venga cuando dice que va a
  venir."*

Qué contexto da hoy quien recomienda (Q10): qué trabajo le hizo, si es prolijo,
si cobra caro o normal, si es puntual o viene en el día, y **para qué rubro
sirve y para cuál no** (*"este es re bueno para cerrajería pero medio colgado
con la pintura"*).

**Decisión:** la creencia 2 se sostiene direccionalmente, pero **cambia de
forma**. El costo dominante no es *elegir entre varios*, sino **saber si el
único que te pasaron sirve** (confianza, precio, puntualidad, rubro), y hoy se
resuelve preguntándole por privado a quien lo recomendó. El contexto que haría
falta ya existe en la cabeza de quien recomienda y se pierde en el camino. Se
propone reformular la creencia 2 en el overview (vía `/review-evidence`); el
umbral sigue siendo de entrevistas (5 de 8).

## Objetivo 3 — Quién aporta hoy (creencia 3)

**Creíamos:** que al menos 10 de las 44 casas sugerirán o calificarán un
profesional en las primeras 12 semanas.

**Mostró la encuesta:**
- **9 de 15** casas le pasaron a un vecino el contacto de un profesional en el
  último año; 5 de ellas, dos veces o más.
- Por dónde: grupo de WhatsApp 6 de 9, mensaje privado 5 de 9, en persona 2.

**Decisión:** hay **al menos 9 casas distintas** que ya comparten contactos:
es un piso, no una proyección, y está cerca de la meta de 10. Pero pasar un
número por WhatsApp no es lo mismo que entrar a una web, registrarse con
Google y un código, y dejar una calificación. La pregunta abierta de la
creencia 3 es **la fricción del traspaso**, no la disposición a recomendar.
Sin datos crudos no se sabe si esas 9 son las mismas casas cercanas al PM.

## Lo que el informe concluye y este análisis no sostiene

- **"Proyectado al total del barrio, la meta de 10 casas aportantes es
  alcanzable":** no se puede proyectar desde una muestra de la red cercana del
  PM. Lo que sí vale es el piso de 9 casas.
- **"46,7% tuvo una mala experiencia por falta de contexto":** la Q6 no pregunta
  la causa.
- **"El piloto contará con suficiente volumen orgánico":** hay volumen de
  contratación, pero no de pedidos en el grupo, que es lo que mide la
  creencia 1.
- **"Avanzar con el piloto":** una encuesta no decide eso; antes vienen las
  entrevistas y `/explore-solutions`.

## Porqués para las entrevistas

- ¿Por qué, aun con una sola opción, le preguntan más a quien se lo pasó? ¿Qué
  preguntan exactamente?
- En las 7 malas experiencias, ¿qué pasó, y qué información habría cambiado la
  decisión (si alguna)?
- ¿Por qué la mitad no pasa por el grupo? ¿Qué se resuelve por privado que no
  se pide en público?
- Para quienes ya recomiendan: ¿qué los haría escribirlo una vez en un lugar en
  vez de repetirlo? ¿Qué los frenaría?

## Pool de reclutamiento

8 de 15 aceptaron una charla. El informe identifica 3 perfiles:

| Candidato | Perfil | Frente a las creencias | Prioridad |
|---|---|---|---|
| A | Vecino nuevo (<2 años), contrató 3 veces, mala experiencia, consultó por privado antes | Confirma la creencia 2 | Media |
| B | Vecino antiguo (>5 años), contrata 4–6 veces por año, nunca compartió un contacto | **Contradice la creencia 3** | **Alta** |
| C | Pasó contactos más de 5 veces en el año | Confirma la creencia 3; clave para entender el traspaso | Media |

Faltan los otros 5 que aceptaron. Priorizar entre ellos a quien **contradiga**
la creencia 2: los que **llamaron directo** sin trabajo extra (3 de 13 en la
Q5), si alguno aceptó. Sin la exportación cruda, el PM tiene que identificarlos
en su herramienta de encuestas.
