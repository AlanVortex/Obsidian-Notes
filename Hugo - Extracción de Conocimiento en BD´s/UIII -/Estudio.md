  

# 📚 Notas de Estudio – Regresión, Clasificación y Métricas

Las metricas que usamos de clasificacion son:
Accuracy: 
Y otras 3 que son
Precisión
Recuerdo
F-Score

## 🔁 Regresiones
### ✅ ¿Qué es la regresión?

La regresión es una técnica de **aprendizaje supervisado** que se utiliza para **predecir valores numéricos continuos** en función de datos históricos.
### Tipos de regresión:

- **Regresión lineal simple**:  

  Tiene **una variable independiente (X)** y **una variable dependiente (Y)**.  

  Se representa mediante una **línea recta** ajustada a los datos.

- **Regresión lineal múltiple**:  

  Implica **una variable dependiente (Y)** y **múltiples variables independientes (X1, X2, ..., Xn)**.

- **Regresión polinomial**:  

  Utiliza un **modelo curvo** para ajustarse a los datos cuando la relación entre X y Y **no es lineal**.

- **Regresión lineal** (en general):  

  Se refiere a un modelo donde la **relación entre variables** sigue una tendencia **lineal**.

---
## 📌 Clasificación
### 🔎 KNN (K-Nearest Neighbors)

El algoritmo **KNN** se utiliza para **clasificación** (y en algunos casos, regresión). Su objetivo es **asignar una clase a un nuevo dato** basándose en la cercanía a otros datos ya clasificados.

---
## ⚖️ Escalamiento de Datos
  
Los algoritmos de machine learning son sensibles a las **magnitudes diferentes entre columnas**. Por ello, se aplica un **escalamiento o normalización**, especialmente cuando hay columnas con diferentes unidades o rangos.

> Por ejemplo: si una columna representa el **ingreso anual** y otra la **edad**, la magnitud del ingreso podría dominar al algoritmo, afectando negativamente los resultados.

---
## 📊 Métricas de Evaluación para Clasificación

### ✅ Accuracy (Precisión global)

- Mide el **porcentaje de predicciones correctas** sobre el total.
- Funciona bien cuando el dataset está **balanceado** (misma cantidad de registros por clase).  
---
### 📌 Métricas clave en clasificación binaria

| Métrica     | Fórmula                        | Significado |

|-------------|--------------------------------|-------------|

| **Precisión (Precision)** | `TP / (TP + FP)`         | Indica qué tan bien el modelo evita **falsos positivos**. Ejemplo: una prueba de embarazo predice que estás embarazada cuando no lo estás. |

| **Recuerdo (Recall / Sensitivity)** | `TP / (TP + FN)`         | Mide la capacidad del modelo para **detectar positivos reales**, evitando **falsos negativos**. |

| **F1 Score** | `2 * (Precision * Recall) / (Precision + Recall)` | Es la **media armónica** entre precisión y recuerdo. Útil cuando se busca un **balance entre ambos**. |

> 🔸 **F1 Score** es especialmente útil cuando el dataset **no está balanceado**.

---
## 📌 Consideraciones

- Usar **accuracy** cuando las clases están **balanceadas**.

- Cuando hay **desbalance** en las clases, es preferible usar **precision**, **recall** o **F1 Score**.

- Evitar métricas que puedan ser **engañosas** en conjuntos de datos desequilibrados.