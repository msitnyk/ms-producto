# T2 · Guion para Martín (access-request)

Prueba: `product/tests/2026-11-16-1111-encontrar-sin-preguntar.md`, T2 (creencia 7a).
Señal: casas distintas que piden acceso a la planilla de vecinos en 7 días. Pasa con 20 o más; falla con menos de 15. Se registra además cuántos leyeron el mensaje.

1. **Requisito previo (antes del día 0).** T1 pasado, y en la planilla de trabajo al menos 10 profesionales con consentimiento "sí" de al menos 3 de los 5 rubros más pedidos (piletero, plomero, gasista, atmosférico, cerrajero). **Si no se cumple, la prueba no se corre.**
2. **Preparación.**
   - Crear la Google Sheet "Profesionales recomendados – Los Sauces" e importar `planilla-vecinos.csv`.
   - Copiar las filas con consentimiento "sí" de la planilla de trabajo.
   - Acceso **Restringido**; quienes reciban acceso entran como **lectores**.
   - Durante los 7 días no se agregan filas, así todos ven lo mismo.
3. **Gabriela.** Mandarle el mensaje A de `mensajes.md` y anotar en `resumen.csv` si lo fija.
4. **Día 0.** Mandar el mensaje B al grupo. Anotar fecha y hora.
5. **Durante los 7 días.**
   - Cada pedido de acceso llega por mail: anotarlo en `hoja-de-captura.csv` y aprobarlo como **lector** dentro de las 24 h.
   - Sin recordatorios, ni por privado ni en el grupo.
   - Si alguien pide la planilla por WhatsApp en vez de pedir acceso: pasarle el link del mensaje y anotarlo en comentarios. **No cuenta hasta que pida acceso.**
6. **Día 7.** En WhatsApp, abrir el mensaje del grupo (mantener presionado → Info) y anotar cuántos lo leyeron. Sacar una captura.
7. **Cómo leer el resultado.** Contar casas distintas con al menos un pedido (dos personas de la misma casa cuentan una vez; la casa de Martín no cuenta).
   - 20 o más → `continue`.
   - 15 a 19 → `change`.
   - Menos de 15 → `discard`.
   - Si falla, cruzar con los leídos: pocos leídos → "no lo vieron"; muchos leídos → "no les interesa".
