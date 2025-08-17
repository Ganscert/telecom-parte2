# 📌 TelecomX2: Predicción de Cancelación (Churn)

El objetivo es **desarrollar modelos predictivos** que permitan identificar a los clientes con mayor probabilidad de cancelar sus servicios.  

La empresa busca adelantarse al problema de la deserción y, en esta etapa inicial, corresponde construir un **pipeline sólido de modelado** que facilite dicha predicción.  

Además, se debe elaborar una **conclusión estratégica** que destaque los principales factores relacionados con la cancelación.  

---

## 🔍 Enfoque del Estudio

Para abordar este desafío se llevó a cabo un análisis exhaustivo de los distintos **métodos de evaluación y validación de modelos**, con el propósito de seleccionar aquel que ofrezca el mejor rendimiento en cuanto a la detección de patrones y tendencias en los datos.  

El conjunto de datos utilizado corresponde al archivo `datos_TelecomX_Fla.json` del **Challenge TelecomX1**, y dado que la variable objetivo es **Churn** (abandono del cliente), se trata de un **problema de clasificación binaria**.  

Los modelos aplicados incluyen:  

1. **Regresión Logística**  
2. **Árboles de Decisión**  
3. **K-Nearest Neighbors (KNN)**  
4. **Máquinas de Vectores de Soporte (SVM)**  
5. **Random Forest Classifier**  

---

## ⚙️ Métodos de Validación y Evaluación

1. Preparación y limpieza del dataset para los modelos predictivos.  
2. Análisis de correlación entre variables numéricas y Churn.  
3. Cálculo de métricas de exactitud (Accuracy).  
4. Validación de cada modelo.  
5. Construcción de matrices de confusión.  
6. Análisis de la curva ROC.  
7. Evaluación con curva Precisión-Recall.  
8. Elaboración de informes de métricas.  
9. Validación cruzada.  
10. Validación cruzada optimizada para sensibilidad (Recall).  
11. Uso de Stratified K-Fold para estratificación de datos.  
12. **Oversampling** para balanceo de clases.  
13. Implementación de pipelines de validación.  
14. **Undersampling** para balanceo alternativo.  
15. Optimización de hiperparámetros.  
16. Generación de insights finales basados en correlaciones con Churn.  

---

## 📈 Insights Finales sobre la Cancelación

### 🔺 Factores que **Incrementan** la Probabilidad de Cancelación
- **Altos cargos mensuales (`Charges.Monthly`)**: clientes con facturas más elevadas muestran mayor tendencia a cancelar.  
- **Facturación electrónica (`PaperlessBilling`)**: usuarios con este tipo de facturación registran un churn más alto, posiblemente por ser clientes más digitales y propensos a comparar proveedores.  
- **Adultos mayores (`SeniorCitizen`)**: muestran una ligera mayor propensión a cancelar, probablemente por factores económicos o menor afinidad tecnológica.  
- **Servicios de streaming (`StreamingTV`, `StreamingMovies`)**: su presencia no garantiza retención y podría estar vinculada con clientes más exigentes.  
- **Líneas múltiples (`MultipleLines`)**: no parecen influir en la retención y son fácilmente reemplazables por promociones externas.  

### 🔻 Factores que **Reducen** la Probabilidad de Cancelación
- **Antigüedad del cliente (`tenure`)**: mientras más tiempo con la empresa, menor riesgo de cancelación.  
- **Tipo de contrato (`Contract`)**: los contratos anuales o bianuales reducen significativamente el churn.  
- **Tipo de internet (`InternetService`)**: servicios de mayor calidad, como fibra, presentan menor tasa de abandono.  
- **Método de pago (`PaymentMethod`)**: clientes con débito automático cancelan menos.  
- **Gasto total (`Charges.Total`)**: clientes con mayor inversión en la empresa tienden a mantenerse.  
- **Servicios de valor agregado (`OnlineSecurity`, `TechSupport`)**: mejoran la experiencia y reducen la cancelación.  
- **Factores personales (`Partner`, `Dependents`)**: clientes con pareja o dependientes suelen ser más estables.  

---

## 🎯 Recomendaciones Estratégicas
- **Fidelizar a nuevos clientes** en sus primeros meses con beneficios personalizados.  
- **Promover contratos a largo plazo** con incentivos y promociones exclusivas.  
- **Incentivar métodos de pago automáticos** para reducir bajas por errores administrativos.  
- **Atender a clientes con altos cargos mensuales**, ofreciéndoles planes personalizados o descuentos.  
- **Ofrecer servicios de valor agregado** como soporte premium o seguridad online.  
- **Segmentar campañas de retención** según perfil de cliente (edad, digitalización, estado civil, etc.).  