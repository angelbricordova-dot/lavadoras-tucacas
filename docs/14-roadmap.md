# 14 · Roadmap y plan de validación

## Fases

| Fase | Duración | Objetivo | Entregables | Criterio de salida |
|------|----------|----------|-------------|--------------------|
| **0. Análisis y diseño** (esta) | ✔ | Documentar y alinear con el cliente | Documentos 00–16 | Aprobación del cliente |
| **1. Validación en campo** | 2–3 sem | Probar demanda y precio | Encuesta (30 anfitriones), censo de apartamentos, cotizaciones de equipos, visita a la junta | ≥ 10 anfitriones interesados con precio aceptado |
| **2. Piloto operativo** | 4–6 sem | Operar con 2 lavadoras sin software | WhatsApp Business + hoja de cálculo + QR | ≥ 20 ciclos, NPS ≥ 40, medir fallas y entregas |
| **3. MVP digital** | 6–8 sem | Bot de WhatsApp + panel mínimo | Reserva, estado, pagos, tareas | 70 % de reservas por bot |
| **4. Ampliación + IoT** | 8–12 sem | 6 lavadoras, sensores, PWA del operador | Flota ampliada, iCal | Utilización ≥ 40 % |
| **5. Catálogo web público** | 4–6 sem | Vitrina pública con disponibilidad | Web responsiva | Aumento de reservas nuevas |
| **6. Hub + lencería** | 3–6 meses | Servicio por kilo e intercambio | Local, equipos, stock | Ingreso ≥ 25 % por servicios |
| **7. Replicación** | continuo | Otros conjuntos/destinos | Receta operativa y licencia | 2.º destino operando |

## Piloto operativo (Fase 2): cómo se hace sin software

1. Compra de **2 lavadoras** (8 y 10 kg) y kit.
2. **WhatsApp Business** con catálogo (fotos, precio) y respuestas rápidas.
3. **Hoja de cálculo** con: máquinas, reservas, tareas, pagos, incidentes, ciclos.
4. QR por máquina que abre un chat de WhatsApp con el ID precargado.
5. Operador registra checklist y fotos en el celular.
6. Revisión semanal con el cliente (KPIs del doc 10).

## Guion de encuesta puerta a puerta (Fase 1)

**Presentación (15 s):** "Alquilamos lavadoras para que laves la lencería de tu apartamento entre huéspedes, la llevamos y la retiramos."

Preguntas (5 min):
1. ¿Alquilas tu apartamento? ¿Con qué frecuencia (noches/mes)?
2. ¿Quién limpia y quién lava la lencería? ¿Dónde?
3. ¿Cuánto pagas hoy por lavado por reserva/mes?
4. ¿Tienes lavadora o toma de agua y desagüe en el apartamento?
5. ¿Qué te molesta más (tiempo, calidad, costo, transporte)?
6. ¿Pagarías por un pase de 24 h de **$__**? (mostrar 3 precios en rotación: 6/9/12)
7. ¿Prefieres membresía mensual o pagar por uso?
8. ¿Cómo prefieres pagar (Pago Móvil, Zelle, efectivo)?
9. ¿Te interesaría intercambiar lencería (sucia por limpia)?
10. ¿Podemos agregarte a un WhatsApp para avisarte cuando empecemos? Te damos **un primer pase gratis**.

Registrar: apartamento, teléfono, respuestas, objeciones, quién decide.

## Métricas por fase

| Métrica | Fase 1 | Fase 2 | Fase 4 |
|---------|--------|--------|--------|
| Anfitriones entrevistados | 30 | — | — |
| Interesados con precio aceptado | ≥ 10 | — | — |
| Clientes registrados | — | ≥ 8 | ≥ 25 |
| Ciclos/mes | — | ≥ 20 | ≥ 150 |
| Utilización | — | medir | ≥ 40 % |
| NPS | — | ≥ 40 | ≥ 50 |
| Fallas/100 ciclos | — | línea base | −30 % |

## Decisiones "go / no-go"

- **Después de Fase 1:** si < 5 anfitriones aceptan el precio → ajustar propuesta (precio, plan, hub) antes de comprar equipos.
- **Después de Fase 2:** si la utilización es < 15 ciclos/máquina/mes → pivotar a hub/servicio por kilo o a segmentos B2B (posadas).
- **Después de Fase 4:** si el costo por falla supera el 5 % del ingreso → revisar modelo de flota (usadas vs. nuevas, otra marca).
