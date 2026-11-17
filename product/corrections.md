# Correcciones

## 2026-10-27 — personas (`/generate-personas`)

- **Qué propuso la IA:** Damián Quiroga (`negative`), dueño de una empresa de reformas de La Plata que vende por redes y quiere aparecer en Ofidi para conseguir clientes, como límite de alcance.
- **Qué decidió el humano:** sacarlo y reemplazarlo por Teófilo "Modesto" (`secondary`), el jardinero de referencia del barrio.
- **Por qué:** el PM prefiere que el set represente a los profesionales que el barrio ya recomienda; el profesional de afuera que se autopromociona no aporta a la discusión del piloto. Queda el set sin persona `negative`.

## 2026-11-13

- **Artifact:** `product/solutions/2026-11-13-1845-encontrar-sin-preguntar.md` (`/explore-solutions`)
- **AI proposed:** probar en paralelo A4 (número de WhatsApp a pedido, atendido a mano) como principal y A3 (paquete de contactos para la agenda) como contraste. Descartaba A2 (planilla compartida) porque cualquiera con el link vería los teléfonos (Ley 25.326) y porque nadie sostuvo nunca una lista (0 de 10).
- **Human decided:** A2 como primera opción, con A3 como contraste; A4 queda `parked`.
- **Why:** A4 depende de una sola persona para responder. Una Google Sheet compartida prueba lo que importa, la unificación de la información, sin depender de nadie. Las dos objeciones de la IA se resuelven con el diseño: acceso restringido a las cuentas de los vecinos (no por link abierto), sólo profesionales con consentimiento, y editores con nombre.

## 2026-11-16

- **Artifact:** `product/tests/2026-11-16-1111-encontrar-sin-preguntar.md`, T1 (`/design-solution-tests`)
- **AI proposed:** 14 días por editor para cargar la planilla, con un recordatorio el día 7.
- **Human decided:** 2 días por editor (48 h desde el acceso), con un recordatorio a las 24 h. Umbral y regla de decisión sin cambios. Decidido antes de correr la prueba.
- **Why:** que la prueba no se haga larga. Límite aceptado: si falla, puede ser por falta de tiempo y no de ganas.

- **Artifact:** `product/tests/2026-11-16-1111-encontrar-sin-preguntar.md`, T1 (en curso)
- **AI proposed:** 4 o 5 editores (diseño); con T1 en curso, sumar a Roberto con sus propias 48 h para no dejar afuera al que más contactos pasa en el grupo.
- **Human decided:** sumar a Roberto como 6.º editor. Umbral sin cambios (3 editores con 2 profesionales o más). Decidido antes de tener resultados.
- **Why:** si la prueba fallaba sin él, quedaba la duda de si se eligió mal a los editores.

## 2026-11-17

- **Artifact:** `product/tests/2026-11-16-1111-encontrar-sin-preguntar.md`, T1 (`/analyze-solution-tests`)
- **AI proposed:** esperar a que se cumplan las 48 h de cada editor para que T1 dé `passed` o `failed`.
- **Human decided:** cerrar T1 el 2026-11-17, antes de tiempo, como `inconclusive`, y rediseñarla con la planilla precargada.
- **Why:** sin novedades de los editores; tras el recordatorio, uno se olvidó y otro no tiene tiempo. 3 de 6 pidieron que la planilla venga cargada.

- **Artifact:** `product/tests/2026-11-16-1111-encontrar-sin-preguntar.md`, T4 (antes de correr)
- **AI proposed:** columna de consentimiento en la planilla de los editores; cada editor pide el consentimiento a los profesionales que firma, y pasar una fila a `sí` cuenta como acción.
- **Human decided:** sacar la columna de consentimiento de la planilla de los editores. El consentimiento lo gestiona Martín internamente (`materiales/candidatos-profesionales-interno.csv`, columna `PublicationConsent`). Pasar a `sí` deja de ser una acción; el umbral no cambia.
- **Why:** el consentimiento es un dato interno, no algo que tengan que manejar los editores.

- **Artifact:** `product/tests/2026-11-16-1111-encontrar-sin-preguntar.md`, T3 (antes de correr)
- **AI proposed:** correr T3 después de la prueba de los editores, con el contenido con consentimiento que saliera de ahí; advirtió que con un paquete de 3 contactos un mal resultado puede deberse a lo pobre del paquete y no a que no quieran importar.
- **Human decided:** arrancar T3 ya, en paralelo con T4, con los 3 profesionales con consentimiento (Teófilo, Leo Gisbert, Fernando). Umbral y regla de decisión sin cambios.
- **Why:** no esperar a T4 para avanzar con la prueba de A3.

- **Artifact:** `product/tests/2026-11-16-1111-encontrar-sin-preguntar.md`, T3 (`/analyze-solution-tests`)
- **AI proposed:** consultar el día 7 (2026-11-24); como alternativa, adelantar la consulta al 2026-11-20; fijar antes del resultado una doble lectura (12 casas y 9 no editoras) por el desvío de 3 casas editoras de T4.
- **Human decided:** consultar el mismo día del envío (2026-11-17) y cerrar T3 como `inconclusive` sin repreguntar a las 4 casas cuya respuesta no se pudo medir. La doble lectura quedó sin efecto.
- **Why:** no cansar a los vecinos con más mensajes y terminar las pruebas hoy. Límite: la señal no se capturó (el marcador "Sauces" choca con cómo los vecinos se agendan entre sí) y la consulta fue el día 0.

- **Artifact:** `product/tests/2026-11-16-1111-encontrar-sin-preguntar.md`, T4 (`/analyze-solution-tests`)
- **AI proposed:** cerrar T4 recién al cumplirse las 48 h del último editor (2026-11-19), leyendo el historial de versiones sin mandar mensajes.
- **Human decided:** cerrar T4 el 2026-11-17, el día del aviso, como `inconclusive`, con 0 acciones en el historial.
- **Why:** terminar las pruebas hoy y no cansar a los vecinos.

- **Artifact:** `product/tests/2026-11-16-1111-encontrar-sin-preguntar.md`, T4 (`/analyze-solution-tests`)
- **AI proposed:** con 0 acciones a horas del aviso, `inconclusive` (el diseño pedía 48 h por editor); para un `failed` válido, mirar el historial el 2026-11-19 sin mandar mensajes.
- **Human decided:** marcar T4 como `failed` el 2026-11-17 y descartar A2.
- **Why:** no esperar hasta el jueves. Límite: un `failed` anticipado no está respaldado por el diseño (la señal todavía podía crecer).

- **Artifact:** `product/solutions/2026-11-13-1845-encontrar-sin-preguntar.md`, A4 (`/analyze-solution-tests`)
- **AI proposed:** según la regla de T4, al descartarse A2 vuelve A4 (número de WhatsApp a pedido).
- **Human decided:** no reactivar A4; queda parked.
- **Why:** el PM no quiere quedar como el cargador de los profesionales.
