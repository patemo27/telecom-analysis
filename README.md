# Analítica de Consumo y Segmentación de Clientes - ConnectaTel

Este proyecto enfoca sus esfuerzos en auditar, limpiar y analizar el comportamiento de consumo de la base de usuarios de **ConnectaTel**. A través de un Análisis Exploratorio de Datos (EDA), identificamos patrones de uso en llamadas, minutos y mensajes, permitiendo segmentar de forma estratégica a los clientes según sus planes actuales (Básico o Premium) y detectar oportunidades comerciales de alto valor.

---

## 🎯 Objetivo del Proyecto
Optimizar la oferta comercial y la rentabilidad de ConnectaTel mediante la identificación de segmentos de comportamiento, análisis demográfico y detección de usuarios con consumos extremos (*Heavy Users*), traduciendo los hallazgos en recomendaciones de negocio accionables.

---

## 📊 Datasets Utilizados
El análisis se alimenta de dos conjuntos de datos principales unificados mediante el identificador único `user_id`:
* **`users`:** Contiene información de perfil de los clientes (edad, ciudad, plan contratado, fecha de registro).
* **`usage`:** Contiene el registro histórico de interacciones (cantidad de mensajes enviados, llamadas realizadas y volumen total de minutos consumidos).

---

## ⚙️ Etapas del Análisis
1.  **Auditoría y Limpieza de Datos:** Identificación y tratamiento de valores nulos estructurales (MAR) y consolidación de métricas de consumo en una tabla agregada.
2.  **Análisis Estadístico Descriptivo:** Obtención de medidas de tendencia central y dispersión para comprender los rangos y distribuciones de las variables.
3.  **Análisis de Distribución Visual:** Creación de histogramas con discriminación por plan (`hue='plan'`) para evaluar la asimetría y el comportamiento de las variables de consumo.
4.  **Detección de Valores Atípicos (Outliers):** Uso de diagramas de caja (`boxplots`) y aplicación del método analítico del Rango Intercuartílico (IQR) para delimitar el consumo de los usuarios extremos.
5.  **Interpretación Estratégica:** Traducción de métricas en propuestas de negocio (creación de planes nuevos y estrategias de upselling).

---

## 🚀 Cómo Ejecutar el Notebook

La opción más rápida y recomendada es ejecutar el análisis en la nube utilizando **Google Colab**:

1.  Descarga el archivo del notebook (`.ipynb`) desde este repositorio.
2.  Entra en [Google Colab](https://colab.research.google.com/).
3.  Selecciona la pestaña **Subir** (*Upload*) y carga el archivo del notebook.
4.  Sube los archivos correspondientes a los datasets (`users` y `usage`) en el almacenamiento temporal de la sesión (icono de carpeta en la barra lateral izquierda).

---

## 🔄 Guía de Reproducción

Para ejecutar el código de forma local o en tu propio entorno Jupyer:

1.  **Clonar el repositorio:**
    ```bash
    git clone [https://github.com/tu-usuario/connectatel-analysis.git](https://github.com/tu-usuario/connectatel-analysis.git)
    cd connectatel-analysis
    ```

2.  **Instalar las dependencias:** Asegúrate de tener instaladas las bibliotecas de análisis de datos requeridas:
    ```bash
    pip install pandas numpy matplotlib seaborn
    ```

3.  **Preparar los archivos:** Coloca los archivos de datos en la misma ruta donde se encuentra el notebook o actualiza los paths en la celda de lectura de datos (`pd.read_csv()`).

4.  **Ejecutar:** Inicia tu servidor de Jupyter o abre el archivo en tu editor favorito (como VS Code) y ejecuta las celdas secuencialmente de arriba hacia abajo para replicar los gráficos y cálculos del IQR.
