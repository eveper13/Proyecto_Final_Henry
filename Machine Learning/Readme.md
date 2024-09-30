# Reviews Sentiment Analysis and Business Insights

## Descripción
Este proyecto tiene como objetivo analizar las reseñas de Yelp utilizando técnicas de **Procesamiento de Lenguaje Natural (NLP)**, **análisis de sentimientos** y **visualización de datos**. El objetivo es identificar las ciudades y negocios con más reseñas negativas. Además, se implementa un modelo de clasificación utilizando **Machine Learning** para predecir si una reseña será negativa en función de su longitud y otras características.

---

## Estructura del Proyecto

### 1. Carga y Exploración de Datos
- Se utiliza `pandas` para cargar y explorar el conjunto de datos de Yelp (`yelp_reviews.csv`), que contiene información sobre reseñas, negocios y ubicaciones.

### 2. Análisis de Sentimientos
- Utilizamos `SentimentIntensityAnalyzer` de **NLTK** para clasificar las reseñas en **positivas**, **negativas** o **neutras**.
- Creamos una columna adicional llamada `sentiment_label` para almacenar la etiqueta de sentimiento correspondiente a cada reseña.

### 3. Visualización de Reseñas Negativas
- Se generan gráficos que muestran las **10 ciudades con más reseñas negativas** y los **10 negocios más criticados**.
- También se implementa una función interactiva para explorar las reseñas negativas por ciudad.

### 4. Transformación de Textos
- Aplicamos la técnica de **TF-IDF** para vectorizar las reseñas negativas.
- Combinamos las **coordenadas geográficas** con las características textuales para realizar un análisis geoespacial más preciso.

### 5. Modelado con Machine Learning
- Utilizamos un **Random Forest Classifier** y técnicas de sobremuestreo (**SMOTE**) para entrenar un modelo que clasifique las reseñas como negativas o no.
- El rendimiento del modelo se evalúa mediante métricas como:
  - **F1-Score**
  - **Matriz de confusión**
  - **Curva ROC**
  - **Gráfico de Precisión vs Recuperación**

### 6. Mapa de Calor de Reseñas Negativas
- Generamos un **mapa de calor interactivo** con **folium** para visualizar las ubicaciones con mayor concentración de reseñas negativas.

---

## Requisitos

- **Python 3.8+**
- Bibliotecas necesarias:
  - `pandas`
  - `seaborn`
  - `matplotlib`
  - `nltk`
  - `scikit-learn`
  - `folium`
  - `scipy`

Para instalar todas las dependencias, ejecuta el siguiente comando:

```bash
pip install -r requirements.txt


Uso del Código
Descargar el dataset: Asegúrate de tener un archivo CSV llamado yelp_reviews.csv que contenga las reseñas, ubicaciones y nombres de los negocios.

Ejecutar el análisis de sentimientos:
yelp_reviews['sentiment_label'] = yelp_reviews['text'].apply(get_sentiment_label)

Visualizar las ciudades con más reseñas negativas:
show_negative_reviews_by_city('New York')

Entrenar el modelo de clasificación:
pipeline.fit(X_train, y_train)

Generar el mapa de calor:
m.save('heatmap.html')

Visualizaciones
Top 10 Ciudades con Más Reseñas Negativas:
![Top](./images/top.png)

Mapa de Calor de Reseñas Negativas:
![Mapa](./images/mapa.png)

Contribuciones
Este proyecto fue desarrollado para analizar patrones en las reseñas de Yelp y crear herramientas de visualización y predicción útiles para comprender mejor el comportamiento de los clientes en diferentes ciudades y negocios.

Enlaces de los Proyectos en Streamlit
Análisis de reviews Negativos: [Ver en Streamlit](https://modelo-reviews.streamlit.app) 
Caso de Éxito: Análisis de Sentimientos del Restaurant con Impresiones de Comida en 3D: [Ver en Streamlit](https://brunomperetti-analisis-melisse-app-ha9pyo.streamlit.app/) 