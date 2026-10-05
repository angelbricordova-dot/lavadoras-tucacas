# 05 · Usuarios y personas

Insight central: **quien paga no es quien usa**. El anfitrión paga, la persona de limpieza opera la lavadora, el operador la lleva. El diseño debe servir a los tres sin exigirles una app.

## Roles

| Rol | Descripción | Canal | Permisos |
|-----|-------------|-------|----------|
| **Anfitrión (propietario)** | Dueño del apartamento; paga; ve disponibilidad y facturas | WhatsApp + PWA | Reservar, pagar, autorizar delegados, ver historial |
| **Anfitrión remoto** | Vive fuera (Caracas/Valencia); coordina a distancia | WhatsApp | Igual; recibe confirmaciones y fotos |
| **Persona de limpieza (delegada)** | Usa la lavadora a diario | WhatsApp (sin app) | Solicitar/confirmar "terminé", reportar problema, según autorización del anfitrión |
| **Operador/mensajero** | Entrega, conecta, retira, revisa | App móvil simple (PWA) | Ver tareas, fotos, escanear QR de máquina, cerrar tareas |
| **Administrador (cliente)** | Dueño del negocio | Panel web | Todo: flota, precios, reportes, usuarios |
| **Técnico** | Mantenimiento externo | WhatsApp | Recibe órdenes de servicio |
| **Junta/administración del conjunto** | Autoriza accesos | Documento / WhatsApp | Lista de operadores autorizados |

## Personas

### Marlene, 48 — persona de limpieza
- Limpia 6–8 apartamentos por semana en Pescadores.
- Hoy lleva sábanas a su casa en moto-taxi; se atrasa en feriados.
- Usa WhatsApp todo el día; **no** instala apps nuevas. Escribe con notas de voz.
- Necesita: saber a qué hora llega la máquina, que sea fácil de conectar, que no la culpen si hay un corte.
- **Diseño:** bot por **nota de voz y botones**; mensajes cortos; confirmación de "máquina lista/ya terminé".

### Carlos, 39 — anfitrión remoto (Valencia)
- Un apartamento, ocupación fin de semana + feriados; precio de noche USD 45.
- Pierde reseñas por "sábanas con olor".
- Paga en USD (Zelle) o Pago Móvil. Quiere **evidencia** (fotos) y **cero sorpresas**.
- **Diseño:** reserva recurrente automática vinculada a su calendario; fotos de entrega/retiro; recibo claro.

### Ana, 55 — propietaria residente
- Vive en el conjunto, alquila 2 habitaciones. Quiere pagar solo cuando usa.
- **Diseño:** ciclo suelto y pase 24 h; sin membresías obligatorias.

### Don Rafael, 60 — operador/mensajero
- Conoce el conjunto y las juntas; tiene moto/carrito.
- **Diseño:** lista de tareas del día en PWA o incluso WhatsApp; QR para registrar máquina; funciona con señal débil.

### El cliente (dueño del negocio)
- Quiere ver, de un vistazo: qué máquinas están afuera, ingresos del mes, quién debe, alertas de mantenimiento.
- **Diseño:** panel simple, 5 indicadores, exportable a Excel.

## Jobs To Be Done

1. *Cuando termina un huésped,* quiero **lavar toda la lencería hoy mismo**, para **recibir al siguiente a tiempo**.
2. *Cuando hay feriado,* quiero **asegurar la máquina con anticipación**, para **no quedarme sin lavar**.
3. *Cuando la luz se va a mitad de ciclo,* quiero **que no me cobren ni me dejen colgada**, para **confiar en el servicio**.
4. *Cuando estoy lejos,* quiero **ver que se hizo bien**, para **no tener que llamar a nadie**.
