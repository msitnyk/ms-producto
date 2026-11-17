# T3 · Guion para Martín (concierge)

Prueba: `product/tests/2026-11-16-1111-encontrar-sin-preguntar.md`, T3 (creencia 8a).
Señal: casas con al menos 1 contacto "Sauces · …" en la agenda al día 7. Pasa con 6 de 12 o más; falla con menos de 4.

1. **Preparación (al cerrar T1).**
   - Completar `contactos.csv` sólo con las filas con consentimiento "sí" de la planilla de trabajo de T1. "Nombre en la agenda" = `Sauces · {Rubro} {Nombre} (rec. {Quién recomienda})`, por ejemplo `Sauces · Jardinero Teófilo (rec. Valentina)`.
   - Guardar cada uno en la agenda de Martín con ese nombre exacto: las tarjetas de contacto de WhatsApp se comparten desde la agenda, así que ese nombre es el que les llega.
2. **Elegir las 12 casas.** Ninguna editora de T1. Mitad casas que pidieron alguna vez en el grupo, mitad casas que sólo leen. Anotarlas en `hoja-de-captura.csv` antes de mandar nada.
3. **Día 0.** A cada casa: el mensaje A de `mensajes.md` y, a continuación, todos los contactos juntos (WhatsApp: adjuntar → Contacto → seleccionar varios). Anotar la fecha. Todas el mismo día.
4. **Durante la prueba.**
   - Sin recordatorios ni explicaciones de cómo importar.
   - Si alguien pregunta cómo se guardan: respuesta corta ("tocás cada uno y le das a Agregar") y anotarlo.
   - Anotar cualquier comentario espontáneo.
5. **Día 7.** Mandar el mensaje B y anotar cuántos contactos "Sauces" dice que le aparecen. Quien no responde en 2 días queda como "sin respuesta" y **no cuenta como que importó**.
6. **Cómo leer el resultado.** Contar las casas con 1 contacto "Sauces" o más.
   - 6 o más de 12 → `continue`.
   - 4 o 5 → `change`.
   - Menos de 4 → `discard`.
