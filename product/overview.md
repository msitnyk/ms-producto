# Ofidi

mode: new · commercial

Ofidi (Oficios Diversos) es una web donde los vecinos de un barrio encuentran
profesionales de oficios (plomeros, cerrajeros, jardineros, atmosféricos…)
recomendados por otros vecinos. Cualquier vecino puede sugerir un profesional
(login con Google) y calificarlo; el profesional gana presencia gracias a la
reputación que le dan los vecinos. Arranca como piloto gratuito en el barrio
Los Sauces (barrio abierto de City Bell, La Plata), con el link fijado en el
grupo de WhatsApp, para reemplazar los pedidos de contactos que hoy se repiten
en el chat. Se empieza por web, no app, para probar primero si funciona; la
monetización queda para después (sponsors o fee a profesionales).

## Para quién

- **Vecinos de Los Sauces** (44 casas, ~44 usuarios): familias en casa con
  parque que necesitan mantenimiento recurrente y hoy piden y se pasan
  contactos en el grupo de WhatsApp del barrio. Son a la vez quienes consultan
  y quienes sugieren y califican.
- **Profesionales de oficios de la zona** que ya trabajan para el barrio por
  recomendación. En el piloto no necesitan hacer nada en la web.

## Lo que sabemos

Hechos con su fuente. Lo que no tiene fuente va a creencias o a hipótesis.

- El barrio tiene 44 casas y un consorcio con administrador externo y una
  comisión de vecinos — dicho por el PM, que vive en el barrio.
- ~87 pedidos de recomendación en el grupo de WhatsApp entre 2019 y 2025, con
  rubros que se repiten (atmosférico, plomero, cerrajero, jardinero) y vecinos
  que vuelven a preguntar lo mismo años después — búsqueda de texto sobre
  `materiales/Chat de WhatsApp con Los Sauces 🍃/`. Es señal de que el problema
  existe, no prueba de que cambien de hábito.
- 41 profesionales candidatos identificados a partir de los contactos
  compartidos en el chat, 3 confirmados para la demo —
  `materiales/candidatos-profesionales-interno.csv`.

## Restricciones y decisiones de diseño

- **Restricción:** los datos de contacto de los profesionales no son públicos
  (protección de datos personales, Ley 25.326). Esto no se negocia.
- **Decisión de diseño (hipótesis):** el acceso es con login de Google más un
  código de invitación del barrio compartido en el grupo. Agrega fricción que
  pega directo en la creencia 1; se mide el embudo clic en el link → registro →
  primera búsqueda. Alternativa si la fricción pesa: mostrar sin login nombre,
  rubro y reseñas, y revelar el contacto sólo después del login.
- **Hipótesis a validar indirectamente:** los profesionales son poco
  tecnológicos y no van a usar la web. Por eso el piloto no los incorpora como
  usuarios. Si fuera falsa, cambiaría el diseño (perfiles gestionados por ellos).

## Creencias no verificadas

Ordenadas por impacto × incertidumbre — la primera es la próxima a atacar.

1. [product] [value] Ofidi se convierte en la respuesta del grupo: cuando
   alguien pide un profesional en el WhatsApp, otros vecinos contestan
   "fijate en Ofidi" en lugar de pasar el contacto. En las primeras 12 semanas
   del piloto, al menos la mitad de los pedidos de recomendación en el grupo se
   responden con Ofidi, y al menos 22 de las 44 casas buscan un profesional en
   la web.
   - **Se refuta si:** a las 12 semanas, menos del 50% de los pedidos del grupo
     reciben una respuesta con Ofidi, o menos de 22 casas distintas hicieron al
     menos una búsqueda.
   - **Dato exacto:** pedidos de recomendación y respuestas que mencionan Ofidi
     o el link, contados sobre una exportación del chat con la misma búsqueda
     de texto usada para el histórico; casas únicas con al menos una búsqueda
     (analytics por usuario logueado).
   - **Dato complementario:** casas únicas con al menos un clic en "contactar"
     a un profesional. Muestra que la web resuelve (encontró y contactó), no
     que el grupo redirija; se lee junto al chat: muchos clics sin
     redirección en el grupo = la web sirve pero el hábito no cambió; grupo
     que redirige con pocos clics = falta oferta en la base.
   - **Por qué primero:** si es falsa, el resto no importa. Y es la más incierta:
     el chat muestra que los vecinos *piden*, pero no hay ninguna señal todavía
     de que vayan a *redirigir* a una web en vez de pasar el número.
   - **Ojo con la estacionalidad:** el piloto cae en verano, la temporada alta
     de jardinería y piletas. Más pedidos dan más volumen para medir, pero
     comparar contra el mismo período de años anteriores del chat, no contra
     el invierno.
2. [opportunity: contexto-recomendaciones] [value] Elegir entre contactos
   sueltos les cuesta a los vecinos lo suficiente como para hacer algo al
   respecto hoy: en entrevistas, al menos 5 de 8 vecinos que pidieron un
   profesional en el último año cuentan un caso concreto en que hicieron
   trabajo extra para elegir (preguntaron por privado, pidieron opiniones,
   buscaron en Google) o eligieron mal por falta de contexto (precio, para qué
   trabajo sirve, cómo le fue a otro vecino).
   - **Se refuta si:** menos de 5 de 8 tienen un caso así: llaman al primero
     que les pasan y les va bien.
   - **Dato exacto:** casos concretos relatados en entrevistas a vecinos
     identificados en el chat como quienes pidieron un profesional.
   - **Brief:** `product/opportunities/2026-10-27-1158-contexto-recomendaciones.md`.
3. [product] [value] Los vecinos van a alimentar la base, no sólo consultarla:
   al menos 10 casas sugieren o califican un profesional en las primeras 12
   semanas. Sin aportes, la base envejece como el chat.
   - **Se refuta si:** a las 12 semanas, menos de 10 casas distintas crearon una
     sugerencia o dejaron una calificación.
   - **Dato exacto:** eventos `sugerencia_creada` y `calificacion_creada` por
     usuario logueado, agrupados por casa.
4. [product] [viability] Al menos 3 comercios locales (corralones, viveros,
   ferreterías de City Bell) pagarían [monto a definir] por mes por aparecer
   como sponsor ante los vecinos del barrio.
   - **Se refuta si:** en 5–7 conversaciones con dueños o encargados, ninguno
     acepta ese rango o no tiene presupuesto para algo así.
   - **Quién la responde:** los dueños de los comercios, no los vecinos. No se
     ataca durante el piloto: depende de que el piloto funcione.
5. [product] [viability] Más adelante, al menos el 30% de los profesionales que
   consigan al menos un trabajo por mes a través de Ofidi pagarían
   [monto a definir] por mes o por contacto por estar listados, aunque sean poco
   tecnológicos.
   - **Se refuta si:** en conversaciones con los profesionales listados, menos
     del 30% acepta pagar, o rechazan el cobro de plano.
   - **Quién la responde:** los profesionales. No se prueba en el piloto.

**Próxima a atacar: la creencia 1.** Además de mirar el uso, hablar con 5–7
vecinos que suelen contestar pedidos en el grupo y con los admins del chat para
entender qué les impediría responder con el link.
