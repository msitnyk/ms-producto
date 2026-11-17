# T4 · Guion para Martín (concierge)

Prueba: `product/tests/2026-11-16-1111-encontrar-sin-preguntar.md`, T4 (creencia 7b, versión precargada).
Señal: editores, sin contar a Martín, con 2 acciones o más en 48 h. Acción = firmar una fila ("Quién recomienda"), corregir un dato o agregar un profesional.
El consentimiento lo gestiona Martín internamente en `materiales/candidatos-profesionales-interno.csv` (columna `PublicationConsent`); no está en la planilla de los editores.

1. **Precarga.** En la misma planilla de trabajo de T1 (los editores ya tienen acceso), importar `precarga.csv` (Archivo → Importar → Reemplazar hoja actual). Son los 41 candidatos, con "Zona", "Quién recomienda" y "Comentario" vacíos. Anotar la hora: lo de Martín hasta ese momento no cuenta.
2. **Acceso.** Confirmar que los 6 editores (Roberto incluido) tienen acceso de editor.
3. **Hora 0.** Mandar el mensaje A de `mensajes.md` a cada editor. Anotar la hora en `hoja-de-captura.csv`: **las 48 h de cada editor corren desde ahí.**
4. **Durante la prueba.**
   - Martín no toca la planilla después de la precarga.
   - Si alguien pide ayuda, Martín puede sentarse con él mientras **él** edita. Se anota "con Martín".
   - Si alguien manda datos para que los cargue Martín: mensaje D y anotar "pidió que cargue Martín".
5. **A las 24 h de cada editor.** Revisar Archivo → Historial de versiones. A quien no hizo nada, mandarle el mensaje C. Es el único recordatorio.
6. **A las 48 h de cada editor.** Revisar el historial, contar sus acciones por tipo, sacar una captura y cerrar su fila. **No cerrar antes de que se cumplan las 48 h del último editor.**
7. **Cómo leer el resultado.** Contar los editores con 2 acciones o más.
   - 3 o más → `continue`.
   - 2, o la mayoría actuó sólo con Martín al lado → `change`.
   - 1 o ninguno → `discard`.

Anotar aparte los profesionales que agreguen de los rubros que faltan (plomero, gasista, piletero): la precarga tiene 1 de plomería/piletas y ningún gasista.
