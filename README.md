# 📊 Data Cleaning – Práctica Bootcamp (Pandas)
## 📁 Contenido del repositorio

En este repositorio se encuentra una práctica completa de limpieza y preparación de datos con Python y pandas realizada durante el Bootcamp.

### Archivos incluidos:

· README.md → documentación del proyecto

· dataset_gimnasio.csv → dataset original sin modificar

· ejercicio_limpieza_pandas_gimnasio.ipynb → notebook con el desarrollo paso a paso del proceso de limpieza y análisis de los datos

### 🎯 Objetivo de la práctica

El objetivo de esta práctica es aprender a limpiar y preparar un dataset real antes de analizarlo.

Durante el ejercicio se trabaja sobre un dataset de entrenamientos que contiene:

· Valores nulos

· Filas duplicadas

· Errores en los datos

· Formatos incorrectos

· Inconsistencias lógicas

La meta final es transformar el dataset original en un dataset limpio y coherente listo para análisis.

### 🧹 ¿Qué se ha trabajado?

En esta práctica se ha realizado un flujo completo de Data Cleaning:

1️⃣ Exploración inicial del dataset

Antes de modificar los datos se analiza la estructura del dataset:

· Número de filas y columnas

· Tipos de datos

· Valores nulos

· Estadísticas básicas

2️⃣ Detección y eliminación de duplicados

Se identificaron filas duplicadas dentro del dataset y posteriormente se eliminaron conservando únicamente la primera aparición.

También se reinició el índice del DataFrame para mantener una estructura ordenada.

3️⃣ Gestión de valores nulos

Se detectaron valores faltantes en distintas columnas.

Se aplicaron distintas estrategias:

· Cálculo de la media de calorías

· Redondeo a 1 decimal

· Sustitución de los valores nulos por esa media

También se eliminaron filas donde faltaban datos críticos (por ejemplo la fecha).

4️⃣ Limpieza y transformación de fechas

La columna de fechas contenía problemas de formato:

· Comillas innecesarias

· Formato de texto

Se realizaron las siguientes acciones:

· Eliminación de caracteres no deseados

· Conversión de la columna a formato datetime

Esto permite trabajar posteriormente con fechas de forma correcta.

5️⃣ Corrección de valores erróneos

Se detectaron valores inconsistentes en los datos:

· Una duración de entrenamiento de 450 minutos, que fue corregida a 45 minutos

Este tipo de errores suelen aparecer en datasets reales y deben validarse durante el proceso de limpieza.

6️⃣ Eliminación de errores lógicos

Se encontró un registro donde el pulso máximo era menor que el pulso normal, lo cual es un dato fisiológicamente imposible.

Esa fila fue eliminada filtrando únicamente los registros válidos.

7️⃣ Validación final del dataset

Una vez terminado el proceso de limpieza se verificó que el dataset:

· No contiene duplicados

· No contiene valores nulos relevantes

· Mantiene coherencia lógica en los datos

### 🧠 Comandos y funciones utilizadas

Durante la práctica se han utilizado principalmente herramientas de pandas para exploración y limpieza de datos.

· Exploración de datos

df.shape

df.dtypes

df.describe()

df.isnull().sum()
· Detección de duplicados

df.duplicated()

df[df.duplicated(keep=False)]

· Eliminación de duplicados

df.drop_duplicates()

df.reset_index()

· Gestión de valores nulos

df.isnull()

df.dropna()

df.fillna()

· Limpieza de texto

str.replace()

· Conversión de tipos de datos

pd.to_datetime()

· Filtrado de datos

df[df['columna'] > valor]

df[df['columna'] >= otra_columna]

· Operaciones estadísticas

mean()

sum()

idxmax()

## 📈 Análisis final realizado

Una vez limpio el dataset se realizaron algunos cálculos básicos:

🔥 Total de calorías quemadas

💓 Pulso medio durante los entrenamientos

🏅 Fecha en la que se quemaron más calorías

⏱️ Número de entrenamientos de exactamente 60 minutos

Esto demuestra cómo, una vez limpios los datos, es posible comenzar a extraer información útil.

## 💡 Aprendizajes clave

Esta práctica demuestra varios principios fundamentales del trabajo con datos:

· La limpieza de datos es una fase crítica del análisis

· Los datasets reales casi nunca vienen perfectos

· Los errores pueden ser de formato, duplicación o lógica

· Siempre se debe validar el dataset después de limpiarlo