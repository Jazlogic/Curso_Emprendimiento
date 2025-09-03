# Clase 5: Inteligencia Artificial y Machine Learning

## Objetivos de la Clase

- Comprender los fundamentos de Machine Learning y sus aplicaciones empresariales
- Implementar modelos de ML para resolver problemas de negocio
- Dominar herramientas y frameworks de IA (TensorFlow, PyTorch, scikit-learn)
- Entender la ética en IA y cómo evitar sesgos algorítmicos

## Navegación del Módulo

| Clase | Tema | Duración | Tipo |
|-------|------|----------|------|
| 1 | Fundamentos de Transformación Digital | 2 horas | Teórica |
| 2 | Estrategias de Adopción Tecnológica | 2 horas | Teórica |
| 3 | Cloud Computing y Arquitecturas Escalables | 3 horas | Práctica |
| 4 | Desarrollo de APIs y Microservicios | 3 horas | Práctica |
| 5 | **Inteligencia Artificial y Machine Learning** | 3 horas | Práctica |
| 6 | Blockchain y Tecnologías Descentralizadas | 2 horas | Teórica |
| 7 | IoT y Conectividad Empresarial | 2 horas | Teórica |
| 8 | Ciberseguridad y Protección de Datos | 2 horas | Teórica |
| 9 | Gestión de Proyectos Tecnológicos | 2 horas | Teórica |
| 10 | Proyecto Integrador: Plataforma Digital | 4 horas | Práctica |

## Contenido Teórico

### 1. Fundamentos de Machine Learning

#### 1.1 ¿Qué es Machine Learning?
Machine Learning (ML) es un subcampo de la Inteligencia Artificial que permite a las máquinas aprender y mejorar automáticamente a partir de la experiencia, sin ser programadas explícitamente para cada tarea.

#### 1.2 Tipos de Machine Learning
- **Supervised Learning**: Aprendizaje supervisado con datos etiquetados
- **Unsupervised Learning**: Aprendizaje no supervisado sin etiquetas
- **Reinforcement Learning**: Aprendizaje por refuerzo basado en recompensas
- **Semi-supervised Learning**: Combinación de datos etiquetados y no etiquetados

#### 1.3 Algoritmos Comunes
- **Clasificación**: Random Forest, SVM, Naive Bayes
- **Regresión**: Linear Regression, Decision Trees, Neural Networks
- **Clustering**: K-Means, Hierarchical Clustering, DBSCAN
- **Dimensionality Reduction**: PCA, t-SNE, LDA

### 2. Aplicaciones de IA en el Negocio

#### 2.1 Marketing y Ventas
- **Personalización**: Recomendaciones personalizadas
- **Predicción de Churn**: Identificar clientes en riesgo
- **Optimización de Precios**: Precios dinámicos
- **Análisis de Sentimientos**: Opiniones de clientes

#### 2.2 Operaciones
- **Mantenimiento Predictivo**: Predecir fallas de equipos
- **Optimización de Inventario**: Gestión inteligente de stock
- **Logística**: Optimización de rutas y entregas
- **Calidad**: Detección de defectos en producción

#### 2.3 Recursos Humanos
- **Reclutamiento**: Screening de candidatos
- **Análisis de Performance**: Evaluación de empleados
- **Predicción de Rotación**: Identificar empleados en riesgo
- **Capacitación**: Personalización de entrenamientos

#### 2.4 Finanzas
- **Detección de Fraude**: Identificar transacciones fraudulentas
- **Scoring Crediticio**: Evaluación de riesgo crediticio
- **Trading Algorítmico**: Automatización de inversiones
- **Análisis de Riesgo**: Evaluación de riesgos financieros

### 3. Herramientas y Frameworks

#### 3.1 Python y Librerías
- **NumPy**: Computación numérica
- **Pandas**: Manipulación de datos
- **Matplotlib/Seaborn**: Visualización
- **Scikit-learn**: Machine Learning clásico
- **TensorFlow**: Deep Learning
- **PyTorch**: Deep Learning dinámico

#### 3.2 Plataformas Cloud
- **AWS**: SageMaker, Rekognition, Comprehend
- **Azure**: Machine Learning Studio, Cognitive Services
- **Google Cloud**: AI Platform, AutoML, Vision API
- **IBM**: Watson Studio, Watson Assistant

#### 3.3 Herramientas de MLOps
- **MLflow**: Gestión del ciclo de vida de ML
- **Kubeflow**: ML en Kubernetes
- **DVC**: Control de versiones para ML
- **Weights & Biases**: Experimentación y monitoreo

### 4. Proceso de Machine Learning

#### 4.1 Pipeline de ML
```
Datos → Preprocesamiento → Entrenamiento → Validación → Despliegue → Monitoreo
```

#### 4.2 Pasos Detallados
1. **Definición del Problema**: Objetivo claro y métricas
2. **Recopilación de Datos**: Fuentes y calidad
3. **Exploración de Datos**: EDA y visualización
4. **Preprocesamiento**: Limpieza y transformación
5. **Selección de Modelo**: Algoritmo apropiado
6. **Entrenamiento**: Ajuste de parámetros
7. **Validación**: Evaluación del rendimiento
8. **Despliegue**: Implementación en producción
9. **Monitoreo**: Seguimiento continuo

### 5. Ética en IA y Sesgos

#### 5.1 Tipos de Sesgos
- **Sesgo de Datos**: Datos no representativos
- **Sesgo de Algoritmo**: Algoritmos discriminatorios
- **Sesgo de Confirmación**: Buscar información que confirme creencias
- **Sesgo de Disponibilidad**: Sobreestimar información disponible

