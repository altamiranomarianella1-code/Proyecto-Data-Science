Resumen del Proyecto: 
Este proyecto analiza los determinantes estructurales e institucionales vinculados a la regularidad y el rendimiento academico de los estudiantes en las instituciones universitarias publicas de Argentina. A traves de tecnicas de Ciencia de Datos y Aprendizaje Automatico Supervisado, se modela y predice la tasa de retencion estudiantil. 

Origen de los Datos: 
Los datos fueron obtenidos de fuentes oficiales del Ministerio de Capital Humano / Secretaria de Educacion de la Nacion: 
Anuario Estadistico Universitario 2024 (el ultimo disponible con fecha mas reciente).
- Cuadro 1.2.2: Indicadores de Recursos Humanos (planta docente universitaria y dedicacion horaria).
- Programa Nacional de Becas Estrategicas Manuel Belgrano 2024.

Objetivo: 
El objetivo nuestro fue predecir si una universidad presenta una “Alta tasa de retencion/regularidad academica” (estudiantes reinscriptos con 2 o mas materias aprobadas) en funcion de variables estructurales: ratio alumno/docente, perfil de ingresantes, dedicacion horaria del cuerpo docente y tamaño institucional.

Hallazgos del Analisis Exploratorio (EDA): 
Escala VS. Rendimiento: El tamaño masivo de una institucion no garantiza por si solo mayor regularidad; existen universidades medianas con indices de aprobacion proporcionalmente superiores. 
Dedicación Docente: La proporcion de cargos docentes con dedicacion exclusiva presenta una relacion positiva con los niveles de retencion. 
Presencia de Outliers: Instituciones como la UBA presentan volúmenes de estudiantes atipicos respecto a la media del sistema, requiriendo metodos de escalado robustos. 

Modelos Evaluados y Optimizacion:
Preprocesamiento: Imputacion de faltantes por mediana y estandarización con StandardScaler integrado en un Pipeline de Scikit-Learn para evitar fuga de informacion.
Algoritmo Seleccionado: Ensamble “Random Forest Classifier”.
Control de Sobreajuste (Overfitting): Optimizacion de hiperparametros (`max_depth`, `n_estimators`, `min_samples_leaf`) mediante `GridSearchCV` sobre una validación cruzada estratificada de 5 pliegues (`StratifiedKFold`).





