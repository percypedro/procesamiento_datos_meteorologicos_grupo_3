# 🌦️ Clasificación y Procesamiento de Datos Climáticos  
**Proyecto Final — Grupo 3**  
**Materia:** Ciencia de Datos / Limpieza y Transformación de Datos  
**Periodo:** 2025  

**Participantes:**
- **Roberto Carlos Ascencio Andrade**  
- **Percy Pedro Fuentes Ramos**  
- **Karina Raquel Romero Flores**
- **Juan Marcos MIranda Nina**


## 📘 Descripción del Proyecto
Este proyecto tiene como objetivo realizar un **análisis y clasificación de datos meteorológicos** utilizando Python y Pandas.  
A partir de un archivo CSV proveniente de la API de Open-Meteo (almacenado en Google Drive), se desarrolló un flujo de trabajo completo que abarca las etapas **ETL (Extract, Transform, Load)** para generar un conjunto de datos limpio, clasificado y estructurado.

El análisis incluye:
- **Clasificación (taxonomía)** de temperatura, precipitación, velocidad del viento y presión atmosférica.  
- **Enriquecimiento temporal** con variables como año, mes, día, día de la semana, estación del año y momento del día.  
- **Evaluación de calidad de datos (Data Quality Report)**.  
- **Almacenamiento estructurado** en SQLite.  
- **Dashboard climático interactivo** con indicadores visuales para el departamento del Beni.

## 🧠 Objetivos
1. Aplicar buenas prácticas de procesamiento y limpieza de datos.  
2. Clasificar variables numéricas en categorías cualitativas (etiquetado o taxonomía simple).  
3. Crear nuevas variables derivadas del tiempo.  
4. Evaluar la calidad del dataset mediante un reporte automatizado.  
5. Almacenar los datos en un formato estructurado (SQLite / CSV).  
6. Visualizar los resultados en un **dashboard interactivo con Plotly**.

## ⚙️ Tecnologías Utilizadas
| Herramienta | Descripción |
|--------------|-------------|
| **Python 3.x** | Lenguaje principal de análisis |
| **Pandas** | Manipulación y transformación de datos |
| **NumPy** | Operaciones numéricas |
| **Matplotlib / Plotly** | Visualización y dashboards |
| **SQLite3** | Base de datos local para almacenamiento |
| **Google Colab / Jupyter Notebook** | Entorno de desarrollo |
| **YData-Profiling / Pandas Profiling** | Generación de reporte de calidad de datos |

## 🧩 Estructura del Código
| Sección | Descripción |
|----------|-------------|
| **1. Importación de librerías** | Carga de paquetes necesarios. |
| **2. Carga del dataset desde Google Drive** | Lectura del archivo CSV con Pandas. |
| **3. Clasificación de variables** | Aplicación de reglas definidas para: <br>– Temperatura (°C) <br>– Precipitación (mm) <br>– Viento (m/s, escala Beaufort) <br>– Presión atmosférica (hPa) |
| **4. Enriquecimiento temporal** | Generación de año, mes, día, día de la semana, estación y momento del día. |
| **5. Evaluación de calidad de datos** | Reporte de nulos, duplicados y cumplimiento de reglas. |
| **6. Almacenamiento estructurado (SQLite)** | Exportación a base de datos `data_set_3.db`. |
| **7. Dashboard climático** | Visualizaciones de temperatura, precipitación, viento, presión y acumulación mensual. |

## 🧮 Taxonomías aplicadas

**Temperatura (°C)**  
Muy fría < 0 • Fría 0–10 • Templada 10–20 • Cálida 20–30 • Calurosa > 30  

**Precipitación (mm)**  
Sin lluvia = 0 • Ligera 0–5 • Moderada 5–20 • Intensa 20–50 • Tormenta > 50  

**Viento (m/s)**  
Calma 0–0.2 • Brisa ligera 1.6–3.3 • Brisa moderada 5.5–7.9 • Fuerte 10.8–13.8 • Temporal/Huracán > 20.7  

**Presión (hPa)**  
Baja < 1000 • Normal 1000–1020 • Alta > 1020  

## 🗂️ Salidas del Proceso
- `clima_enriquecido.csv` — dataset final con variables clasificadas.  
- `data_set_3.db` — base de datos SQLite con tabla `clasificacion_proceso_datos`.  
- `informe_clima_1_hoja.xlsx` — hoja resumen con KPI y estadísticas.  
- `dashboard_climatico.html` — dashboard generado con Plotly.  

## 📊 Ejemplo de Resultados
**Dashboard Climático — Departamento del Beni**  
Muestra la distribución de categorías térmicas, tipos de precipitación, presión atmosférica, viento (escala Beaufort) y acumulado mensual de lluvias.

> Los resultados evidencian un predominio de **días cálidos**, **presión normal** y **precipitaciones ligeras a moderadas**, coherentes con el comportamiento climático de la región tropical del Beni.

## 🧾 Data Quality Report
Se generó un reporte automático de calidad que evalúa:
- Porcentaje de **nulos, duplicados y unicidad**.  
- **Cumplimiento de reglas** de rango y validez.  
- **Integridad global:** 99% de cumplimiento, con excepciones en las variables `snow` y `tsun` (fuera de rango por falta de datos).

## 🧑‍💻 Autores — Grupo 3
| Nombre | Rol | Contribución principal |
|---------|------|-----------------------|
| [Nombre 1] | Análisis y clasificación de variables | Taxonomías y transformación |
| [Nombre 2] | Limpieza y calidad de datos | Data Quality Report |
| [Nombre 3] | Base de datos y almacenamiento | Exportación SQLite |
| [Nombre 4] | Dashboard y visualización | Diseño de gráficos Plotly |
| [Nombre 5] | Redacción y documentación | Informe final y README |

## 🚀 Ejecución del Proyecto
```bash
# Clonar o abrir el notebook en Google Colab
!git clone https://github.com/percypedro/procesamiento_datos_meteorologicos_grupo_3.git

# Instalar dependencias necesarias
!pip install pandas numpy plotly ydata-profiling

# Ejecutar el notebook
# (o abrir directamente TRABAJO_FINAL_GRUPO_3.ipynb en Colab)
```

## 🧭 Conclusiones
El flujo implementado permitió construir un **pipeline reproducible** de análisis climático, garantizando:
- Alta calidad de los datos.
- Clasificaciones interpretables y consistentes.
- Resultados visuales claros y reutilizables en nuevos escenarios.

Este enfoque puede ampliarse para otros departamentos o regiones de Bolivia, incorporando más variables meteorológicas y análisis multitemporales.
