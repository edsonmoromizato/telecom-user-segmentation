# telecom-user-segmentation
Análisis estadístico, limpieza de datos y segmentación de clientes para la empresa de telecomunicaciones ConnectaTel. Desarrollado con Python y Pandas.

Este es un proyecto de análisis de datos para **ConnectaTel** (una empresa de telefonía), en el cual analizo cómo usan los clientes su servicio para ayudar a la empresa a entender qué tipo de usuarios tiene y doy recomendaciones de negocio en base a las conclusiones del análisis.

---

## ¿Cuál es el objetivo de este proyecto?
*   **Limpiar los datos:** Ver qué información falta (datos nulos), qué errores hay y cómo arreglarlos sin alterar los resultados.
*   **Conocer a los clientes:** Agruparlos según su edad y qué tanto usan el teléfono (si consumen poco, medio o mucho).
*   **Dar ideas de negocio:** Proponer mejoras para los planes **Básico** y **Premium** basadas en los datos reales.

---

## ¿Qué datos usé?
Trabajamos con dos tablas principales (archivos CSV):

1.  **`users` (Datos de las personas):**
    *   Contiene información básica como el nombre, edad, ciudad, el plan que tienen contratado (Básico/Premium) y si ya cancelaron el servicio o siguen activos.
2.  **`usage` (El uso del servicio):**
    *   Contiene el registro de cada llamada y mensaje que hacen los usuarios, incluyendo la duración de las llamadas y el largo de los mensajes de texto.

---

## Pasos que seguí en el análisis

1.  **Primer vistazo:** Revisé cuántas filas y columnas tenían las tablas y busqué datos vacíos (nulos).
2.  **Limpieza inteligente:** 
    *   Descubrí que los nulos en `churn_date` (fecha de cancelación) son normales: significa que el cliente sigue activo
    *   También vi que los mensajes no tienen "duración" y las llamadas no tienen "caracteres", lo cual explica otros datos vacíos normales en la tabla `usage`.
3.  **Crear grupos (Segmentación):** Usé código en Python para clasificar a los clientes automáticamente en grupos de edad y niveles de uso (Bajo uso, Uso medio, Alto uso).
4.  **Hacer gráficos:** Creé gráficos de barras (frecuencias) usando las librerías `Seaborn` y `Matplotlib` para ver visualmente dónde se concentra la mayoría de los usuarios.
5.  **Conclusiones:** Escribí recomendaciones para que el equipo de marketing sepa cómo mejorar los planes.

---

## Cómo ejecutar el notebook

1. Abre el notebook en Google Colab haciendo clic aquí: [Abrir en Colab](https://colab.research.google.com/github/edsonmoromizato/telecom-user-segmentation/blob/main/S7%20Version-Estudiante-Project-ConnectaTel.ipynb)
2. Ve a `Runtime → Run all` para ejecutar todas las celdas
3. Asegúrate de tener acceso a los archivos de datos

---

## Guía de reproducción

- **Lenguaje:** Python 3.x
- **Librerías necesarias:** pandas, matplotlib, seaborn
- **Datos:** Archivos `users.csv`, `usage.csv` y `plans.csv`
- **Pasos:**
  1. Clona este repositorio
  2. Abre el notebook en Colab o Jupyter
  3. Ejecuta las celdas en orden