#### 5.2 Principios Éticos
- **Transparencia**: Explicabilidad de decisiones
- **Equidad**: Tratamiento justo e imparcial
- **Privacidad**: Protección de datos personales
- **Responsabilidad**: Responsabilidad por decisiones de IA

#### 5.3 Mitigación de Sesgos
- **Datos Diversos**: Inclusión de poblaciones diversas
- **Auditoría Regular**: Evaluación continua de sesgos
- **Algoritmos Justos**: Técnicas de fair ML
- **Diversidad en Equipos**: Equipos diversos de desarrollo

## Ejercicios Prácticos

### Ejercicio 1: Análisis Predictivo con Python
**Objetivo**: Crear un modelo de predicción de ventas

**Instrucciones**:
1. Carga y explora un dataset de ventas
2. Preprocesa los datos
3. Entrena un modelo de regresión
4. Evalúa el rendimiento del modelo

**Código de Ejemplo**:
```python
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score

# Cargar datos
df = pd.read_csv('sales_data.csv')

# Preprocesamiento
X = df[['price', 'advertising', 'competition']]
y = df['sales']

# División de datos
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

# Entrenamiento del modelo
model = LinearRegression()
model.fit(X_train, y_train)

# Predicciones
y_pred = model.predict(X_test)

# Evaluación
mse = mean_squared_error(y_test, y_pred)
r2 = r2_score(y_test, y_pred)

print(f'MSE: {mse}')
print(f'R²: {r2}')
```

### Ejercicio 2: Clasificación con Scikit-learn
**Objetivo**: Clasificar clientes según su probabilidad de churn

**Instrucciones**:
1. Carga datos de clientes
2. Preprocesa las variables categóricas
3. Entrena un modelo de clasificación
4. Evalúa con métricas de clasificación

**Código de Ejemplo**:
```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.preprocessing import LabelEncoder
from sklearn.metrics import classification_report, confusion_matrix

# Preprocesamiento de variables categóricas
le = LabelEncoder()
df['category_encoded'] = le.fit_transform(df['category'])

# Preparación de datos
X = df[['age', 'income', 'category_encoded', 'usage_frequency']]
y = df['churn']

# Entrenamiento
model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(X_train, y_train)

# Evaluación
y_pred = model.predict(X_test)
print(classification_report(y_test, y_pred))
print(confusion_matrix(y_test, y_pred))
```

### Ejercicio 3: Deep Learning con TensorFlow
**Objetivo**: Crear una red neuronal para reconocimiento de imágenes

**Instrucciones**:
1. Carga un dataset de imágenes
2. Preprocesa las imágenes
3. Construye una red neuronal convolucional
4. Entrena y evalúa el modelo

**Código de Ejemplo**:
```python
import tensorflow as tf
from tensorflow.keras import layers, models

# Construcción del modelo
model = models.Sequential([
    layers.Conv2D(32, (3, 3), activation='relu', input_shape=(32, 32, 3)),
    layers.MaxPooling2D((2, 2)),
    layers.Conv2D(64, (3, 3), activation='relu'),
    layers.MaxPooling2D((2, 2)),
    layers.Conv2D(64, (3, 3), activation='relu'),
    layers.Flatten(),
    layers.Dense(64, activation='relu'),
    layers.Dense(10, activation='softmax')
])

# Compilación
model.compile(optimizer='adam',
              loss='sparse_categorical_crossentropy',
              metrics=['accuracy'])

# Entrenamiento
model.fit(X_train, y_train, epochs=10, validation_data=(X_test, y_test))
```

## Conceptos Clave

- **Machine Learning**: Aprendizaje automático de patrones
- **Supervised Learning**: Aprendizaje con datos etiquetados
- **Unsupervised Learning**: Aprendizaje sin etiquetas
- **Deep Learning**: Redes neuronales profundas
- **MLOps**: Operaciones de Machine Learning
- **Ética en IA**: Principios éticos en inteligencia artificial

## Preguntas de Repaso

1. ¿Cuál es la diferencia entre Machine Learning y Deep Learning?
2. ¿Cómo se puede evitar el overfitting en modelos de ML?
3. ¿Qué métricas son apropiadas para evaluar modelos de clasificación?
4. ¿Por qué es importante la ética en IA?
5. ¿Cómo se puede implementar MLOps en una empresa?

## Próximos Pasos

1. **Practicar** con datasets reales
2. **Explorar** diferentes algoritmos de ML
3. **Implementar** un proyecto de ML completo
4. **Aprender** sobre MLOps y despliegue

## Recursos Adicionales

### Datasets para Práctica
- **Kaggle**: https://www.kaggle.com/datasets
- **UCI ML Repository**: https://archive.ics.uci.edu/
- **Google Dataset Search**: https://datasetsearch.research.google.com/
- **AWS Open Data**: https://registry.opendata.aws/

### Cursos Online
- **Coursera**: Machine Learning by Andrew Ng
- **edX**: MIT Introduction to Machine Learning
- **Udacity**: Machine Learning Engineer Nanodegree
- **Fast.ai**: Practical Deep Learning for Coders

### Herramientas y Plataformas
- **Jupyter Notebooks**: Entorno de desarrollo interactivo
- **Google Colab**: Notebooks en la nube
- **Kaggle Kernels**: Competencias y datasets
- **Weights & Biases**: Experimentación y monitoreo

### Libros Recomendados
- "Hands-On Machine Learning" - Aurélien Géron
- "The Elements of Statistical Learning" - Hastie, Tibshirani, Friedman
- "Deep Learning" - Ian Goodfellow, Yoshua Bengio, Aaron Courville
- "AI Ethics" - Mark Coeckelbergh

---

**¡Siguiente Clase!** 🚀
En la próxima clase aprenderás sobre **Blockchain y Tecnologías Descentralizadas** y su potencial en el mundo empresarial.
