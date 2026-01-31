# Análisis de Datos de Ventas de Tiendas (Challenge Alura Latam)

## Índice

- [Descripción del Proyecto](#descripción-del-proyecto)
- [Fuentes de Datos](#fuentes-de-datos)
- [Análisis Realizado](#análisis-realizado)
  - [1. Preparación y Combinación de Datos](#1-preparación-y-combinación-de-datos)
  - [2. Análisis de Facturación (Ingresos Totales por Tienda)](#2-análisis-de-facturación-ingresos-totales-por-tienda)
  - [3. Ventas por Categoría](#3-ventas-por-categoría)
  - [4. Calificación Promedio de la Tienda](#4-calificación-promedio-de-la-tienda)
  - [5. Productos Más y Menos Vendidos](#5-productos-más-y-menos-vendidos)
  - [6. Envío Promedio por Tienda](#6-envío-promedio-por-tienda)
- [Visualizaciones Clave](#visualizaciones-clave)
- [Recomendación Estratégica para el Sr. Joao](#recomendación-estratégica-para-el-sr-joao)
- [Conclusiones](#conclusiones)
- [Cómo Ejecutar el Notebook](#cómo-ejecutar-el-notebook)

## Descripción del Proyecto

Este proyecto tiene como objetivo analizar los datos de ventas de cuatro tiendas diferentes para proporcionar una recomendación estratégica al Sr. Joao. El análisis abarca métricas clave como ingresos totales, categorías de productos más vendidas, calificación promedio de clientes, productos individuales más vendidos y costos de envío promedio por tienda. Los resultados se visualizan mediante gráficos y se consolidan en una recomendación final para optimizar el rendimiento del negocio.

## Fuentes de Datos

Los datos utilizados provienen de cuatro archivos CSV alojados en GitHub:

- Tienda 1: `https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_1%20.csv`
- Tienda 2: `https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_2.csv`
- Tienda 3: `https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_3.csv`
- Tienda 4: `https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_4.csv`

## Análisis Realizado

### 1. Preparación y Combinación de Datos

Se cargaron los datos de cada tienda en DataFrames individuales de `pandas`. Posteriormente, se añadió una columna `Tienda` a cada DataFrame para identificar la procedencia de los datos, y finalmente, se combinaron todos en un único DataFrame (`df_combined`) para facilitar el análisis global.

### 2. Análisis de Facturación (Ingresos Totales por Tienda)

Se calcularon los ingresos totales generados por cada tienda, sumando la columna `Precio` del DataFrame combinado. Esto permitió identificar las tiendas con mayor y menor desempeño en términos de ventas brutas.

- **Tienda 1:** 1.150.880.000
- **Tienda 2:** 1.116.344.000
- **Tienda 3:** 1.098.020.000
- **Tienda 4:** 1.038.376.000

La **Tienda 1** generó consistentemente los ingresos más altos.

### 3. Ventas por Categoría

Se identificaron las categorías de productos más vendidas tanto a nivel global como desglosado por cada tienda, contando la frecuencia de `Categoría del Producto`.

- **Top Categorías Globales:** Muebles, Electrónicos, Juguetes.
- Estas categorías también dominan las ventas a nivel de tienda.

### 4. Calificación Promedio de la Tienda

Se calculó la calificación promedio de los clientes (`Calificación`) para cada tienda, proporcionando una métrica de la satisfacción general.

- **Tienda 1:** 3.98
- **Tienda 2:** 4.04
- **Tienda 3:** 4.05
- **Tienda 4:** 4.00

La **Tienda 3** tuvo la calificación promedio más alta, mientras que la **Tienda 1** tuvo la más baja.

### 5. Productos Más y Menos Vendidos

Se determinaron los productos individuales más y menos vendidos contando la frecuencia de cada `Producto` en el DataFrame combinado.

- **Productos Más Vendidos:** 'Mesa de noche', 'Carrito de control remoto', 'Microondas', 'Batería', 'Cama king', 'Secadora de ropa', 'Modelado predictivo', 'Set de ollas', 'Cama box', 'Bloques de construcción'. Muchos pertenecen a las categorías de Muebles y Electrodomésticos.

### 6. Envío Promedio por Tienda

Se calculó el costo de envío promedio (`Costo de envío`) para cada tienda, lo cual es relevante para la rentabilidad.

- **Tienda 1:** 26.018,61
- **Tienda 2:** 25.216,24
- **Tienda 3:** 24.805,68
- **Tienda 4:** 23.459,46

La **Tienda 1** tuvo el costo de envío promedio más alto, y la **Tienda 4** el más bajo.

## Visualizaciones Clave

Se generaron los siguientes gráficos de barras para visualizar los resultados del análisis:

1.  **Ingresos Totales por Tienda:** Muestra la contribución de cada tienda a los ingresos generales, destacando a la Tienda 1 como líder.
2.  **Calificación Promedio por Tienda:** Ilustra la satisfacción del cliente en cada ubicación, señalando a la Tienda 3 con la mejor calificación.
3.  **Top 5 Categorías de Productos Más Vendidas:** Presenta las categorías con mayor volumen de ventas a nivel global, como Muebles, Electrónicos y Juguetes.

## Recomendación Estratégica para el Sr. Joao

Basándonos en el análisis exhaustivo de los datos, las siguientes recomendaciones son cruciales para optimizar el rendimiento de las tiendas del Sr. Joao:

1.  **Foco en la Tienda 1 y Tienda 2 para el Crecimiento de Ingresos:**
    La **Tienda 1** es claramente la líder en ingresos, seguida de cerca por la **Tienda 2**. Se recomienda invertir en marketing, expansión y optimización de estas tiendas para capitalizar su fuerte desempeño y capacidad para generar ventas.

2.  **Mejorar la Satisfacción del Cliente en la Tienda 1:**
    Aunque la Tienda 1 lidera en ingresos, su calificación promedio (3.98) es la más baja. Es fundamental investigar las causas de esta menor satisfacción (posibles problemas con tiempos de envío, calidad del producto o servicio al cliente) y aplicar mejoras para alinear su calificación con sus altos ingresos y con la de otras tiendas como la Tienda 3.

3.  **Optimización de Costos de Envío:**
    La **Tienda 1** presenta el costo de envío promedio más alto. Se sugiere revisar la logística y los proveedores de envío para identificar oportunidades de reducción de costos sin comprometer los tiempos de entrega. Podría ser beneficioso analizar y replicar las prácticas de la Tienda 4, que tiene los costos de envío más bajos.

4.  **Capitalizar las Categorías y Productos Estrella:**
    Las categorías de **Muebles**, **Electrónicos** y **Juguetes** son consistentemente las más vendidas. Se recomienda asegurar un stock adecuado y ofrecer promociones específicas en productos como 'Mesa de noche', 'Carrito de control remoto' y 'Microondas'. Un análisis más profundo de los márgenes de beneficio de estos productos podría guiar decisiones futuras de inventario y precios.

5.  **Analizar el éxito de la Tienda 3 en Calificación:**
    La **Tienda 3** tiene la calificación promedio más alta (4.05). Sería beneficioso analizar sus prácticas operacionales y de servicio al cliente para identificar qué la hace exitosa en este aspecto y aplicar estas mejores prácticas en las otras tiendas, especialmente en la Tienda 1.

En resumen, el Sr. Joao debería centrarse en consolidar el liderazgo en ventas de la Tienda 1 y 2, mejorar la experiencia del cliente en la Tienda 1 y optimizar los costos de envío. Al mismo tiempo, debe continuar potenciando las categorías de productos que demuestran ser los principales impulsores de ventas en todo el negocio.

## Conclusiones

El análisis de datos ha proporcionado una visión clara del rendimiento individual de cada tienda y de las tendencias generales del negocio. Las recomendaciones buscan un equilibrio entre el crecimiento de los ingresos, la satisfacción del cliente y la eficiencia operativa. Implementar estas estrategias permitirá al Sr. Joao tomar decisiones informadas para mejorar el rendimiento general de sus tiendas.

## Cómo Ejecutar el Notebook

1.  **Clonar el Repositorio:** Descarga o clona este repositorio de GitHub.
2.  **Abrir en Google Colab o Jupyter:** Puedes abrir el archivo `.ipynb` directamente en Google Colab (recomendado) o en un entorno local de Jupyter Notebook.
3.  **Instalar Dependencias:** Asegúrate de tener instaladas las bibliotecas necesarias (`pandas`, `matplotlib`, `seaborn`). Si usas Colab, estas suelen estar preinstaladas. Si no, puedes instalarlas con `pip install pandas matplotlib seaborn`.
4.  **Ejecutar Celdas:** Ejecuta todas las celdas del notebook en orden para reproducir el análisis y las visualizaciones.
