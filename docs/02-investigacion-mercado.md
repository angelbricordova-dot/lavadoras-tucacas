# 02 · Investigación de mercado y entorno (Tucacas / Venezuela)

> Todo lo marcado [DATO] proviene de las fuentes en `16-fuentes.md`. Lo marcado [HIPÓTESIS] se debe validar en campo. No se encontró información pública específica sobre **Pescadores 1** ni sobre la cantidad de apartamentos turísticos del conjunto: es lo primero que hay que levantar (censo).

## 1. Oferta turística en Tucacas

- [DATO] Airbnb lista **~40 propiedades en condominios de Tucacas** desde ~USD 30/noche, y ~320 con acceso a playa desde ~USD 20/noche. Hay anuncios identificados con conjuntos tipo "Pescadores III". → Hay oferta concentrada y precio bajo: el margen del anfitrión es ajustado, **sensibles al costo de lavado**.
- [DATO] La economía de Tucacas, Boca de Aroa y alrededores se mueve ~**70 % por turismo** (Parque Nacional Morrocoy).
- [DATO] Falcón proyectó **> 90 % de ocupación en Carnaval 2026**; destinos como Morrocoy rondaron **> 50 % en Semana Santa 2026**.
- **Implicación:** demanda **muy estacional y de picos** (fines de semana, Carnaval, Semana Santa, agosto, Navidad). La flota debe dimensionarse para picos moderados y tener un plan de uso en temporada baja (ver doc 04: segmentos alternos).

## 2. Servicios públicos: agua y electricidad

- [DATO] Medios regionales (2026) describen a **Falcón entre los estados más vulnerables en servicios públicos**: fallas eléctricas diarias en los 25 municipios y agua por tubería que llega **cada 40–50 días** en algunas comunidades; camiones cisterna alrededor de **USD 10 por tanque** en algunos sectores. Se menciona colapso de servicios en Tucacas.
- **Implicaciones de diseño (críticas):**
  1. La lavadora consume agua (≈ 40–100 L por ciclo según modelo [HIPÓTESIS, verificar ficha técnica]). Elegir **modelos de bajo consumo de agua** (carga frontal, "HE").
  2. Antes de entregar: **checklist de agua** (tanque/cisterna con volumen suficiente) y **de energía** (tomacorriente 110 V/220 V, estado del cableado).
  3. **Protector de voltaje / regulador** incluido en el kit: las fluctuaciones queman equipos ("muchas familias han perdido electrodomésticos").
  4. Política de **ciclo interrumpido por corte** (doc 07).
  5. Considerar un **punto de lavado (hub)** propio con tanque de agua y planta eléctrica/inversor (fase 2): independiza del apartamento del cliente.

## 3. Pagos y economía digital

- [DATO] El **IGTF de 3 %** grava pagos en divisas en efectivo (o cripto fuera del sistema financiero) además del **IVA 16 %**; **no aplica** al pagar en bolívares. En 2026 el bolívar ganó participación en transacciones comerciales (≈ 53 % en abril).
- [DATO] Zelle es muy usado por quien tiene cuenta en EE. UU.; **Pago Móvil** es el estándar para pagos en Bs. Airbnb permite cobro a anfitriones vía PayPal/Payoneer/transferencia internacional según país (los anfitriones venezolanos ya manejan esto).
- [DATO] Casi todas las transacciones comerciales en Venezuela son digitales; el pago móvil representa ~42 % de las transacciones (reportes 2026).
- **Implicaciones:** precios en USD, cobro en Bs (tasa BCV) por **Pago Móvil** como opción primaria (evita IGTF), Zelle/efectivo USD como alternativas; conciliación por **referencia** (manual al inicio, automatizable después).

## 4. Canales de comunicación

- [DATO] **> 90 % de los usuarios de smartphone en Venezuela tienen WhatsApp**; los catálogos de WhatsApp Business y los grupos se usan ampliamente para vender.
- **Implicación:** el producto debe vivir **dentro de WhatsApp**: catálogo, reserva, confirmación, recordatorios, seguimiento. La web/PWA es complemento. Internet puede ser inestable → **diseño ligero, tolerante a baja conectividad**.

## 5. Corrosión por salitre

- [DATO general] La exposición al salitre/humedad acelera la corrosión; los fabricantes y guías de mantenimiento recomiendan proteger la lavadora de humedad, sol y salpicaduras, y mantener el equipo nivelado y seco.
- [HIPÓTESIS del cliente] El uso constante reduce el daño frente a la inmovilidad. No se halló evidencia pública directa; **validar con 2 técnicos de la zona** y llevar un registro de fallas desde el piloto.
- **Implicaciones:** almacén techado y ventilado ("depósito"), **lavado/enjuague externo** y spray anticorrosión periódico, **rotación** de la flota, vida útil conservadora (36 meses en finanzas).

## 6. Mercados análogos en Latinoamérica

- [DATO] En Medellín existen negocios de **alquiler de lavadoras** de pequeña escala (p. ej., Aburrá: de 3 a 14 máquinas) que generaron empleo directo. Valida que el modelo funciona a escala artesanal.

## 7. Hallazgos de investigación pendientes (campo)

1. Censo de apartamentos de Pescadores 1 y conjuntos vecinos (Pescadores II/III, otros).
2. ¿Cuántos tienen conexión de lavadora (toma de agua + desagüe)?
3. ¿Quién limpia hoy y dónde lava? Precio actual del lavado de un juego de lencería.
4. ¿Qué reglas impone la junta de condominio?
5. Precios de lavadoras nuevas y usadas en Falcón/Valencia, repuestos y técnicos disponibles.
