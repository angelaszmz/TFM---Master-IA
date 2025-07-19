# TFM---Master-IA
Código de TFM de máster en Inteligencia Artificial

Este proyecto aplica técnicas de aprendizaje no supervisado (PCA + K-means) sobre datos clínicos y de imagen para identificar patrones fisiopatológicos compatibles con los fenotipos brain-first y body-first en pacientes con enfermedad de Parkinson.

Este proyecto utiliza Python 3.9+ y las siguientes librerías:
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- scipy

**Metodología**
**1. Análisis Exploratorio (EDA)**
- Revisión de distribuciones y valores atípicos

- Visualización de correlaciones y reducción de redundancia

- Categorización de variables por dominios fisiopatológicos

**2. PCA por dominios**
- Aplicación de Análisis de Componentes Principales por dominio clínico (motor, autonómico, cognitivo, etc.)

- Conservación de componentes que explican ≥80% de la varianza

- Visualización en 2D del espacio latente

**3. Clustering K-means**
- Clustering con k=2 (presuntos grupos brain-first vs body-first) en cada dominio

- Aplicación directa sobre datos estandarizados si el dominio tiene ≤3 variables

- Visualización: biplots, histogramas y gráficos de dispersión codificados por clúster

**4. Comparación cruzada y reglas heurísticas**
- Identificación de variables significativamente distintas entre clústeres

- Cálculo de umbrales clínicos (valor medio entre medias) para clasificación intuitiva

- Análisis cruzado para detectar correlatos clínicos entre dominios

**Objetivo**

El objetivo es avanzar hacia una clasificación fenotípica reproducible y clínicamente interpretable de los subtipos de Parkinson idiopático, integrando información autonómica, motora, cognitiva y de captación MIBG mediante técnicas estadísticas multivariantes y reglas heurísticas simples.

