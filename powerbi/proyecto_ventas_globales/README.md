**Proyecto: Ventas Globales** 

Análisis completo del rendimiento de ventas a nivel global utilizando Power BI.

**1. Descripción del proyecto:** Este dashboard analiza el comportamiento de ventas por región, país, categoría y canal. Incluye un modelo de datos optimizado, KPIs clave y proyecciones usando DAX avanzado.

**2. Técnicas utilizadas**

**Modelado de datos**
- Relaciones 1:N y N:N
- Tablas auxiliares (Calendario, Regiones)
- Normalización y reducción de cardinalidad
- Creación de jerarquías (Región → País → Ciudad)

**DAX avanzado**
- Cálculos YTD, MTD, QTD
- Medidas con TIME INTELLIGENCE
- Funciones CALCULATE, FILTER, ALL, REMOVEFILTERS
- Rankings por ventas
- Medidas dinámicas con SELECTEDVALUE

**Ejemplo de una medida usada:**

```DAX
Ventas YTD = 
TOTALYTD(
    SUM(FactVentas[TotalVenta]),
    DimFecha[Fecha]
)
