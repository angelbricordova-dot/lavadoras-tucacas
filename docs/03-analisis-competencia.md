# 03 · Análisis de la competencia

> **Límite honesto:** la búsqueda web no encontró competidores venezolanos ni de Tucacas con presencia digital que alquilen lavadoras. La competencia **local real** es informal (señoras que lavan, lavanderías, WhatsApp) y debe levantarse en campo. Lo de abajo son **modelos análogos internacionales** de los que sí aprendemos.

## 1. Mapa de competidores / referentes

| Referente | Modelo | Precio (dato público) | Qué hace bien | Dónde falla |
|-----------|--------|-----------------------|---------------|-------------|
| **Bundles** (Países Bajos) | Suscripción: lavadora Miele en casa, pago por uso, enchufe inteligente mide ciclos y avisa de servicio | €18,95 / 15 ciclos · €19,95 / 25 · €21,95 / 35 al mes | Medición automática, mantenimiento incluido, relación precio-uso clara | Reseñas: **cargos ocultos**, **€125 de tarifa de reubicación/salida**, penalizaciones que vuelven "más barato" comprar |
| **Rentomojo** (India) | Alquiler de electrodomésticos por plazos | ₹665–812/mes (lavadora 8 kg; 3 vs 11 meses) | Plazos con descuento por permanencia; incluye mantenimiento y reubicación | Plazos largos; pensado para residentes, no para usos intermitentes |
| **Rent-A-Center / Aaron's** (EE. UU.) | Alquiler con opción a compra; incluyen entrega, instalación y reparaciones | Varía | Todo incluido; sin historial de crédito | (conocimiento general) costo total alto frente a comprar; no pensado para uso por horas |
| **Aburrá y similares** (Medellín) | Alquiler local por días/semana | Local | Funciona con pocas máquinas; empleo directo | Sin catálogo ni disponibilidad en vivo; logística manual |
| **BnB Laundry** (Londres) | Lavandería y alquiler de lencería para Airbnb; ventana de entrega de 3 h; pago por uso, sin contrato | Por paquete | **Entrega rápida garantizada, sin contrato**, lencería de calidad hotelera | Requiere planta central; la lencería sale del inmueble; no existe en Tucacas |
| **WashHouse / The Laundry Hub** (Dubái) | Lavandería y planchado para casas vacacionales; opción de alquiler de lencería | Por paquete | Paquetes por tipo de propiedad, recogida/entrega | Igual: dependen de logística y planta centralizada |
| **HappyNest / Love2Laundry** | App de recogida y entrega, "Airbnb" como segmento | Por kg/ítem | App con preferencias, día siguiente | Modelo urbano de alta densidad; no resuelve el lavado *in situ* |
| **Turno (ex TurnoverBnB)** (EE. UU.) | Software de turnos de limpieza: sincroniza calendarios, asigna limpiador principal y de respaldo, checklists con fotos, pago automático | Desde ~USD 96/propiedad/año; 93 % de reseñas positivas | **Sincronización de calendario**, respaldo automático, evidencia con fotos | Reseñas piden facturación/pago a limpiadores más claro; no cubre equipos ni lencería |
| **Fat Llama / Peerby** (marketplaces P2P) | Alquiler de objetos entre personas | Comisión | Confianza: verificación, garantías, seguro; Fat Llama respondió con su dinero a daños | Tiempos de respuesta lentos ante daños (≈ 1 semana); reparaciones de >1 mes |
| **Informal local** (Tucacas) | Señoras que lavan, lavanderías, grupos de WhatsApp | A levantar | Cercanía, confianza, precio | Sin garantías, sin capacidad en picos, calidad variable |

## 2. Qué copiamos (mejores prácticas)

1. **Medición con enchufe inteligente** (Bundles) → usamos sensor de consumo para saber estado real y cobrar justo.
2. **Mantenimiento y reubicación incluidos** (Rentomojo, Rent-A-Center) → "todo incluido" como promesa.
3. **Ventana de entrega comprometida y sin contrato** (BnB Laundry) → SLA de entrega y planes sin permanencia forzada.
4. **Sincronización de calendario + respaldo** (Turno) → importar iCal del anuncio y reservar el lavado automáticamente tras el check-out; si el operador falla, hay lavadora/operador de respaldo.
5. **Checklists con fotos** (Turno) → fotos de entrega y retiro para evidenciar estado de la máquina (protege a ambas partes).
6. **Confianza antes que tecnología** (Fat Llama) → garantía clara de daños y respuesta rápida.
7. **Descuento por plazo** (Rentomojo) → membresías mensual/trimestral con precio decreciente.

## 3. Qué evitamos (errores de la competencia)

| Error observado | Cómo lo evitamos |
|-----------------|------------------|
| Cargos ocultos / cuotas de salida (Bundles) | **Precio total visible antes de reservar**; cero cargos por cancelar membresía; cargos de reubicación solo si el cliente pide mover el equipo fuera de zona, informados por adelantado |
| Respuesta lenta a daños (Fat Llama) | **SLA de 24 h** para atender una avería; lavadora de reemplazo del stock de respaldo |
| Contratos largos para uso intermitente | Planes **por ciclo y por día** además de mensuales; pausar membresía en temporada baja |
| Software que ignora el equipo físico (Turno) | Nuestro eje es el **activo físico** + calendario |
| Logística pesada y planta central (BnB Laundry, Dubái) | Lavado **in situ** con la máquina; hub solo en fase 2 |
| Asumir infraestructura estable | Diseño para **cortes de agua y luz** (doc 07) |
| Interfaces solo-app | **WhatsApp primero** |

## 4. El hueco (posicionamiento)

```
                      Equipo físico
                           ▲
        Bundles/Rentomojo  │   ★ LavaTuca
        (hogares, largo    │   (anfitriones, por ciclo/día/mes,
         plazo)            │    disponibilidad en vivo, calendario)
  ◄────────────────────────┼────────────────────────►
   Genérico                │                Turismo / STR
        Fat Llama          │   Turno, BnB Laundry,
        (P2P objetos)      │   WashHouse (software / lavandería)
                           ▼
                       Servicio / software
```

**Nadie combina**: equipo en alquiler + disponibilidad en vivo + integración con el calendario del anfitrión + entrega local, en un entorno con servicios públicos inestables y pagos mixtos en USD/Bs.

## 5. Ventajas defendibles (moat)

1. **Densidad local:** operador y depósito en Tucacas; ningún competidor remoto entrega en 60 min.
2. **Datos de ocupación:** al enlazar calendarios (con permiso) se anticipa la demanda y se prepara la flota.
3. **Confianza:** garantías claras + presencia física + referidos del conjunto.
4. **Conocimiento técnico costero:** protocolo anticorrosión propio y registro de fallas.

## 6. Trabajo de campo de competencia (pendiente)

- Visitar lavanderías de Tucacas/Chichiriviche; anotar precio por kg/ juego, tiempo, disponibilidad.
- Preguntar a 5 señoras de limpieza cómo lavan hoy y cuánto cobran.
- Buscar ferreterías/electrodomésticos que alquilen equipos en Falcón.
