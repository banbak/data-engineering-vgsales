🚀 Video Game Sales Data Analysis Project

![Python](https://img.shields.io/badge/Python-3.8-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-1.3.3-orange.svg)
![Numpy](https://img.shields.io/badge/Numpy-1.21.2-blue.svg)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.4.3-green.svg)
![SQL](https://img.shields.io/badge/SQL-SQLite-yellow.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)

Análisis de datos de ventas de videojuegos: Un proyecto que muestra mis habilidades como ingeniero de datos usando Python, SQL, Pandas, Numpy, Matplotlib, y más.

📄 Descripción del Proyecto
Este proyecto analiza un conjunto de datos de ventas de videojuegos (vgsales.csv), utilizando SQL para la manipulación y consultas de los datos, así como bibliotecas de Python como Pandas y Matplotlib para la visualización y análisis adicional. El objetivo principal es obtener información útil sobre las tendencias de ventas de videojuegos en diferentes plataformas, géneros y regiones.

📈 Tecnologías y Herramientas Utilizadas
SQL (SQLite): Consultas avanzadas y manipulación de datos.
Python: Procesamiento de datos.
Pandas: Manejo y limpieza de datos.
Numpy: Cálculos numéricos.
Matplotlib: Visualización de datos.
Jupyter Notebook: Desarrollo interactivo y presentación de resultados.

⚙️ Funcionalidades del Proyecto
Carga de datos desde archivo CSV a una base de datos SQL.
Análisis de datos con consultas SQL (incluyendo cálculos de porcentajes y agregados).
Visualización de tendencias de ventas a lo largo de los años.
Comparación de ventas por plataforma y género.
Obtención de estadísticas clave, como los juegos más vendidos y las regiones con mayores ventas.

🧑‍💻 Ejecución del Proyecto
Clona el repositorio:
git clone https://github.com/banbak/data-engineering-vgsales.git
cd data-engineering-vgsales

Abre el archivo VGames.ipynb en Jupyter Notebook:
jupyter notebook VideoGame_Sales_Analysis.ipynb

📊 Resultados Clave
Aquí se presentan algunos de los resultados más interesantes del análisis:

Plataformas con mayores ventas: Las plataformas PS2, X360, y PS3 dominan el mercado.
Géneros más populares: Los juegos de Acción y Deportes son los más vendidos.
Evolución de las ventas: Las ventas globales de videojuegos alcanzaron su punto más alto alrededor de 2010, con una tendencia a la baja en años recientes.

🔍 Consultas SQL Utilizadas
Algunas de las consultas SQL más importantes utilizadas en este proyecto incluyen:

Total de ventas globales por plataforma
SELECT Platform, COUNT(*) AS Num_Juegos, SUM(Global_Sales) AS Ventas_Globales
FROM ventas
GROUP BY Platform
ORDER BY Ventas_Globales DESC;

Porcentaje de ventas globales
WITH Total_Ventas AS (
    SELECT SUM(Global_Sales) AS Total_Global_Sales
    FROM ventas
)
SELECT Platform, 
       SUM(Global_Sales) AS Ventas_Globales, 
       PRINTF('%.2f', (SUM(Global_Sales) * 100.0 / (SELECT Total_Global_Sales FROM Total_Ventas))) AS Pct_Ventas_Globales
FROM ventas
GROUP BY Platform
ORDER BY Ventas_Globales DESC;

🏆 Conclusiones
Este proyecto demuestra mis competencias en el manejo de datos con SQL y Python, junto con mi habilidad para comunicar hallazgos mediante análisis visuales. Con el uso de Pandas, Numpy y Matplotlib, he sido capaz de transformar un conjunto de datos crudos en insights valiosos que podrían ser útiles para empresas de videojuegos o cualquier organización que trabaje con grandes volúmenes de datos.
