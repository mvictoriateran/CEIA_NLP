# Procesamiento de Lenguaje Natural (NLP) - Especialización en Inteligencia Artificial
Autora: María Victoria Terán Beiza

Este repositorio contiene una serie de trabajos prácticos realizados en el marco de la materia Procesamiento de Lenguaje Natural (NLP), parte de la Especialización en Inteligencia Artificial. Los desafíos abordados cubren una variedad de técnicas y herramientas de NLP, desde la clasificación de documentos y la medición de similitud entre textos hasta la construcción de modelos de lenguaje y chatbots. En cada uno de estos trabajos se aplicaron diferentes enfoques para resolver problemas relacionados con el análisis y la generación de texto.

A continuación, se presenta un resumen de cada uno de los trabajos realizados:

### Desafío 1: Clasificación y similitud entre documentos
Notebook: Desafio_1.ipynb

En este desafío se trabajó con el dataset fetch_20newsgroups de sklearn, que contiene documentos clasificados en 20 categorías diferentes. 

Los pasos realizados fueron:

Vectorización de documentos y evaluación de la similitud de documentos mediante la similitud del coseno.
Conclusión: Dependiendo del documento seleccionado, la similitud con otros documentos variaba. Esto se debe al vocabulario compartido entre distintas clases de documentos, lo que puede llevar a una similaridad errónea entre clases solo por la coincidencia de términos comunes.

Entrenamiento de modelos de clasificación Naive Bayes (MultinomialNB y ComplementNB), ajustando hiperparámetros para maximizar el F1-score macro.
Conclusión: La mejor métrica alcanzada (F1-score macro = 0.6980) se logró con el modelo ComplementNB (α = 0.5) y un TfidfVectorizer con el parámetro min_df = 2.

Transposición de la matriz documento-término y evaluación de la similitud entre palabras.
Conclusión: Las similitudes entre términos no siempre se basaron en sinónimos, sino en la coocurrencia dentro de los mismos documentos. Algunos términos mostraron similitudes con palabras afines, mientras otros mostraron similaridad con términos de un mismo contexto.

### Desafío 2: Vectores y similitudes con Gensim
Notebook: Desafio_2.ipynb

En este desafío se utilizaron los modelos Word2Vec de Gensim para entrenar word embeddings a partir del corpus de la novela Moby Dick de Herman Melville. Cada oración fue considerada un documento. 

Los pasos realizados fueron:

Entrenamiento de embeddings de palabras utilizando Word2Vec.
Visualización del espacio de embeddings en 2D y 3D.
Cálculo de similitudes entre palabras y planteamiento de analogías para evaluar las relaciones semánticas.

Conclusión: Las palabras similares no siempre fueron sinónimos, sino que estuvieron relacionadas en el contexto literario del texto. Además, las analogías confirmaron que el modelo logró capturar adecuadamente las relaciones semánticas entre palabras.

### Desafío 3: Modelo de lenguaje Many-to-Many
Notebook: Desafio_3_many_to_many_corregido.ipynb

En este trabajo se entrenó un modelo de lenguaje many-to-many utilizando LSTM, con el corpus de la novela Persuasion de Jane Austen, para predecir la siguiente palabra en una secuencia. Los pasos realizados fueron:

Tokenización del corpus y entrenamiento del modelo LSTM.
Evaluación de predicciones de una palabra adicional en secuencias.
Implementación de estrategias de beam search (determinístico y estocástico) para mejorar la generación de secuencias más largas.

Conclusión: El modelo predijo correctamente la siguiente palabra en secuencias cortas, pero mostró dificultades para mantener la coherencia en secuencias más largas. 

### Desafío 4: QA Bot
Notebook: Desafio_4.ipynb

En este desafío se construyó un chatbot para responder preguntas utilizando el dataset del challenge ConvAI2 (Conversational Intelligence Challenge 2) de conversaciones en inglés. El modelo se entrenó utilizando embeddings de FastText de dimensión 300 tanto para el encoder como el decoder. 

Los pasos realizados fueron:

Preprocesamiento de datos y tokenización de las preguntas y respuestas.
Entrenamiento de un modelo encoder-decoder con embeddings de FastText.
Evaluación del chatbot para generar respuestas coherentes y semánticamente correctas.

Conclusión: El chatbot generó respuestas variadas y coherentes, con un largo adecuado de salida. Aunque no todas las respuestas fueron exactas, todas mostraron sentido semántico. Además, el modelo aprendió a cerrar las oraciones correctamente, evitando respuestas sin finalización.
