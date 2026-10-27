# Ofidi

mode: new · commercial

Ofidi (Oficios Diversos) es una web donde los vecinos de un barrio encuentran
profesionales de oficios (plomeros, cerrajeros, jardineros, atmosféricos…)
recomendados por otros vecinos. Cualquier vecino puede sugerir un profesional
(login con Google) y calificarlo; los datos de los profesionales sólo se ven
con login, para protegerlos, y para registrarse hace falta un código de
invitación del barrio que se comparte en el grupo de WhatsApp. El profesional gana presencia gracias a la
reputación que le dan los vecinos. Arranca como piloto gratuito en el barrio
Los Sauces (City Bell, La Plata), con el link fijado en el grupo de WhatsApp,
para reemplazar los pedidos de contactos que hoy se repiten en el chat. Se
empieza por web, no app, para probar primero si funciona; la monetización
queda para después (sponsors o fee a profesionales).

## Para quién

- **Vecinos de Los Sauces** (44 casas, ~44 usuarios): familias en casa con
  parque que necesitan mantenimiento recurrente y hoy piden y se pasan
  contactos en el grupo de WhatsApp del barrio. Son a la vez quienes consultan
  y quienes sugieren y califican.
- **Profesionales de oficios de la zona** que ya trabajan para el barrio por
  recomendación: 41 candidatos identificados en el chat
  (`materiales/candidatos-profesionales-interno.csv`), 3 confirmados para la
  demo. Son poco tecnológicos: en el piloto no necesitan hacer nada en la web.

Señal del problema (no prueba): ~87 pedidos de recomendación en el chat del
barrio entre 2019 y 2025, con rubros que se repiten y vecinos que vuelven a
preguntar lo mismo años después (`materiales/Chat de WhatsApp con Los Sauces 🍃/`).

## Creencias no verificadas

Ordenadas por impacto × incertidumbre — la primera es la próxima a atacar.

1. [product] [value] Ofidi se convierte en la respuesta del grupo: cuando
   alguien pide un profesional en el WhatsApp, otros vecinos contestan
   "fijate en Ofidi" en lugar de pasar el contacto. En los primeros 3 meses del
   piloto, al menos la mitad de los pedidos de recomendación en el grupo se
   responden con Ofidi, y al menos 22 de las 44 casas buscan un profesional en
   la web.
2. [product] [value] Los vecinos van a alimentar la base, no sólo consultarla:
   al menos 10 casas sugieren o califican un profesional (con login de Google)
   en los primeros 3 meses. Sin aportes, la base envejece como el chat.
3. [product] [viability] Comercios locales (corralones, viveros, ferreterías)
   pagarían por aparecer como sponsor ante los vecinos del barrio. (A definir.)
4. [product] [viability] Más adelante, los profesionales que consigan trabajos
   por Ofidi pagarían un fee por estar listados, aunque sean poco tecnológicos.
   (No se prueba en el piloto.)

**Próxima a atacar: la creencia 1.** Si el grupo sigue pasándose contactos
como siempre, el resto no importa.
