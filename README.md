# LavaTuca (nombre provisional) — Alquiler de lavadoras para apartamentos turísticos en Tucacas

> **Fase actual: Análisis y Diseño.** Este repositorio contiene **solo documentación**. No se construye la página web en esta fase.

## ¿Qué es?

Un servicio (con catálogo digital de disponibilidad) que alquila lavadoras —por ciclo, por día o por membresía— a propietarios y anfitriones de apartamentos turísticos (Airbnb, Stay, redes sociales) en Tucacas, empezando por el Conjunto Residencial **Pescadores 1** y conjuntos vecinos. Un operador local entrega, instala, retira y da mantenimiento a las máquinas, de modo que la persona de limpieza pueda lavar sábanas, fundas y toallas en cada cambio de huésped sin que el propietario tenga que comprar y mantener una lavadora que el salitre destruye cuando está quieta.

## Cliente y contexto

- **Cliente / dueño del negocio:** propietario de un apartamento en Pescadores 1 (Tucacas, Falcón) que lo usa como inversión y para disfrute propio.
- **Primer usuario real (dogfooding):** el propio apartamento del cliente.
- **Mercado:** anfitriones del mismo conjunto, conjuntos vecinos, posadas pequeñas, embarcaciones/marinas y familias residentes.

## Índice de documentos

| # | Documento | Qué responde |
|---|-----------|--------------|
| 00 | [Resumen ejecutivo](docs/00-resumen-ejecutivo.md) | La idea en 2 minutos, decisiones clave |
| 01 | [Contexto y problema](docs/01-contexto-y-problema.md) | Qué duele y a quién |
| 02 | [Investigación de mercado y entorno](docs/02-investigacion-mercado.md) | Tucacas, Venezuela: agua, luz, pagos, WhatsApp, estacionalidad |
| 03 | [Análisis de la competencia](docs/03-analisis-competencia.md) | Qué copiar, qué evitar, dónde está el hueco |
| 04 | [Propuesta de valor y modelo de negocio](docs/04-propuesta-valor-modelo-negocio.md) | Planes, precios hipótesis, extras que añadimos |
| 05 | [Usuarios y personas](docs/05-usuarios-personas.md) | Quién usa, quién paga, quién decide |
| 06 | [Requisitos](docs/06-requisitos.md) | Funcionales, no funcionales, priorización MoSCoW |
| 07 | [Reglas de negocio y políticas](docs/07-reglas-negocio.md) | Cancelaciones, daños, cortes de luz/agua, depósitos |
| 08 | [Flujos y casos de uso](docs/08-flujos-casos-uso.md) | Diagramas de proceso y estados |
| 09 | [Diseño de la solución](docs/09-diseno-solucion.md) | Arquitectura, modelo de datos, catálogo (wireframes de texto), IoT |
| 10 | [Operaciones y logística](docs/10-operaciones-logistica.md) | Flota, turnos, mantenimiento anticorrosión, entrega |
| 11 | [Finanzas y unit economics](docs/11-finanzas.md) | Inversión, escenarios, punto de equilibrio |
| 12 | [Riesgos](docs/12-riesgos.md) | Matriz de riesgos y mitigaciones |
| 13 | [Legal y fiscal (a validar)](docs/13-legal-fiscal.md) | IVA, IGTF, condominio, contratos |
| 14 | [Roadmap y plan de validación](docs/14-roadmap.md) | Fases, hitos, métricas |
| 15 | [Preguntas abiertas](docs/15-preguntas-abiertas.md) | Lo que necesitamos preguntarle al cliente / validar en campo |
| 16 | [Fuentes y límites de la investigación](docs/16-fuentes.md) | De dónde sale cada dato y qué es suposición |

## Convenciones

- **[HIPÓTESIS]** = suposición que debe validarse en campo (no es un dato verificado).
- **[DATO]** = respaldado por una fuente citada en `docs/16-fuentes.md`.
- Precios en **USD** como moneda de referencia; equivalente en Bs a tasa BCV del día.
- Idioma: español (Venezuela).
