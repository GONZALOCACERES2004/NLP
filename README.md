# Informe de Análisis de Sentimientos en Reseñas

Debido a limitaciones de tiempo y recursos computacionales, nos vimos en la necesidad de trabajar con una muestra representativa de las reseñas disponibles. En este proceso, nos enfocamos principalmente en seleccionar reseñas con sentimientos claramente positivos o negativos, excluyendo aquellas de carácter neutral. Esta estrategia nos permitió optimizar el análisis y concentrarnos en los casos más relevantes para nuestro estudio de polaridad de opiniones.

Se realizó una exploración y preprocesamiento de los datos, en los casos necesarios, antes de aplicar los modelos de análisis de sentimientos.

## Modelos Evaluados

### Regresión Logística vs Random Forest

La Regresión Logística superó al Random Forest en todas las métricas:

- **Precisión:** 0.85 vs 0.81
- **Recall:** ~0.85 vs ~0.81
- **F1-score:** ~0.85 vs ~0.81

La matriz de confusión mostró menos errores de clasificación para la Regresión Logística, con un acuerdo del 89.61% entre las predicciones de ambos modelos.

### LSTM (Deep Learning)

El modelo LSTM alcanzó:

- **Accuracy:** 83%
- **Precisión y recall equilibrados para ambas clases:** 0.83

Se observó una mejora rápida en las primeras épocas, pero también un ligero sobreajuste a partir de la tercera época.

### Modelo "Dmyadav2001/Sentimental-Analysis"

Este modelo mostró el mejor rendimiento:

- **Accuracy global:** 92%
- **Precisión:** 0.91 (clase 0), 0.94 (clase 1)
- **Recall:** 0.94 (clase 0), 0.91 (clase 1)
- **F1-score:** 0.92 para ambas clases

## Conclusión

El modelo "Dmyadav2001/Sentimental-Analysis" se destaca como el mejor para el análisis de sentimientos en este estudio, con un rendimiento superior en todas las métricas evaluadas. Su alta precisión, recall equilibrado y F1-score consistente demuestran su eficacia en la clasificación de sentimientos positivos y negativos.

Para mejorar aún más los resultados, se recomienda:

1. Aumentar la regularización en modelos propensos al sobreajuste.
2. Ajustar hiperparámetros.
3. Implementar técnicas de aumento de datos.
4. Realizar un análisis detallado de errores para identificar patrones que los modelos podrían estar pasando por alto.
