# Análisis de Ventas, Clientes y Marketing con Python

Análisis exploratorio y estadístico de datos de ventas retail, orientado a identificar productos y categorías de alto rendimiento, y a generar recomendaciones estratégicas basadas en datos.

## Objetivo

A partir de tres fuentes de datos (ventas, clientes y campañas de marketing), el proyecto busca responder preguntas de negocio como:
- ¿Qué productos y categorías generan más ingresos?
- ¿Cómo se distribuyen las ventas? ¿Hay productos que se destacan por encima del resto?
- ¿Existe relación entre el precio de un producto y las unidades vendidas?
- ¿Qué recomendaciones estratégicas se pueden extraer del análisis?

## Datasets

Datos sintéticos generados para fines educativos, incluidos en la carpeta [`/data`](./data):

| Archivo | Filas | Descripción |
|---|---|---|
| `ventas.csv` | 3,035 | Ventas individuales: producto, precio, cantidad, fecha, categoría |
| `clientes.csv` | 567 | Datos demográficos de clientes: edad, ciudad, ingresos |
| `marketing.csv` | 90 | Campañas de marketing: producto, canal, costo, fechas |

## Proceso de análisis

El notebook [`analisis_ventas.ipynb`](./analisis_ventas.ipynb) sigue un flujo de trabajo típico de análisis de datos:

1. **Carga y exploración inicial (EDA)** — inspección de estructura, tipos de datos y primeras filas de cada dataset.
2. **Control de calidad de datos** — detección de valores nulos, duplicados exactos y duplicados por clave.
3. **Limpieza de datos** — eliminación de duplicados y normalización de campos (por ejemplo, precios almacenados como texto con símbolo `$`).
4. **Transformación** — cálculo de ingresos por venta (`precio × cantidad`) y construcción de una tabla de productos de alto rendimiento (top 20%).
5. **Agregación** — resumen de ventas por producto y por categoría.
6. **Integración** — combinación de los datasets de ventas y marketing para relacionar ingresos con inversión publicitaria.
7. **Estadística descriptiva** — media, mediana, moda, desviación estándar, rango intercuartílico (IQR) y detección de outliers.
8. **Análisis de correlación** — relación entre precio promedio y unidades vendidas por producto.
9. **Visualización** — gráficos con Matplotlib, Seaborn y dashboards interactivos con Plotly.

## Herramientas utilizadas

- **Python** (Google Colab)
- **Pandas** y **NumPy** — manipulación y análisis de datos
- **Matplotlib** y **Seaborn** — visualización estática
- **Plotly** — dashboards interactivos

## Principales hallazgos

- **Productos líderes:** Lámpara de Mesa ($82,276), Auriculares ($74,176) y Microondas ($72,563) concentran los mayores ingresos individuales.
- **Categorías destacadas:** Electrodomésticos ($505,300) y Electrónica ($482,578) son las de mayor facturación.
- **Distribución de ingresos:** la diferencia entre media ($48,903) y mediana ($48,140) es de solo 1.6%, lo que indica una distribución relativamente balanceada, sin una asimetría extrema.
- **Outliers:** se identificaron 4 productos "excepcionales" que en conjunto representan el 19.7% de los ingresos totales, un peso considerable para un grupo tan reducido.
- **Concentración:** el top 10 de productos concentra el 41% de los ingresos totales.

## Recomendaciones estratégicas

A partir del análisis, se proponen las siguientes líneas de acción:
- Potenciar los productos líderes replicando las estrategias que explican su éxito.
- Priorizar inversión en las categorías de mayor rendimiento (Electrodomésticos y Electrónica).
- Estudiar en detalle los factores detrás de los productos outlier para capitalizar ese desempeño en otros productos.
- Optimizar la inversión en marketing enfocándose en el retorno (ROI) por canal y producto.

## Cómo ejecutar este proyecto

```bash
git clone https://github.com/Miri-ai/analisis-ventas-marketing-python.git
cd analisis-ventas-marketing-python
pip install pandas numpy matplotlib seaborn plotly
```

Luego abrí `analisis_ventas.ipynb` en Jupyter Notebook, JupyterLab o Google Colab. Los datasets ya están incluidos en la carpeta `/data`, por lo que el notebook puede ejecutarse de principio a fin sin dependencias externas.

## Autora

**Miriam Sivira** — En transición de Contadora a Data Analyst.
Stack: Excel, SQL, Python, Power BI, Google Colab, Looker Studio, Tableau.

[GitHub](https://github.com/Miri-ai)
