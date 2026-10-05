# 06 · Requisitos

Priorización MoSCoW: **M** (imprescindible MVP) · **S** (debería) · **C** (podría) · **W** (no por ahora).

## 1. Requisitos funcionales

### Catálogo y disponibilidad
| ID | Requisito | P |
|----|-----------|---|
| RF-01 | Listar lavadoras con foto, capacidad (kg), tipo, estado y tarifa | M |
| RF-02 | Mostrar estado en vivo: **Disponible ahora · Se libera en ~N min · Reservada desde HH:MM · En ruta · En uso · Mantenimiento** | M |
| RF-03 | Mostrar "próxima disponibilidad" por lavadora y por zona (conjunto) | M |
| RF-04 | Lista de espera: "avísame cuando haya una" | S |
| RF-05 | Filtros por capacidad, zona y fecha | S |

### Reserva y programación
| ID | Requisito | P |
|----|-----------|---|
| RF-10 | Reservar por ciclo, pase 24 h, membresía o temporada | M |
| RF-11 | Elegir franja horaria de entrega y de retiro | M |
| RF-12 | Reprogramar y cancelar según política (doc 07) | M |
| RF-13 | Importar calendario iCal del anuncio y proponer lavados post check-out | S |
| RF-14 | Reservas recurrentes (cada fin de semana) | S |
| RF-15 | Prioridad automática por tipo de plan y por antigüedad | S |

### Despacho y operación
| ID | Requisito | P |
|----|-----------|---|
| RF-20 | Asignar tarea de entrega/retiro a un operador con orden sugerido de ruta | M |
| RF-21 | Checklist de entrega: agua OK, voltaje OK, mangueras, fotos de la máquina | M |
| RF-22 | Escaneo de **QR de máquina** para registrar entrega/retiro/limpieza | M |
| RF-23 | Registrar cortes de luz/agua durante un ciclo y generar crédito automático | M |
| RF-24 | Órdenes de mantenimiento y bitácora por máquina | M |
| RF-25 | Máquina de reemplazo en ≤ 24 h | S |

### Usuarios y delegados
| ID | Requisito | P |
|----|-----------|---|
| RF-30 | Registro de anfitrión (nombre, apartamento, conjunto, teléfono) | M |
| RF-31 | Delegados autorizados (persona de limpieza) con PIN y alcance limitado | M |
| RF-32 | Verificación básica del cliente (cédula/teléfono/referencia de vecino) | S |
| RF-33 | Aprobación de acceso por conjunto (lista de operadores autorizados) | S |

### Pagos y facturación
| ID | Requisito | P |
|----|-----------|---|
| RF-40 | Precios en USD con equivalente en Bs (tasa BCV configurable) | M |
| RF-41 | Registrar pagos: Pago Móvil (referencia), Zelle, efectivo USD, transferencia | M |
| RF-42 | Aviso de IGTF 3 % en pagos en divisa efectiva | M |
| RF-43 | Recibos/ comprobantes por WhatsApp | M |
| RF-44 | Estado de cuenta, saldo a favor, créditos | S |
| RF-45 | Conciliación semiautomática de Pago Móvil | C |
| RF-46 | Facturación fiscal según requerimiento legal (a validar) | S |

### Comunicación
| ID | Requisito | P |
|----|-----------|---|
| RF-50 | Bot de WhatsApp: ver catálogo, reservar, preguntar estado, reportar problema | M |
| RF-51 | Notificaciones: confirmación, "operador en camino", recordatorio de retiro, cobro | M |
| RF-52 | Mensajes por nota de voz transcritos / atención por humano como respaldo | C |

### Administración y reportes
| ID | Requisito | P |
|----|-----------|---|
| RF-60 | Panel: utilización por máquina, ingresos, morosidad, tareas del día | M |
| RF-61 | Gestión de precios, planes, promociones y feriados | M |
| RF-62 | Exportar a Excel/CSV | M |
| RF-63 | Alertas de mantenimiento por ciclos/horas | S |

### IoT
| ID | Requisito | P |
|----|-----------|---|
| RF-70 | Enchufe inteligente con medición de consumo: detectar "en uso/idle" y ciclos | S |
| RF-71 | Estimar fin de ciclo para "se libera en ~N min" | S |
| RF-72 | **Respaldo manual** (temporizador/confirmación) si no hay conectividad | M |

## 2. Requisitos no funcionales

| ID | Categoría | Requisito |
|----|-----------|-----------|
| RNF-01 | Conectividad | Debe funcionar con datos móviles inestables; carga inicial < 200 KB; modo offline para operadores con sincronización posterior |
| RNF-02 | Resiliencia | Tolerar cortes de energía: sin pérdida de datos; el estado se reconstruye al reconectar |
| RNF-03 | Usabilidad | Persona de limpieza completa una reserva en ≤ 4 mensajes; textos simples; botones y audio |
| RNF-04 | Disponibilidad | 99 % de lunes a domingo 6:00–22:00 (hosting en la nube) |
| RNF-05 | Seguridad | Autenticación por teléfono (OTP/WhatsApp); roles; datos mínimos; registros de auditoría |
| RNF-06 | Privacidad | Solo datos necesarios; consentimiento para leer el calendario; no compartir con terceros |
| RNF-07 | Costos | Costo mensual de infraestructura < USD 40 en el piloto |
| RNF-08 | Escalabilidad | Soportar 100 clientes y 30 lavadoras sin rediseño |
| RNF-09 | Mantenibilidad | Software modular; configuración de precios sin código |
| RNF-10 | Localización | Español (VE), fechas DD/MM, zona horaria America/Caracas, USD/Bs |
| RNF-11 | Accesibilidad | Contraste alto, tipografías grandes, uso con una mano |

## 3. Restricciones

- Presupuesto y equipo pequeños; operación local.
- No depender de una sola pasarela de pago (acceso internacional limitado).
- Proveedores de tarjeta/PayPal pueden no estar disponibles: **no** se diseña dependiente de ellos.
- Normativa del condominio y legislación fiscal (doc 13).

## 4. Criterios de aceptación del MVP (operativo, sin web)

1. 2 lavadoras alquiladas ≥ 20 ciclos en 4 semanas con registro completo en hoja de cálculo.
2. 0 incidentes graves de seguridad/ daños sin resolver.
3. ≥ 8 anfitriones registrados y ≥ 3 recurrentes.
4. Entrega promedio ≤ 60 min.
