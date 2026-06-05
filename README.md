# NovaRetail+: Explorando Drivers de Comportamiento Económico

## 📌 1. Introducción y Contexto del Negocio
En el entorno altamente competitivo del comercio electrónico, entender qué motiva el gasto de los usuarios es fundamental para diseñar estrategias de retención eficientes. Este proyecto analiza el comportamiento de millones de usuarios de la plataforma **NovaRetail+**, integrando variables demográficas, hábitos de navegación y rendimiento económico.

El objetivo principal es identificar qué factores o comportamientos están más fuertemente asociados con el ingreso anual generado por los clientes, permitiendo a la dirección tomar decisiones comerciales respaldadas por evidencia estadística sólida y evitar interpretaciones causales engañosas.

---

## 💡 2. Preguntas Clave del Negocio
* ¿Existe una relación real entre la edad o los niveles de ingresos declarados por el cliente con su nivel de gasto final?
* ¿Qué métricas de comportamiento dentro de la plataforma (clics, tiempo de navegación, recurrencia) son los verdaderos "drivers" del valor económico?
* ¿Cómo podemos segmentar eficazmente a la audiencia para optimizar las campañas de marketing sin desperdiciar recursos?

---

## 🛠️ 3. Tecnologías y Metodologías Estadísticas Utilizadas
Para este análisis de extremo a extremo en **Jupyter Notebook**, utilicé un flujo de trabajo híbrido con las siguientes librerías de **Python**: `Pandas`, `NumPy`, `Matplotlib` y `Seaborn`.

Debido a la diversidad en la naturaleza de los datos, apliqué diferentes metodologías analíticas y coeficientes estadísticos específicos:
* **Variables Numéricas Continuas:** Coeficientes de correlación de **Pearson** y **Spearman** para evaluar relaciones lineales y monótonas.
* **Variables Dicotómicas / Binarias:** Correlación **Punto Biserial** para medir el impacto de comportamientos específicos (ej. si cuenta con membresía activa o no) sobre el ingreso.
* **Variables Categóricas:** Coeficiente **V de Cramér** para evaluar asociaciones cualitativas mediante tablas de contingencia.
* **Visualización Avanzada:** Matrices de correlación (*Heatmaps*) y gráficos de dispersión (*Scatterplots*) automatizados.

---

## 📊 4. Hallazgos Principales e Impacto Operativo
* **Mito Desmentido:** Tras el análisis correlacional, se descubrió que los factores demográficos tradicionales (como la edad y el ingreso base del cliente) mostraron una **correlación cercana a cero** con el gasto real en la plataforma. Esto demostró que las campañas enfocadas únicamente en la edad no eran eficientes.
* **El Verdadero Driver:** Los comportamientos transaccionales internos y la frecuencia de interacción digital mostraron los coeficientes más altos de asociación con el valor económico total.
* **Enfoque en el Negocio:** Al identificar estas correlaciones reales, la dirección pudo reorientar su estrategia de segmentación, pasando de un enfoque demográfico tradicional a un modelo basado puramente en el comportamiento del usuario.

---

## 📦 5. Estructura del Repositorio y Entregables
* `NovaRetail_Analisis_Drivers.ipynb`: Libreta principal en Jupyter Notebook con todo el código documentado, limpio y reproducible.
* `README.md`: Explicación del proyecto orientada al negocio.
