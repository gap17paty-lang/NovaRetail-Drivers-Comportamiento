# NovaRetail+: Explorando Drivers de Comportamiento Económico

## 📌 1. Introducción y Contexto del Negocio
En el entorno altamente competitivo del comercio electrónico, entender qué motiva el gasto de los usuarios es fundamental para diseñar estrategias de retención eficientes. Este proyecto analiza el comportamiento de millones de usuarios de la plataforma **NovaRetail+**, integrando variables demográficas, hábitos de navegación y rendimiento económico.

**El objetivo principal** es identificar qué factores o comportamientos están más fuertemente asociados con el ingreso anual generado por los clientes, permitiendo a la dirección tomar decisiones comerciales respaldadas por evidencia estadística sólida y evitar interpretaciones causales engañosas.

---
## 📂 2. Datasets Analizado 
* **Nombre: '/datasets/novaretail_comportamiento_clientes_2024.csv'**
---
## 📊 3 Exploración y Preparación de Datos

En esta fase, realicé un diagnóstico integral del conjunto de datos para garantizar su idoneidad antes del análisis exploratorio profundo:

* **Auditoría de Dimensiones:** Inspeccioné la estructura base de la información, validando el número total de registros y columnas disponibles.
* **Control de Calidad:** Verifiqué la integridad del dataset, confirmando la ausencia de valores nulos o faltantes en todas las variables.
* **Clasificación de Variables:** Identifiqué y segmenté los datos según su tipo en variables numéricas, binarias y categóricas.
* **Análisis Estadístico Inicial:** Apliqué estadística descriptiva sobre las variables numéricas para entender su distribución, tendencias centrales y dispersión inicial.

---

## 💡 4. Preguntas Clave del Negocio
* ¿Existe una relación real entre la edad o los niveles de ingresos declarados por el cliente con su nivel de gasto final?
* ¿Qué métricas de comportamiento dentro de la plataforma (clics, tiempo de navegación, recurrencia) son los verdaderos "drivers" del valor económico?
* ¿Cómo podemos segmentar eficazmente a la audiencia para optimizar las campañas de marketing sin desperdiciar recursos?

---

## 🛠️ 5. Tecnologías y Metodologías Estadísticas Utilizadas
Para este análisis de extremo a extremo en **Jupyter Notebook**, utilicé un flujo de trabajo híbrido con las siguientes librerías de **Python**: `Pandas`, `NumPy`, `Matplotlib` y `Seaborn`.

Debido a la diversidad en la naturaleza de los datos, apliqué diferentes metodologías analíticas y coeficientes estadísticos específicos:
* **Variables Numéricas Continuas:** Coeficientes de correlación de **Pearson** y **Spearman** para evaluar relaciones lineales y monótonas.
* **Variables Dicotómicas / Binarias:** Correlación **Punto Biserial** para medir el impacto de comportamientos específicos (ej. si cuenta con membresía activa o no) sobre el ingreso.
* **Variables Categóricas:** Coeficiente **V de Cramér** para evaluar asociaciones cualitativas mediante tablas de contingencia.
* **Visualización Avanzada:** Matrices de correlación (*Heatmaps*) y gráficos de dispersión (*Scatterplots*) automatizados.


---

## 📊 6. Hallazgos y recomendación de Negocio

El análisis se estructuró bajo la metodología estadística y de negocio **C+F+I** (Contexto/Correlación, Falsa Causalidad e Implicación):

### 1. El motor principal del ingreso anual
* **Evidencia:** *Scatter Plot* (`compras_mes` vs. `ingreso_anual`) | Correlación de Pearson: **0.97** (Muy fuerte).
* **Interpretación:** Existe una relación lineal positiva casi perfecta entre la frecuencia de compra mensual y el valor anual del cliente. El valor de vida del cliente escala de forma predecible según su recurrencia.
* **Falsa Causalidad:** No se puede asumir causalidad directa ni forzar la frecuencia; el ingreso anual es, por definición, el resultado acumulado de dichas transacciones.
* **Recomendación:** Las estrategias de fidelización y los incentivos de recompra a corto plazo (ej. cupones en el mismo mes) son la vía más directa para maximizar el *Customer Lifetime Value* (CLV).

### 2. Eficiencia de la inversión publicitaria y el embudo de conversión
* **Evidencia:** *Heatmap* global y *Pairplot* | Correlación de Pearson: **0.58** (`gasto_publicidad_dirigida` vs. `visitas_mes`).
* **Interpretación:** La publicidad dirigida tiene una asociación moderada-alta con la atracción de tráfico, demostrando efectividad en la captura de atención.
* **Falsa Causalidad:** El gasto publicitario no se traduce automáticamente en ventas directas, ya que la correlación con `ingreso_anual` desciende a **0.20**.
* **Recomendación:** La publicidad cumple su objetivo de generar tráfico, pero existe un cuello de botella en la conversión. Se recomienda que el equipo de Producto optimice la experiencia de usuario (UX) para transformar las visitas publicitarias en compras efectivas.

### 3. Independencia de factores demográficos (Segmentación Conductual)
* **Evidencia:** *Heatmap* global | Correlación de edad y `nivel_ingreso` con `ingreso_anual` cercana a **0.02** y **0.00**.
* **Interpretación:** Ausencia total de asociación lineal entre el perfil demográfico tradicional y el comportamiento de gasto. El valor del cliente está determinado por su interacción con la plataforma, no por sus atributos demográficos.
* **Falsa Causalidad:** Esto no descarta el valor de ciertos nichos, sino que demuestra que la edad o el ingreso por sí solos carecen de poder predictivo para NovaRetail+.
* **Impacto de Negocio:** El equipo de Marketing debe priorizar la **segmentación conductual** (clics, historial de navegación, compras previas) sobre la demográfica. Es más rentable pautar con base en "lo que el cliente hace" que en "quién es".

---

## ⚠️ Limitaciones y Próximos Pasos

### Limitaciones del Proyecto
1. **Correlación no implica causalidad:** El estudio identifica variables que se mueven juntas, pero no garantiza que alterar una variable (como forzar visitas) incremente los ingresos automáticamente.
2. **Temporalidad restringida:** Los datos se limitan exclusivamente al año 2024, omitiendo variables externas como la inflación, estacionalidad extendida o cambios competitivos del mercado.

### Próximos Pasos Recomendados
* **Análisis de Ticket Promedio:** Investigar la dispersión de ingresos en clientes con la misma frecuencia de compra mediante el análisis del valor y categoría de los productos seleccionados.
* **A/B Testing en el Funnel:** Diseñar experimentos controlados en el flujo de *"Visitas a Compras"* para optimizar la tasa de conversión del tráfico adquirido por publicidad.

---

## 📦 6. Estructura del Repositorio y Entregables
* `NovaRetail_Analisis_Drivers.ipynb`: Libreta principal en Jupyter Notebook con todo el código documentado, limpio y reproducible.
* `README.md`: Explicación del proyecto orientada al negocio.
