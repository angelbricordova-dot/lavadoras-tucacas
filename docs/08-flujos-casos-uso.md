# 08 · Flujos y casos de uso

Los diagramas usan Mermaid (se renderizan en GitHub).

## 1. Casos de uso principales

| ID | Caso de uso | Actor |
|----|-------------|-------|
| CU-01 | Ver catálogo y disponibilidad | Anfitrión, delegado |
| CU-02 | Reservar una lavadora (ciclo / 24 h) | Anfitrión, delegado* |
| CU-03 | Contratar membresía | Anfitrión |
| CU-04 | Entregar e instalar la lavadora | Operador |
| CU-05 | Usar y terminar ("ya terminé") | Delegado |
| CU-06 | Retirar y revisar la lavadora | Operador |
| CU-07 | Reportar falla / corte de luz-agua | Delegado, anfitrión |
| CU-08 | Sincronizar calendario y agendar post check-out | Anfitrión, sistema |
| CU-09 | Pagar y registrar pago | Anfitrión, administrador |
| CU-10 | Mantenimiento programado | Operador, técnico |
| CU-11 | Gestionar flota, precios y reportes | Administrador |

\* El delegado solicita; el anfitrión (o su plan activo) paga.

## 2. Flujo: reservar y entregar

```mermaid
sequenceDiagram
    participant H as Anfitrión/Delegada
    participant B as Bot WhatsApp
    participant S as Sistema
    participant O as Operador
    H->>B: "Necesito lavadora hoy 12 pm"
    B->>S: consulta disponibilidad (zona, hora)
    S-->>B: Lavadora #3 disponible 12:00; #5 se libera 12:40
    B-->>H: Opciones + precio total (USD y Bs)
    H->>B: Elige #3, pase 24 h
    B->>S: crea reserva (pendiente de pago)
    S-->>H: datos de pago (Pago Móvil / Zelle / efectivo)
    H->>B: envía referencia de pago
    S->>S: valida pago (manual o automático)
    S-->>O: tarea de entrega #3 (checklist, QR)
    O->>H: "Voy en camino" (ETA)
    O->>S: escanea QR, checklist agua/voltaje, fotos
    S-->>H: confirmación de entrega + instrucciones
```

## 3. Flujo: ciclo con corte de luz/agua

```mermaid
flowchart TD
    A[Ciclo en curso] --> B{¿Corte de luz o agua?}
    B -- No --> C[Ciclo termina; delegada confirma 'terminé']
    B -- Sí --> D[Sensor/delegada reporta + foto]
    D --> E{Plan}
    E -- Ciclo suelto --> F[No se cobra el ciclo]
    E -- Pase 24 h --> G[Se extiende el pase por el tiempo perdido]
    F --> H[Operador reinicia ciclo si se solicita]
    G --> H
    H --> C
```

## 4. Estados de la lavadora

```mermaid
stateDiagram-v2
    [*] --> Disponible
    Disponible --> Reservada: reserva confirmada
    Reservada --> EnRuta: operador sale
    EnRuta --> EnUso: entrega + checklist OK
    EnRuta --> Disponible: checklist falla (reprogramar)
    EnUso --> EnRecojo: cliente termina o vence el pase
    EnRecojo --> Revision: operador retira
    Revision --> Disponible: limpieza + revisión OK
    Revision --> Mantenimiento: falla detectada
    Mantenimiento --> Disponible: reparada
    Mantenimiento --> Baja: irreparable / corrosión
    Baja --> [*]
```

## 5. Estados de la reserva

```mermaid
stateDiagram-v2
    [*] --> Solicitada
    Solicitada --> PendientePago
    PendientePago --> Confirmada: pago validado
    PendientePago --> Expirada: sin pago en 30 min
    Confirmada --> EnCurso: entrega completada
    Confirmada --> Cancelada: según política
    EnCurso --> Completada: retiro completado
    EnCurso --> Incidente: falla/daño
    Incidente --> Completada: resuelto
    Completada --> [*]
```

## 6. Flujo: sincronización con calendario (iCal)

1. El anfitrión pega el enlace iCal del anuncio (o lo envía por WhatsApp).
2. El sistema lee los check-out de los próximos 30 días (solo fechas; sin datos del huésped).
3. Para cada check-out propone: *"El sábado 11:00 sale tu huésped. ¿Reservo lavadora para 12:00–24 h?"*
4. El anfitrión acepta una vez ("hazlo siempre") o confirma cada vez.
5. Si cambia el calendario, se reprograma o se avisa.

## 7. Flujo de lencería con intercambio (fase 2)

```mermaid
flowchart LR
    A[Check-out] --> B[Delegada retira lencería sucia]
    B --> C[Operador entrega juego limpio al instante]
    C --> D[Lencería sucia al hub]
    D --> E[Lavado + secado + doblado]
    E --> F[Stock limpio]
    F --> C
```
