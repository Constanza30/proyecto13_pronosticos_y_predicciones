# 📊 Proyecto 13. Predicción de Churn y Segmentación de Clientes — Model Fitness

## 🧠 Descripción del proyecto
En el presente repositorio se analiza el abandono de clientes (churn) del gimnasio Model Fitness utilizando técnicas de análisis exploratorio, modelos de clasificación supervisada y clustering no supervisado.  
El objetivo es predecir la cancelación de clientes, segmentarlos según su comportamiento y proponer acciones estratégicas de retención basadas en datos.

---

## 🔍 Análisis exploratorio de datos
- Se construyó una matriz de correlación para identificar relaciones entre variables y el churn.
- Se detectaron variables clave con correlación negativa significativa con la cancelación:
  - `Lifetime`
  - `Age`
  - `Avg_class_frequency_current_month`
  - `Contract_period`
- Se identificaron variables altamente correlacionadas entre sí, lo que permitió interpretar dependencias internas y evitar conclusiones erróneas.

---

## 🤖 Modelos de Machine Learning
Se desarrollaron y compararon dos modelos de clasificación binaria para predecir la cancelación de clientes:

| Modelo | Accuracy | Precision | Recall |
|------|---------|-----------|--------|
| Regresión Logística | 0.91 | 0.82 | 0.80 |
| Random Forest | **0.92** | **0.84** | **0.82** |

- Ambos modelos muestran un alto desempeño predictivo.
- **Random Forest** fue seleccionado como el mejor modelo por su mayor capacidad de generalización.
- El uso de Recall fue clave para el negocio, ya que permite identificar clientes con alto riesgo de abandono y actuar preventivamente.

---

## 👥 Segmentación de clientes
- Se estandarizaron las variables y se aplicó clustering jerárquico para estimar el número óptimo de grupos.
- Se entrenó un modelo K-Means (k = 5) para segmentar a los clientes.
- Los clústeres presentan patrones de comportamiento claramente diferenciados y tasas de churn distintas:

| Clúster | Tasa de churn | Perfil general |
|-------|-------------|----------------|
| Clúster 2 | ~35% | Clientes nuevos, baja frecuencia y contratos cortos |
| Clúster 3 | ~4% | Clientes leales, alta frecuencia y mayor gasto |

---

## 📌 Principales hallazgos
- Los clientes con baja interacción temprana tienen mayor probabilidad de cancelar.
- La frecuencia de uso y el tiempo de permanencia son factores clave de retención.
- El factor social (entrenar con amigos o pareja) influye positivamente en la lealtad.
- El gasto en servicios adicionales es un fuerte indicador de compromiso con el gimnasio.

---

## 🎯 Recomendaciones basadas en datos
- Implementar estrategias de onboarding personalizado para clientes nuevos.
- Incentivar membresías grupales y programas de referidos.
- Diseñar beneficios exclusivos para clientes fieles, como descuentos o recompensas por antigüedad.
- Usar el modelo predictivo para detectar clientes en riesgo y activar campañas preventivas.

---

## 🚀 Impacto del proyecto
Este proyecto demuestra la aplicación práctica de machine learning para la toma de decisiones, permitiendo:
- Anticipar el abandono de clientes.
- Optimizar estrategias de marketing y retención.
- Transformar datos en acciones concretas de negocio.
  
---

## 🛠️ Tecnologías y habilidades aplicadas
- Python
- Análisis de datos: Pandas, NumPy
- Visualización: Matplotlib, Seaborn
- Machine Learning: Scikit-learn
- Modelado predictivo: Regresión Logística, Random Forest
- Clustering: K-Means, análisis jerárquico (dendrogramas)
- Evaluación de modelos: Accuracy, Precision, Recall
- Estandarización de variables y selección de features
