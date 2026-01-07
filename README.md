# Efecto de la Edad Relativa en el Fútbol Profesional

![Distribución de meses de nacimiento](figures/birth_month_distribution.png)

## 📌 Descripción del proyecto

Este proyecto analiza el **Efecto de la Edad Relativa (Relative Age Effect, RAE)** en el fútbol profesional, explorando si los jugadores nacidos a comienzos del año calendario están sobrerrepresentados entre quienes logran llegar al nivel profesional.

A partir de un dataset amplio y real de futbolistas profesionales, el análisis muestra un **sesgo claro y estadísticamente significativo** a favor de los jugadores nacidos en los primeros meses del año —especialmente enero— en comparación con aquellos nacidos hacia fin de año.

---

## ❓ ¿Qué es el Efecto de la Edad Relativa?

En muchos sistemas de fútbol juvenil, las categorías se definen por año calendario. Como consecuencia, los jugadores nacidos a principios de año son relativamente mayores dentro de la misma categoría etaria.

Esta ventaja relativa suele traducirse en:
- Ventajas físicas y madurativas
- Mayor probabilidad de selección temprana
- Más acceso a entrenamientos y competencia de calidad

Con el tiempo, estas ventajas iniciales pueden acumularse e influir en qué jugadores terminan alcanzando el fútbol profesional.

---

## 📊 Dataset

- **Fuente**: Datos públicos de jugadores profesionales (scrapeados de Transfermarkt)
- **Alcance**: Global — jugadores profesionales de múltiples ligas y países
- **Variable clave**: `date_of_birth`

> ⚠️ Debido al tamaño de los archivos, los datasets crudos y procesados no se incluyen en el repositorio.  
> El análisis es completamente reproducible descargando los datos y ejecutando los notebooks.

Solo se incluyeron jugadores con fecha de nacimiento válida.

---

## 🛠️ Metodología

1. **Preparación de datos**
   - Conversión de fechas de nacimiento
   - Eliminación de valores faltantes o inválidos
   - Creación de variables derivadas:
     - `birth_month`
     - `birth_quarter`

2. **Análisis exploratorio**
   - Distribución de jugadores por mes de nacimiento
   - Identificación visual de sobrerrepresentación y subrepresentación

3. **Test estadístico**
   - Prueba de bondad de ajuste Chi-cuadrado
   - Hipótesis nula: distribución uniforme de meses de nacimiento

---

## 📈 Resultados principales

- Los jugadores nacidos en el **primer trimestre (Q1: enero–marzo)** están claramente sobrerrepresentados.
- Los nacidos en el **último trimestre (Q4: octubre–diciembre)** están subrepresentados.
- La prueba Chi-cuadrado **rechaza la hipótesis de distribución uniforme** (p < 0.05).

**Conclusión:**  
El mes de nacimiento tiene un impacto estadísticamente significativo en la probabilidad de llegar al fútbol profesional, confirmando la presencia de un fuerte Efecto de la Edad Relativa.

---

## 📂 Estructura del repositorio

```
data/
  raw/         # Datos originales (no incluidos por tamaño)
  processed/   # Datos procesados (no incluidos por tamaño)

notebooks/
  01_exploracion_y_limpieza.ipynb
  02_analisis_estadistico.ipynb

figures/
  birth_month_distribution.png
```

---

## 🚀 Cómo reproducir el análisis

1. Descargar el dataset desde su fuente pública
2. Colocar el archivo CSV en `data/raw/`
3. Instalar dependencias:

```bash
pip install -r requirements.txt
```

4. Ejecutar los notebooks en orden:
   - `01_exploracion_y_limpieza.ipynb`
   - `02_analisis_estadistico.ipynb`

---

## 🔮 Trabajo futuro

- Analizar el efecto por **país o región**
- Comparar por **posición de juego**
- Estudiar cohortes por década de nacimiento

---

## 👤 Autor

**Luciano Mosquén**  
Senior Data Analyst  
Python · SQL · Power BI

