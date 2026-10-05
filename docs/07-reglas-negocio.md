# 07 · Reglas de negocio y políticas

> Borrador para validar con el cliente y con un abogado/contador local. Cada regla tiene ID para referenciarla en requisitos y pruebas.

## 1. Reservas y disponibilidad

| ID | Regla |
|----|-------|
| RN-01 | Una lavadora solo puede estar en **un** estado a la vez (Disponible, Reservada, En ruta, En uso, En recojo, En mantenimiento, Baja). |
| RN-02 | Entre dos reservas se aplica un **margen de limpieza/traslado** (por defecto 45 min). |
| RN-03 | La franja mínima de un pase 24 h es de 24 h contadas desde la entrega confirmada. |
| RN-04 | Prioridad ante conflicto: (1) Membresía de temporada con anticipo, (2) Membresía mensual, (3) Pase 24 h, (4) Ciclo suelto. Empate → orden de reserva. |
| RN-05 | El estado "se libera en ~N min" se calcula con el sensor; si no hay lectura, con el temporizador del plan (3 h por ciclo) y se marca como *estimado*. |
| RN-06 | Lista de espera: al liberarse una lavadora se notifica por orden; 15 min para confirmar. |

## 2. Cancelaciones y reprogramación

| ID | Regla |
|----|-------|
| RN-10 | Cancelación gratis hasta **2 h antes** de la entrega (24 h antes en feriados). |
| RN-11 | Cancelación tardía: cargo del **50 %** del precio del pase (cubre el traslado). |
| RN-12 | Si la empresa cancela o llega con > 60 min de retraso por su causa: **crédito del 100 %** y prioridad en la siguiente reserva. |
| RN-13 | Reprogramar es gratis una vez por reserva; después, sujeto a disponibilidad. |

## 3. Cortes de luz y agua (diferenciador)

| ID | Regla |
|----|-------|
| RN-20 | Antes de entregar: **checklist** de agua (volumen del tanque ≥ mínimo del modelo) y energía (toma y voltaje). Si no pasa, se reprograma sin cargo. |
| RN-21 | Si un **corte de luz o agua** interrumpe un ciclo, **no se cobra** ese ciclo (ciclo suelto) o se **extiende** el pase por el tiempo perdido (pase 24 h). La evidencia es el registro del sensor o el reporte de la persona de limpieza (con foto). |
| RN-22 | Fluctuación de voltaje: el protector es obligatorio; si el cliente lo retira y hay falla, aplica cláusula de daños. |
| RN-23 | Si el apartamento no tiene agua en el pase, el cliente puede devolver la máquina sin cargo hasta 1 h después de la entrega. |

## 4. Daños, pérdida y mantenimiento

| ID | Regla |
|----|-------|
| RN-30 | **Depósito reembolsable** (USD 20) o **cuota de protección** de USD 1 por pase, a elección del cliente. |
| RN-31 | Desgaste normal y daños por **salitre/humedad** no se cobran al cliente. |
| RN-32 | Daños por mal uso (golpes, objetos metálicos, sobrecarga, conexión indebida) se descuentan del depósito hasta el costo de reparación; fotos de entrega/retiro como evidencia. |
| RN-33 | Avería no atribuible al cliente: **reemplazo en ≤ 24 h** sin costo. |
| RN-34 | Cada máquina recibe **limpieza externa y enjuague anticorrosión** al retorno y revisión técnica cada 100 ciclos o 60 días. |
| RN-35 | Pérdida/robo: costo de reposición menos depreciación (36 meses lineal). |

## 5. Pagos

| ID | Regla |
|----|-------|
| RN-40 | Precios publicados en **USD**; se muestra el equivalente en Bs a la tasa BCV del día de pago. |
| RN-41 | **Pago Móvil** y bolívares no generan IGTF; pagos en divisa en efectivo **sí** (3 %), mostrado antes de confirmar. *(Validar con contador.)* |
| RN-42 | Pase 24 h y ciclo: pago al reservar o contra entrega (efectivo/Pago Móvil). Membresía: pago por adelantado; **sin penalización de salida**. |
| RN-43 | Mora: sin reservas nuevas con saldo vencido > 7 días; recordatorio por WhatsApp a los 3 y 7 días. |
| RN-44 | Reembolsos en el mismo medio de pago o como crédito, a elección del cliente, en ≤ 72 h. |

## 6. Delegados y seguridad

| ID | Regla |
|----|-------|
| RN-50 | El anfitrión autoriza por nombre y teléfono a sus delegados; cada acción del delegado queda registrada. |
| RN-51 | El delegado **no puede** pagar ni cambiar planes; solo solicitar, confirmar, reportar. |
| RN-52 | El operador solo ingresa al conjunto con el listado aprobado por la junta; los datos de acceso no se comparten por mensajes abiertos. |

## 7. Operación

| ID | Regla |
|----|-------|
| RN-60 | Horario de servicio estándar: 6:00–22:00; fuera de horario solo emergencias con recargo informado. |
| RN-61 | **Tiempo de respuesta**: confirmación en ≤ 10 min en horario de servicio; entrega ≤ 60 min en Tucacas. |
| RN-62 | Una lavadora no se asigna si su **última inspección** tiene alerta crítica. |
| RN-63 | Máximo de lavadoras por cliente simultáneas: 2 (excepción: posadas). |

## 8. Atención al cliente

| ID | Regla |
|----|-------|
| RN-70 | Cualquier reclamo se responde en ≤ 2 h hábiles; resolución ≤ 24 h. |
| RN-71 | Encuesta de 1 pregunta por WhatsApp tras cada servicio (1–5 + comentario). |
