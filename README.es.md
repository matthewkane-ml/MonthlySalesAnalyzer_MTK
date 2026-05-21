# Analizador de Ventas Mensuales

> Una herramienta de análisis de ventas en Python puro construida sobre un dataset de 20 días y 3 productos — implementando ocho funciones analíticas desde cero usando únicamente bucles, condicionales y estructuras de datos.

---

## Problema

Antes de recurrir a pandas o NumPy, un analista de datos necesita saber cómo extraer información directamente de estructuras nativas de Python. Este proyecto construye un pipeline completo de análisis de ventas usando solo Python puro — sin librerías externas — para responder las preguntas que cualquier stakeholder de negocio haría: qué producto lidera, qué día fue el pico, cuántos días superaron un umbral objetivo.

## Dataset

Una lista de 20 diccionarios, cada uno representando un día de ventas de tres productos:

```python
{"day": 1, "product_a": 202, "product_b": 142, "product_c": 164}
```

- 20 días × 3 productos (A, B, C)
- Sin archivo externo — los datos están definidos directamente en `monthly_sales_analyzer.py`

## Funciones Implementadas

| Función | Descripción |
|---|---|
| `total_sales_by_product(data, key)` | Suma todas las ventas diarias de un producto dado |
| `average_daily_sales(data, key)` | Media de ventas diarias de un producto dado |
| `best_selling_day(data)` | Día con las ventas combinadas más altas en todos los productos |
| `days_above_threshold(data, key, threshold)` | Cuenta los días en que las ventas de un producto superaron un umbral |
| `top_product(data)` | Cuál de A/B/C tuvo las ventas totales más altas en el período |
| `worst_selling_day(data)` *(bonus)* | Día con las ventas combinadas más bajas |
| `show_top_three(data)` *(bonus)* | Los 3 mejores días clasificados por ventas totales |
| `get_range(data, key)` *(bonus)* | Diferencia máximo − mínimo para un producto dado |

## Resultados

A lo largo del período de 20 días:

- **Producto líder:** Producto C — consistentemente el mayor volumen diario, con un total de ~5.300 unidades frente a ~3.750 de A y ~2.435 de B
- **Mejor día de ventas:** Día 12 (total combinado ~690 unidades: 287 + 64 + 339)
- **Días de Producto C por encima de 300:** 8 de 20 días

Las tres funciones bonus también fueron implementadas. `show_top_three` funciona llamando a `best_selling_day` de forma iterativa y eliminando el día encontrado de una copia de la lista — reutilizando la lógica existente de forma limpia sin duplicar código.

## Stack Tecnológico

`Python` · solo estructuras de datos nativas (listas, diccionarios, bucles, condicionales)

## Ejecutar Localmente

```bash
git clone https://github.com/matthewkane-ml/MonthlySalesAnalyzer_MTK.git
cd MonthlySalesAnalyzer_MTK
python monthly_sales_analyzer.py
```

Sin dependencias — Python puro.

## Próximos Pasos

- Refactorizar los bucles para usar funciones integradas de Python (`sum()`, `max()`, `min()`, comprensiones de listas) ahora que la lógica manual ya se entiende — el siguiente paso natural después de este ejercicio
- Cargar los datos desde un archivo CSV para que el analizador funcione con exportaciones reales de ventas de fin de mes
- Añadir una capa de visualización con Matplotlib para graficar los totales diarios y las tendencias por producto a lo largo del tiempo

---

**Autor:** Matthew Kane — [LinkedIn](https://www.linkedin.com/in/thomas-k-392094410/) · [Portafolio GitHub](https://github.com/matthewkane-ml)
