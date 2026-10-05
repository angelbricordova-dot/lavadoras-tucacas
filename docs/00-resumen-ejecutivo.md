# 00 · Resumen ejecutivo

## La idea

Alquilar lavadoras a anfitriones de apartamentos turísticos en Tucacas, con **un catálogo de disponibilidad en tiempo casi real**, **reserva por franjas**, y **un operador local que entrega, conecta y retira la máquina**. La persona de limpieza lava la lencería en el propio apartamento (o en un punto de lavado) justo después del check-out.

## Por qué tiene sentido

1. **Problema real y recurrente:** cada cambio de huésped exige lavar sábanas, fundas y toallas. Pocos apartamentos tienen lavadora.
2. **Comprar no conviene [HIPÓTESIS del cliente]:** en costa, una lavadora que pasa semanas parada se corroe por el salitre; en movimiento (flota rotando) dura más. *Debe validarse con un técnico local.*
3. **Demanda concentrada y alcanzable:** decenas de apartamentos en el mismo conjunto y conjuntos vecinos; se vende puerta por puerta y por WhatsApp.
4. **Competencia indirecta, no directa:** existen servicios de lavandería para anfitriones (Dubái, Londres), alquiler de electrodomésticos por suscripción (Países Bajos, India, EE. UU.) y software de turnos de limpieza (Turno). **Nadie combina las tres cosas** —equipo en alquiler + disponibilidad en vivo + calendario del anfitrión— y menos en el contexto venezolano.

## La propuesta en una frase

> *"Tu lavadora lista cuando sale el huésped, sin comprarla, sin repararla y sin que se oxide."*

## Decisiones de diseño (resumen)

| Tema | Decisión propuesta |
|------|--------------------|
| Canal principal | **WhatsApp primero** (bot + catálogo), PWA liviana como complemento. WhatsApp es el estándar del comercio en Venezuela. |
| Quién usa vs. quién paga | El **anfitrión paga**, la **persona de limpieza usa**. Se modelan "delegados autorizados". |
| Planes | Ciclo suelto · Pase 24 h · Membresía mensual · Reserva de temporada/feriado · Lavadora fija en el apartamento. |
| Disponibilidad "se desocupa pronto" | Enchufe inteligente con medición de consumo + temporizador manual como respaldo (hay cortes de luz). |
| Cortes de luz/agua | Política explícita: **ciclo interrumpido por corte = no se cobra / se repone**. Revisión previa de agua y voltaje. |
| Pagos | USD como referencia; Pago Móvil (Bs), Zelle/efectivo USD; aviso claro del IGTF 3 % si se paga en divisa en efectivo. |
| Extras diferenciadores | Kit completo (jabón, ganchos, bolsas, protector de voltaje), **sincronización con calendario iCal** de Airbnb, **intercambio de lencería**, fase 2 de **punto de lavado (hub)**, venta a posadas/embarcaciones. |
| 24/7 | Cobertura realista: operador en horario extendido + guardia de emergencia; el bot atiende 24/7. |

## Números orientativos [HIPÓTESIS — ver doc 11]

- Flota piloto: **6 lavadoras**, inversión ≈ **USD 2.820**.
- Punto de equilibrio en caja: ≈ **93 ciclos/mes** en toda la flota (≈ 15 por máquina, medio ciclo al día).
- Escenario base: ≈ **USD 600/mes de margen de caja**, recuperación de inversión ≈ **5 meses**.
- Escenario conservador: casi sin ganancia (recuperación > 2 años) → por eso el piloto valida utilización antes de comprar la flota completa.

## Qué NO está en alcance ahora

- No se desarrolla la página web ni la app. Esta fase deja listos: análisis, requisitos, reglas, flujos, modelo de datos, wireframes de texto, plan operativo, finanzas y riesgos.

## Próximos pasos inmediatos

1. Responder las preguntas abiertas (doc 15) con el cliente.
2. Encuesta puerta a puerta a 30 anfitriones (guion en doc 14).
3. Piloto de 2 lavadoras con WhatsApp + hoja de cálculo antes de invertir en software.
