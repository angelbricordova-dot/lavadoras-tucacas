# 11 · Finanzas y unit economics

> **Todo es [HIPÓTESIS]**: los precios de compra, salarios y niveles de uso son supuestos para modelar; deben sustituirse por cotizaciones reales y datos del piloto. Las cifras se calcularon con un script reproducible (ver al final).

## 1. Supuestos

| Supuesto | Valor |
|----------|-------|
| Flota piloto | 6 lavadoras |
| Costo por lavadora (compra) | USD 450 |
| Accesorios por máquina (protector, mangueras, enchufe inteligente, QR) | USD 20 |
| **Inversión en flota** | 6 × 470 = **USD 2.820** |
| Vida útil (conservadora por salitre) | 36 meses |
| Depreciación mensual | 2.820 / 36 ≈ **USD 78** |
| Operador (parcial) | USD 200/mes |
| Reserva de mantenimiento y repuestos | 3 % de la inversión/mes ≈ **USD 85** |
| Software, WhatsApp, hosting | USD 30/mes |
| Comisiones/IGTF/otros sobre ingresos | 3 % |
| Precio medio por ciclo-equivalente | USD 3,0 / 3,5 / 4,0 según escenario |
| Electricidad y agua del ciclo | **a cargo del cliente** (se informa en la reserva) |

Costos fijos mensuales de caja = 200 + 85 + 30 = **USD 315**; con depreciación = **USD 393**.

## 2. Escenarios mensuales (flota de 6)

| Escenario | Ciclos por máquina/mes | Precio medio | Ingresos | Comisiones 3 % | Margen de caja | Margen neto (tras depreciación) | Recuperación de inversión |
|-----------|-----------------------|--------------|----------|----------------|----------------|--------------------------------|---------------------------|
| Conservador | 25 | 3,0 | 450 | 14 | **122** | 44 | ≈ 23 meses |
| **Base** | 45 | 3,5 | 945 | 28 | **602** | 524 | ≈ 4,7 meses |
| Optimista | 70 | 4,0 | 1.680 | 50 | **1.315** | 1.237 | ≈ 2,1 meses |

> Nota: el margen de caja no incluye el sueldo del propietario ni impuestos sobre la renta. "Ciclo-equivalente" convierte pases 24 h y membresías a ciclos usados para modelar.

## 3. Punto de equilibrio

- **Caja:** 315 / (3,5 × 0,97) ≈ **93 ciclos/mes** en toda la flota ≈ **15 ciclos por máquina** (≈ medio ciclo al día).
- **Con depreciación:** ≈ **116 ciclos/mes** ≈ 19 por máquina.
- Conclusión: el negocio es **sensible a la utilización más que al precio**. Con 6 máquinas basta, aproximadamente, con 5–6 anfitriones recurrentes (≈ 4 ciclos por semana cada uno ≈ 17 ciclos/mes) para cubrir costos de caja.

## 4. Palancas de rentabilidad

1. **Utilización:** sumar segmentos (posadas, embarcaciones, residentes) para llenar la temporada baja.
2. **Mix de planes:** el pase de 24 h y la membresía suben ingreso por máquina sin más traslados.
3. **Insumos y kit:** margen alto (jabón, suavizante, bolsas).
4. **Eficiencia de ruta:** agrupar entregas por torre.
5. **Lavadoras usadas bien revisadas** para la flota ampliable (menor capex).
6. **Hub y lencería (fase 2):** ingreso recurrente por kilo y por intercambio.
7. **Referidos y alianzas** que reducen el costo de adquisición.

## 5. Sensibilidad (flota de 6, precio 3,5)

| Ciclos por máquina/mes | Margen de caja aprox. (USD) |
|------------------------|-----------------------------|
| 15 | ≈ 0 |
| 25 | ≈ 194 |
| 35 | ≈ 398 |
| 45 | ≈ 602 |
| 60 | ≈ 907 |

(Cálculo: ciclos × 6 × 3,5 × 0,97 − 315.)

## 6. Fuentes de financiamiento y fases de inversión

| Fase | Inversión orientativa | Condición para avanzar |
|------|----------------------|------------------------|
| Piloto | 2 lavadoras + kit + depósito ≈ USD 1.000–1.300 | ≥ 20 ciclos en 4 semanas, ≥ 8 clientes registrados |
| Ampliación | +4 lavadoras ≈ USD 1.900 | Utilización ≥ 40 % en 8 semanas |
| Hub | Local + tanque + 2–3 equipos ≈ a cotizar | Demanda de posadas validada |
| Software | Bot + panel + PWA ≈ a cotizar | Piloto operando manualmente con ≥ 15 clientes |

## 7. Aspectos clave de precio

- Referencias de comparación: costo de lavar fuera, costo de una lavadora nueva (USD 450 supuesto) y precio medio de la noche (USD 30–45 en Airbnb Tucacas). Si el lavado representa más de ~10 % de lo que el anfitrión gana por noche, hay resistencia; probar precio con 30 anfitriones.
- Estrategia de lanzamiento: **primer pase gratis** a los 10 primeros anfitriones a cambio de testimonio y datos.

## 8. Reproducibilidad (script usado)

```python
fleet=6; unit=450+20; capex=fleet*unit
op=200; maint=round(capex*0.03); soft=30; dep=round(capex/36)
cash_fixed=op+maint+soft
for name,cyc,price in [("conservador",25,3.0),("base",45,3.5),("optimista",70,4.0)]:
    rev=fleet*cyc*price; fee=rev*0.03
    cash=rev-cash_fixed-fee; net=cash-dep
    print(name, rev, round(fee), round(cash), round(net), round(capex/cash,1))
```
