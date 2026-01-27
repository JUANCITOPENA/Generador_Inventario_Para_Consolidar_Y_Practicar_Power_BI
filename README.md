# 📦 Proyecto de Simulación y Análisis de Inventarios

## 📌 Descripción General

Este proyecto consiste en la **generación, validación y análisis de datos de inventario** con una lógica **100% realista y auditable**, orientada a su uso en **Power BI, análisis BI, simulaciones empresariales y prácticas académicas**.

El dataset simula **entradas y salidas de inventario por fechas y meses completos**, garantizando coherencia matemática, continuidad del stock y una clasificación de estatus basada en métricas porcentuales previamente definidas.

---

## 🎯 Objetivos del Proyecto

* Simular movimientos reales de inventario (entradas y salidas)
* Garantizar que el **stock final siempre cuadre matemáticamente**
* Respetar **rangos de fechas con meses completos**
* Clasificar el inventario por estatus según reglas de negocio
* Cumplir una **distribución porcentual exacta de estatus**
* Facilitar análisis, KPIs e indicadores en Power BI

---

## 🧮 Lógica de Cálculo del Inventario

### Fórmula Base (Obligatoria)

```
Stock_Final = Stock_Inicial + Entradas - Salidas
```

### Reglas Clave

* El **Stock Inicial** de cada registro es el **Stock Final del registro anterior**
* No existen saltos ni reinicios artificiales
* Todas las entradas y salidas impactan directamente el stock
* El inventario negativo solo ocurre cuando las salidas superan las entradas

### Ejemplos

| Stock Inicial | Entradas | Salidas | Stock Final |
| ------------- | -------- | ------- | ----------- |
| 0             | 37       | 12      | 25          |
| 25            | 75       | 50      | 50          |
| 50            | 10       | 60      | -10         |

---

## 📅 Gestión de Fechas

* El sistema genera **todos los meses completos** dentro del rango definido
* No se omiten meses (ejemplo: abril no se pierde)
* Cada mes contiene múltiples registros
* Ideal para análisis temporales, comparativos y acumulados

---

## 🚦 Estatus de Inventario

Los estatus **NO son aleatorios**. Se asignan según el **Stock Final** y se ajustan para cumplir una métrica global predefinida.

### Estatus Definidos

| Estatus                | Descripción                    |
| ---------------------- | ------------------------------ |
| Inventario Excelente   | Alto nivel de stock disponible |
| Óptimo                 | Stock saludable y controlado   |
| Alerta Poco Inventario | Riesgo de quiebre de stock     |
| Inventario Negativo    | Salidas mayores que entradas   |

### 📊 Distribución Porcentual Global

| Estatus                | Porcentaje Objetivo |
| ---------------------- | ------------------- |
| Inventario Excelente   | **73%**             |
| Óptimo                 | **15%**             |
| Alerta Poco Inventario | **10%**             |
| Inventario Negativo    | **2%**              |

> El algoritmo ajusta entradas y salidas para que el stock final y el estatus **sean coherentes** y cumplan exactamente esta distribución.

---

## 🗂️ Estructura del Dataset

Las columnas **se mantienen intactas**, sin cambios de nombre.

Ejemplo típico:

* Fecha
* Mes
* Año
* Stock_Inicial
* Entradas
* Salidas
* Stock_Final
* Estatus_Inventario

---

## 📈 Casos de Uso

* Dashboards de Inventario en Power BI
* KPIs logísticos y operativos
* Simulación de escenarios empresariales
* Prácticas académicas de BI y análisis de datos
* Validación de modelos DAX

---

## 🔍 Beneficios del Modelo

* ✔ Datos realistas y consistentes
* ✔ Inventarios auditables
* ✔ Métricas confiables
* ✔ Análisis temporal sin errores
* ✔ Compatible con Power BI, Excel, SQL y Python

---

## 🚀 Recomendaciones para Power BI

* Crear medidas DAX basadas en `Stock_Final`
* Validar porcentajes de estatus con `COUNTROWS`
* Analizar tendencias mensuales y acumulados
* Usar segmentadores por mes, año y estatus

---

## 🧠 Conclusión

Este proyecto proporciona una **base sólida y profesional** para cualquier análisis de inventarios, eliminando errores comunes como stocks incoherentes, meses faltantes o estatus irreales. Es ideal para entornos reales, simulaciones y enseñanza de BI.

---

📌 *Proyecto diseñado para garantizar coherencia matemática, lógica de negocio y análisis confiable.*
