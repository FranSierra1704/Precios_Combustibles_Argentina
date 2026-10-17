# Hallazgos — Precios de combustibles en Argentina

Fuente: dataset público "Precios en surtidor" (Secretaría de Energía, datos.energia.gob.ar).
Descarga: 17/10/2026. Archivo de precios vigentes: 36.649 filas, 19 columnas.

## 1. Decisiones de limpieza

- **Horario:** se usó solo el precio diurno. Coincide con el nocturno en el 99,4% de los pares estación-producto. Las pocas diferencias incluyen extremos (−$2.259 / +$1.000) que parecen errores de carga.
- **Antigüedad del dato:** el problema principal del dataset no son los errores de tipeo, sino los precios desactualizados. Hay precios con fecha de 2016 (por ejemplo, nafta súper a $17,52).
- **Corte de fecha:** se consideran vigentes los precios con fecha desde el 01/09/2026. Quedan 3.236 filas (unas 864 estaciones).
- **Mínimo de estaciones por provincia:** 1. Todas las provincias entran en la comparación, pero cada mediana se muestra junto con la cantidad de estaciones que la sostiene.
- **Métrica:** mediana del precio por provincia y producto, menos sensible a valores extremos que el promedio.

## 2. Cobertura del dataset

- **Pico de junio de 2025:** 6.363 estaciones tienen su último precio cargado en junio de 2025 (contra 491 en mayo y 1.266 en julio). Coincide con la Resolución 717/2025, publicada el 2 de junio de 2025, que derogó la obligación de informar precios. La coincidencia es clara, aunque no prueba la causa.
- **Reporte activo actual:** septiembre y octubre de 2026 suman 3.236 precios, el núcleo de estaciones que hoy reporta.
- **Cobertura desigual:** Buenos Aires tiene 397 estaciones activas; Santa Cruz y San Luis, 1 cada una. Neuquén tiene solo 3. La cobertura depende de qué estaciones deciden reportar, no del tamaño del mercado.

## 3. Patrones de precios (desde 01/09/2026)

1. **NOA y NEA, caros en todo:** Jujuy, Misiones y Tucumán están entre las más caras en los cuatro combustibles líquidos.
2. **Patagonia, barata en naftas pero no en gasoil:** en nafta súper, las seis provincias patagónicas más La Pampa son las más baratas ($1.798–$2.019, contra $2.182–$2.364 en el resto). En gasoil premium, en cambio, Neuquén es la más cara del país ($2.895). Sin explicación confirmada.
3. **Relación entre productos invertida en la Patagonia:** en el centro, el gasoil común es más barato que la nafta premium (CABA: $2.369 vs. $2.489). En la Patagonia ocurre lo contrario (Neuquén: $2.499 vs. $2.267).
4. **GNC sin datos en 13 provincias**, sobre todo en el sur y el NEA. No se puede distinguir si no hay estaciones que lo vendan o si no reportan. Los extremos (Río Negro $1.390, CABA $694) pueden apoyarse en pocas estaciones.

## 4. Limitaciones

- Cada precio es lo que declara la estación, no un relevamiento independiente.
- Las provincias con 1 o 2 estaciones no permiten conclusiones a nivel provincial; los hallazgos se leen por región.
- El reporte es voluntario desde junio de 2025, así que la muestra no es aleatoria.
