# 📊 **VISUALIZACIÓN** 📊

_ _ _

## 🔍 **Introducción a la Visualización de Datos con Seaborn y Matplotlib** 🔍

### ¿Por qué es importante la visualización como analistas de datos?
La visualización es fundamental para los analistas de datos por varias razones:

1. **Comprensión de los datos:** 🧠  
   Las visualizaciones permiten explorar y comprender los datos de manera más intuitiva. Al representar los datos gráficamente, es más fácil identificar patrones, tendencias, relaciones y anomalías en los datos que pueden no ser evidentes en una tabla o conjunto de números.

2. **Identificación de insights:** 🔍  
   Las visualizaciones pueden revelar insights valiosos ocultos en los datos. Al representar los datos en diferentes formatos gráficos, es posible descubrir patrones, correlaciones o discrepancias que pueden conducir a nuevos conocimientos y oportunidades para el negocio.

3. **Detección de errores y valores atípicos:** 🚨  
   Las visualizaciones pueden ayudar a identificar errores en los datos o valores atípicos que pueden afectar los análisis. Al observar los gráficos, es más probable que se detecten discrepancias o valores inusuales que requieran una revisión adicional.

4. **Soporte para la toma de decisiones:** 📈  
   Las visualizaciones brindan una base sólida para la toma de decisiones fundamentada en datos. Al presentar información de manera visual, los analistas pueden respaldar sus argumentos con evidencia visual y facilitar la comprensión y aceptación de sus conclusiones por parte de los tomadores de decisiones.

5. **Comunicación efectiva:** 🗣️  
   Las visualizaciones ayudan a comunicar los resultados y hallazgos de análisis de datos de manera clara y concisa. Los gráficos y las visualizaciones permiten transmitir información compleja de una manera más accesible y comprensible para las partes interesadas, lo que facilita la toma de decisiones informadas.

_ _ _

### 📚 **Librerías para Visualizaciones en Python** 📚

En Python, existen varias librerías populares para realizar visualizaciones de datos. Algunas de las herramientas más comunes son:

- **Matplotlib:** 📉  
  Es una biblioteca de visualización ampliamente utilizada en Python. Proporciona una amplia gama de gráficos y permite un control detallado sobre los aspectos visuales. Matplotlib es altamente personalizable y se puede utilizar para crear gráficos simples y complejos. Es una base fundamental para otras bibliotecas de visualización.

- **Seaborn:** 🌈  
  Seaborn se basa en Matplotlib y proporciona una interfaz de alto nivel para crear gráficos estadísticos atractivos. Seaborn simplifica la creación de gráficos como histogramas, gráficos de dispersión, diagramas de caja y violín, y permite una fácil personalización. Seaborn también ofrece opciones para visualizar relaciones estadísticas complejas.

| **Característica**     | **Matplotlib**               | **Seaborn**                  |
|------------------------|------------------------------|------------------------------|
| Nivel de abstracción   | Bajo nivel                   | Alto nivel                   |
| Estilo y apariencia    | Requiere configuración detallada | Estilos prediseñados         |
| Tipos de gráficos      | Amplia variedad              | Enfoque en gráficos estadísticos |
| Integración con Pandas | Requiere manipulación de datos | Integración estrecha con Pandas |
| Interactividad         | Limitada                     | No proporciona directamente, pero puede combinarse con otras bibliotecas para agregar interactividad |

_ _ _

### **Tipos de Gráficas** 📈

#### **Análisis de Variables Numéricas**

| **Tipo de Gráfica** | **Método Seaborn** | **Método Matplotlib** | **Explicación**                                                 |
|---------------------|--------------------|-----------------------|-----------------------------------------------------------------|
| Histograma          | sns.histplot()     | plt.hist()            | Representa la distribución de una variable numérica.             |
| Diagrama de caja    | sns.boxplot()      | plt.boxplot()         | Muestra la distribución y valores atípicos de una variable numérica. |
| Violinplot          | sns.violinplot()   | -                     | Combina un diagrama de caja con una estimación de densidad.      |
| Gráfico de dispersión| sns.scatterplot() | plt.scatter()         | Muestra la relación entre dos variables numéricas.               |
| Gráfico de regresión| sns.regplot()      | -                     | Muestra una línea de regresión entre dos variables numéricas.    |
| Pairplot            | sns.pairplot()     | -                     | Muestra la relación entre múltiples variables numéricas.         |
| Heatmap             | sns.heatmap()      | plt.imshow()          | Visualiza la relación entre variables numéricas mediante colores. |

_ _ _

#### **Análisis de Variables Categóricas y Relación entre Variables Categóricas**

| **Tipo de Gráfica** | **Método Seaborn** | **Método Matplotlib** | **Explicación**                                              |
|---------------------|--------------------|-----------------------|--------------------------------------------------------------|
| Countplot           | sns.countplot()    | -                     | Muestra la frecuencia de cada categoría en una variable categórica mediante barras. |
| Pieplot             | -                  | plt.pie()             | Visualiza la proporción de cada categoría en una variable categórica mediante un gráfico circular. |

_ _ _

#### **Relación Variables Numéricas con Categóricas**

| **Tipo de Gráfica** | **Método Seaborn** | **Método Matplotlib** | **Explicación**                                              |
|---------------------|--------------------|-----------------------|--------------------------------------------------------------|
| Barplot             | sns.barplot()      | plt.bar()             | Muestra la relación entre una variable categórica y una variable numérica mediante barras. |
| Violinplot          | sns.violinplot()   | plt.violinplot()      | Muestra la distribución de una variable numérica para cada categoría en una variable categórica. |
| Boxplot             | sns.boxplot()      | plt.boxplot()         | Muestra la distribución de una variable numérica para cada categoría en una variable categórica. |
| Pointplot           | sns.pointplot()    | -                     | Muestra la relación entre una variable categórica y una variable numérica mediante puntos y líneas. |

_ _ _

### **¿Para qué utilizaremos Seaborn y Matplotlib en esta lección?**

1. **Seaborn para Visualizaciones Estilizadas:**  
   Aprenderemos a utilizar Seaborn para crear visualizaciones estilizadas y atractivas. Seaborn simplifica la creación de gráficos y proporciona una amplia variedad de paletas de colores y estilos para personalizar nuestras visualizaciones.

2. **Matplotlib para Personalización Avanzada:**  
   Exploraremos Matplotlib para un control total sobre la personalización de nuestros gráficos. Matplotlib nos permite ajustar cada detalle, desde tamaños de fuente hasta colores y estilos de línea.

_ _ _

### **¿Qué aprenderemos en esta lección?**

1. **Tipos de Gráficos:**  
   Exploraremos una variedad de tipos de gráficos, como gráficos de barras, gráficos de dispersión, gráficos de líneas, histogramas y más. Comprenderemos cuándo y cómo utilizar cada tipo de gráfico en función de los datos y los objetivos de visualización.

2. **Personalización de Gráficos:**  
   Aprenderemos a personalizar nuestros gráficos para que se adapten a nuestras necesidades, incluyendo la adición de etiquetas, títulos, leyendas y personalización de colores y estilos.

3. **Exploración de Datos:**  
   Utilizaremos visualizaciones para explorar datos y revelar patrones y tendencias ocultas. La visualización nos ayudará a obtener una comprensión más profunda de los datos antes de realizar análisis más avanzados.

4. **Comunicación Efectiva:**  
   Aprenderemos cómo diseñar visualizaciones que comuniquen de manera efectiva información a audiencias técnicas y no técnicas. La visualización es una herramienta poderosa para contar historias con datos.

_ _ _

## 📈 **Análisis de Variables Numéricas** 📈

Vamos a plantear algunas preguntas que nos van a ayudar a decidir qué tipo de gráfica podemos o debemos usar. Intentaremos contestar las siguientes preguntas:

1. **¿Cómo se distribuyen las edades de los individuos en el conjunto de datos?**  
   **Histograma de la variable "age":** Esta gráfica mostraría la distribución de las edades de los individuos en el DataFrame, lo que nos permitiría obtener información sobre la dispersión y la forma de la distribución.

2. **¿Existe alguna relación entre la edad y el número de días que han pasado desde el último contacto?**  
   **Gráfico de dispersión entre las variables "age" y "pdays":** Este gráfico nos permitiría explorar la relación entre la edad y el tiempo de contacto. Esto podría ayudarnos a identificar posibles patrones o correlaciones entre estas variables.

3. **¿Existen valores atípicos en la cantidad de contactos realizados durante la campaña publicitaria?**  
   **Boxplot de la variable "campaign":** Este gráfico nos ayudaría a identificar la distribución de la cantidad de contactos realizados durante la campaña publicitaria, así como a identificar posibles valores atípicos.

Estas son solo algunas de las preguntas que podríamos contestar, pero siéntete libre de probar con otras variables numéricas y ver cómo se verían sus gráficas para seguir aprendiendo.

_ _ _

### **Histograma o histplot** 📊

Es una representación gráfica de la distribución de una variable numérica. El histograma divide el rango de valores de la variable en intervalos llamados "bins" y muestra la frecuencia o conteo de observaciones que caen en cada bin. Esto permite visualizar la forma y la concentración de los datos en la variable, identificar patrones y detectar posibles valores atípicos.

- El eje x del histograma representa los valores de la variable numérica.
- El eje y muestra la frecuencia o densidad de los valores en cada bin.

Usaremos un histograma cuando deseemos representar la distribución de una variable numérica. Cuando se trabaja con datos numéricos, es importante comprender cómo se distribuyen los valores y qué patrones o tendencias pueden estar presentes en los datos.

Veamos cómo se hace esta visualización con Seaborn:

```python
sns.histplot(data, x="variable", bins=10, kde=False, color="blue")
```

- `data`: El DataFrame o la Serie que contiene los datos.
- `x`: La variable numérica (columna) que se desea representar en el eje x del histograma.
- `bins` (opcional): El número de intervalos (bins) en los que se dividirá el rango de valores. Puede ser un entero o una lista de valores para especificar los límites de los bins.
- `kde` (opcional): Un valor booleano que indica si se desea trazar una estimación de la densidad kernel junto con el histograma (por defecto es False).
- `color` (opcional): El color que se utilizará para el histograma (por defecto es "blue").

_ _ _

### **Gráfico de dispersión o scatterplot** 📈

Un gráfico de dispersión, también conocido como diagrama de dispersión o gráfico XY, se utiliza para mostrar la relación y la distribución de los datos entre las dos variables. Cada punto en el gráfico representa un par de valores correspondientes a las dos variables consideradas. La posición de cada punto en el gráfico indica el valor de ambas variables para ese punto de datos específico.

Usaremos este tipo de gráfica para identificar patrones, tendencias o correlaciones entre las dos variables. Puede ayudar a responder preguntas como: ¿existe una relación lineal entre las variables? ¿Hay una relación positiva o negativa? ¿Existen valores atípicos o puntos que se desvíen de la tendencia general?

De nuevo, usando la librería de Seaborn, su sintaxis básica es:

```python
sns.scatterplot(x, y, data, hue, style, size)
```

Explicación de los parámetros principales:

- `x` y `y`: Las variables numéricas que se utilizarán para el eje x e y respectivamente.
- `data`: El DataFrame que contiene los datos.
- `hue` (opcional): Permite agregar una tercera dimensión a través de colores diferentes para diferentes categorías.
- `markers` (opcional): Permite cambiar los puntos por otro tipo de marcador en la gráfica. Algunos de los markers que podemos usar son:
  - `'.'` Punto
  - `'*'` Estrella
  - `'+'` Cruz
  - `'x'` Cruz diagonal
- `size` (opcional): Permite asignar diferentes tamaños a los puntos de datos según una variable categórica.
- `color` (opcional): Nos permite cambiar el color de los puntos de la gráfica.

_ _ _

### **Gráfico de regresión o regplot** 📉

Es una gráfica que se utiliza para trazar un gráfico de dispersión (scatter plot) junto con una línea de regresión lineal que se ajusta a los datos. Esta línea de regresión lineal muestra la tendencia general de la relación entre dos variables y puede ayudar a identificar patrones o tendencias en los datos.

Al igual que el scatter plot, usaremos este tipo de gráfica cuando queramos explorar la relación entre dos variables numéricas y, al mismo tiempo, ver cómo se ajusta una línea de regresión lineal a esos datos. Es útil para identificar la dirección y la fuerza de la relación entre las variables, y para evaluar si existe una correlación lineal entre ellas.

Su sintaxis básica es:

```python
sns.regplot(x, y, data, markers)
```

- `x`: Especifica el nombre de la columna que se colocará en el eje x (horizontal).
- `y`: Indica el nombre de la columna que se colocará en el eje y (vertical).
- `data`: Es el DataFrame que contiene tus datos.
- `markers` (opcional): Permite cambiar los puntos por otro tipo de marcador en la gráfica. Podremos usar los mismos que en el scatterplot.
- `color` (opcional): Nos permite cambiar el color de los puntos de la gráfica.

📌 **NOTA:** Para este tipo de gráfico no tenemos método en Matplotlib.

_ _ _

### **Gráfico de cajas o boxplot y violinplot** 📦🎻

Ambos son una representación gráfica que muestra la distribución de un conjunto de datos numéricos a través de cuartiles. Estos tipos de gráficos proporcionan información sobre la mediana, los cuartiles (Q1 y Q3) y los valores atípicos de un conjunto de datos.

Antes de seguir viendo cómo construir las gráficas, contestemos a la pregunta de ¿Qué son los valores atípicos u outliers?

**Valores atípicos (outliers):** Son observaciones que se encuentran muy alejadas del resto de los datos en un conjunto de datos o una muestra estadística. Estas observaciones son consideradas anormales o extremas en comparación con el resto de los datos.

Es importante identificar los outliers por varias razones:

1. **Impacto en el análisis estadístico:** Pueden tener un impacto significativo en los resultados de un análisis estadístico. Pueden afectar la media, la desviación estándar y otros estadísticos descriptivos, lo que puede llevar a conclusiones erróneas o sesgadas. Identificar y tratar los outliers adecuadamente permite obtener resultados más precisos y confiables.

2. **Detección de errores o problemas:** Pueden indicar errores en la recopilación o entrada de datos. También pueden señalar problemas en el proceso de medición o en la calidad de los datos. Al identificar y examinar los outliers, es posible detectar y corregir errores, así como identificar áreas problemáticas que requieren atención.

3. **Identificación de casos especiales:** Pueden representar casos especiales o excepcionales que son de interés particular. Estos casos pueden contener información valiosa o representar situaciones únicas que requieren un análisis o tratamiento especial. Identificar y comprender estos outliers puede proporcionar información adicional y perspectivas importantes.

En resumen, identificar y tratar los outliers es importante para garantizar la precisión y confiabilidad de los análisis estadísticos, detectar errores o problemas en los datos, preservar la validez de los modelos y comprender casos especiales o excepcionales en los datos. Si bien hablaremos de ellos más adelante en las lecciones de estadística, hemos hecho una primera introducción a ellos para ir familiarizándonos con estos conceptos.

Como ya hemos aprendido los subplots, haremos las gráficas de Seaborn y de Matplotlib a la vez en una misma figura.

#### **Boxplot** 📦

Un boxplot es una representación gráfica que proporciona información sobre la distribución de un conjunto de datos numéricos. Se utiliza para resumir y visualizar la dispersión y la tendencia central de los datos, así como para detectar la presencia de valores atípicos (outliers). Un boxplot es especialmente útil cuando tienes datos en diferentes categorías o grupos y deseas comparar sus distribuciones.

La representación gráfica de un boxplot consiste en un rectángulo (la caja) que abarca desde el primer cuartil (Q1) hasta el tercer cuartil (Q3). Dentro de la caja, se traza una línea que representa la mediana. Además, se dibujan líneas verticales u horizontales (los bigotes) que se extienden desde la caja hasta los valores mínimo y máximo que no se consideran atípicos. Los valores atípicos se representan como puntos individuales más allá de los bigotes.

Características de un boxplot:

- La caja central representa el rango intercuartílico (IQR), que abarca desde el primer cuartil (Q1) hasta el tercer cuartil (Q3).
- La línea dentro de la caja es la mediana (Q2).
- Los "bigotes" se extienden desde la caja hasta los valores más extremos dentro de un rango determinado (por defecto, 1.5 veces el IQR).
- Los valores fuera de los bigotes se consideran valores atípicos (outliers).

📦 Un boxplot proporciona una forma rápida y efectiva de resumir la distribución y la dispersión de tus datos en una sola figura, además de facilitar la identificación de valores atípicos en los datos.

La sintaxis de un boxplot en Seaborn es:

```python
sns.boxplot(x, y, data, hue, width, palette, color)
```

- `x`: Nombre de la columna que queremos poner en el eje x (horizontal). Por lo general, esta columna contiene categorías o grupos que deseas comparar. Esto solo lo usaremos si queremos establecer la relación entre una variable numérica y una categórica, veremos un ejemplo más adelante en la lección.
- `y`: Nombre de la columna que tiene los valores numéricos que queremos representar en el eje y (vertical). Estos valores se utilizarán para construir los boxplots y mostrar cómo se distribuyen los datos.
- `data`: DataFrame que contiene tus datos.
- `hue`: Permite agregar una dimensión adicional de agrupación y colorea los boxplots según la categoría especificada. Esto solo lo usaremos cuando queramos establecer la relación entre variable categórica y numérica, que veremos más adelante.
- `width`: Define el ancho relativo de los boxplots.
- `color`: El color que queremos en el boxplot. Este parámetro lo usaremos cuando estemos analizando solo UNA variable numérica.
- `palette`: La paleta de colores que queremos en nuestra gráfica. Usaremos este parámetro cuando estemos analizando la relación entre una variable numérica y una categórica. Veremos un ejemplo un poco más adelante en la lección.

La sintaxis de un boxplot en Matplotlib es:

```python
plt.boxplot(data['variable'], widths=0.7, patch_artist=True, boxprops=dict(facecolor='blue'))
```

- `data['variable']`: La columna con los datos numéricos a representar.
- `widths`: Ancho relativo de las cajas en los boxplots.
- `patch_artist`: Si se establece en True, permite llenar las cajas con color.
- `boxprops`: Para cambiar el color de la caja, entre otros atributos.

_ _ _

### **Violinplot** 🎻

La representación gráfica de un violin plot es una forma de visualizar la distribución de datos numéricos en diferentes categorías o grupos. Este tipo de gráfico combina un boxplot y un gráfico de densidad, proporcionando una visión más completa de la distribución y variabilidad de los datos. Los violin plots son especialmente útiles cuando deseas comparar distribuciones entre diferentes categorías y explorar la forma y simetría de los datos.

**Características de un violin plot:**

- **Violines:** Los "violines" en un violin plot se asemejan a dos espejos reflejados a lo largo del eje y. Cada violin representa la distribución de datos dentro de una categoría. La parte más ancha del violin indica una mayor densidad de datos, y las partes más delgadas indican áreas de menor densidad.
- **Cajas y bigotes:** Al igual que en un boxplot, un violin plot a menudo incluye una caja y bigotes en el medio de cada violin. Estos elementos representan el rango intercuartílico (IQR) y los valores atípicos de los datos.
- **Puntos y valores atípicos:** Los puntos individuales y valores atípicos se pueden mostrar en los violines para resaltar valores individuales.

**Ventajas del violin plot frente a un boxplot:**

- Muestra la distribución completa de los datos, incluyendo la densidad y la forma.
- Proporciona una comprensión más rica de la variabilidad y la forma de las distribuciones.
- Permite la comparación directa de distribuciones entre categorías.

Su sintaxis básica en Seaborn es:

```python
sns.violinplot(x, y, data, color, palette, linewidth)
```

- `x`: Aquí se coloca el nombre de la columna que quieres poner en el eje horizontal (eje x). Esta columna debe tener datos categóricos, como diferentes categorías o etiquetas. Lo utilizaremos cuando queramos establecer la relación entre una variable numérica y una categórica.
- `y`: Coloca el nombre de la columna que tiene los valores numéricos que deseas representar en el eje vertical (eje y). Estos valores se usarán para construir los violines que mostrarán cómo se distribuyen los datos.
- `data`: Aquí pones el nombre del DataFrame que contiene tus datos. Asegúrate de haber cargado o creado este DataFrame antes de usarlo en el violin plot.
- `color`: El color que queremos en el violinplot. Este parámetro lo usaremos cuando estemos analizando solo UNA variable numérica.
- `palette`: La paleta de colores que queremos en nuestra gráfica. Usaremos este parámetro cuando estemos analizando la relación entre una variable numérica y una categórica. Veremos un ejemplo un poco más adelante en la lección.
- `linewidth`: Lo usaremos cuando queramos cambiar el grosor de la línea del violín.
- `width`: Define el ancho relativo de los boxplots.

_ _ _

## 📊 **Análisis de Variables Categóricas** 📊

### **Countplot**

Es una visualización específica que se utiliza para mostrar la frecuencia de observaciones en diferentes categorías. Este tipo de gráfico es especialmente útil cuando deseas contar y comparar cuántas veces aparece cada categoría en una variable categórica.

La sintaxis del countplot de Seaborn es bastante sencilla. Aquí tienes la estructura básica:

```python
sns.countplot(x='variable', data=df, palette='Set2', color='blue', hue='otra_variable')
```

- `x`: Es el nombre de la columna que contiene las categorías que deseas contar.
- `data`: Es el DataFrame o conjunto de datos con el que estamos trabajando.
- `palette` (opcional): Es un argumento que te permite especificar la paleta de colores a utilizar en el gráfico.
- `color` (opcional): Indicamos de qué color queremos que sean las barras.
- `hue` (opcional): Permite agregar otra variable categórica para diferenciar aún más las barras.
- `order` y `hue_order` (opcional): Te permiten definir el orden en el que se muestran las categorías en el eje X.
- `orient` (opcional): Puedes cambiar la orientación de las barras (horizontal o vertical).

_ _ _

### **Pieplot o Gráfico de Quesitos** 🥧

Es un tipo de gráfico utilizado para mostrar la proporción de diferentes partes en relación con un todo. Se representa como un círculo dividido en sectores, donde cada sector representa una categoría y su tamaño angular está en proporción a la cantidad que representa dentro del conjunto total. Los pie charts son útiles cuando deseamos visualizar cómo las partes contribuyen al total, especialmente cuando las partes son fácilmente distinguibles y la cantidad de categorías no es demasiado grande.

Sintaxis básica de un pie chart utilizando la librería Matplotlib (en Seaborn no tenemos este tipo de gráfico):

```python
plt.pie(valores, labels=etiquetas, autopct='%1.1f%%', startangle=90, colors=colores)
```

- `etiquetas`: Es la columna que contiene las etiquetas de cada sector del gráfico.
- `valores`: Es la columna que contiene los valores numéricos de cada sector.
- `autopct` (opcional): Agrega los porcentajes en cada sector con un formato específico.
- `startangle` (opcional): Controla el ángulo desde donde comienza el primer sector.
- `data`: El DataFrame del que provienen los datos.
- `colors` (opcional): Debe ser una lista con los colores que le queremos dar a cada una de las categorías.
- `textprops` (opcional): Debe ser un diccionario, nos permite cambiar el tamaño y tipo de la letra.

📌 **NOTA IMPORTANTE I:** Este tipo de gráfica nunca la podremos usar para evaluar la relación entre dos variables categóricas.

📌 **NOTA IMPORTANTE II:** Este tipo de gráfico raramente se podrá hacer desde el DataFrame original y tendremos que hacer una serie de cálculos. En concreto para realizar este tipo de gráfico necesitaremos dos columnas:

- Una columna donde tengamos los valores únicos de la columna categórica que queramos visualizar.
- Una columna donde tengamos el conteo de cada una de las categorías de la columna.

Esto lo podremos conseguir haciendo un `groupby`. Como en el caso del countplot, vamos a empezar contestando la siguiente pregunta:

_ _ _

## 📉 **Análisis de la Relación entre Variables Numéricas y Categóricas** 📉

En este apartado de la lección, casi todas las gráficas que vamos a usar ya las hemos aprendido a lo largo de la lección. La gráfica que no hemos visto hasta el momento es el barplot.

### **Barplot** 📊

Es una visualización que representa datos categóricos utilizando barras rectangulares. Es una herramienta efectiva para mostrar la distribución, comparación y relaciones entre diferentes categorías. Cada barra representa una categoría y su altura está proporcional a la frecuencia, el recuento o el valor asociado con esa categoría. Es un tipo de gráfico que encontramos tanto en Matplotlib como en Seaborn, así que pongámonos manos a la obra para ver cuál es la sintaxis de cada librería.

Sintaxis de un barplot usando Matplotlib:

```python
plt.bar(categorias, height=valores, color='blue')
```

Donde cada parámetro significa:

- `categorias`: Representa las categorías o etiquetas en el eje X del gráfico de barras.
- `height`: Corresponde a los valores numéricos asociados con cada categoría en el eje X.
- `color` (opcional): Controla el color de las barras en el gráfico.
- `data`: Es el DataFrame del que sacaremos los datos.
- `hue` (opcional): Permite agregar una dimensión adicional a la visualización al diferenciar las barras por un factor categórico adicional.

Sintaxis de un barplot usando Seaborn:

```python
sns.barplot(x='categorias', y='valores', palette='Set2', ci=None, hue='factor_adicional')
```

- `x`: Este parámetro especifica los valores que se ubicarán en el eje X del gráfico. En este caso, `categorias` es una lista de etiquetas o valores categóricos que se utilizarán en el eje X del gráfico de barras.
- `y`: Este parámetro establece los valores que se mostrarán en el eje Y del gráfico. Corresponde a los valores numéricos asociados con cada categoría en el eje X.
- `palette` (opcional): Aquí definimos la paleta de colores que se utilizará para colorear las barras en el gráfico. Seaborn proporciona varias paletas predefinidas, y "Set2" es una de ellas. Puedes utilizar otras paletas predefinidas o incluso crear tus propias paletas personalizadas.
- `ci` (opcional): Este parámetro controla la visualización del intervalo de confianza alrededor de las barras. Al establecerlo en `None`, se desactiva la representación del intervalo de confianza.
- `hue` (opcional): Permite agregar una dimensión adicional al gráfico de barras al diferenciar las barras por un factor categórico adicional.

```python
sns.barplot(x='categorias', y='valores', palette='Set2', ci=None, hue='factor_adicional')
```

_ _ _

## 📊 **Resumen** 📊

En esta lección, aprendiste a utilizar diversas herramientas y técnicas para la visualización de datos en Python, específicamente con la librería Seaborn.

### **Conceptos Clave**

1. **Violin Plot:** Combina características de boxplot y KDE plot para mostrar la distribución de datos.

   - **Sintaxis básica:**
     ```python
     sns.violinplot(x, y, data, color, palette, linewidth)
     ```
   - **Parámetros importantes:**
     - `x`: Variable categórica.
     - `y`: Variable numérica.
     - `data`: DataFrame con los datos.
     - `color`: Color para una sola variable.
     - `palette`: Paleta de colores para variables categóricas.
     - `linewidth`: Grosor de las líneas.

   - **Interpretación del Violin Plot:**
     - La forma del violín muestra la distribución.
     - Los picos indican densidad alta de datos.
     - La línea central puede representar la mediana o la media.

2. **Boxplot:** Visualiza la distribución de datos a través de sus cuartiles y valores atípicos.

   - **Sintaxis básica:**
     ```python
     sns.boxplot(x, y, data, hue, palette)
     ```
   - **Parámetros:**
     - `hue`: Agrupación adicional.

3. **Subplots y Facets:**
   - Utilización de `plt.subplots` y `sns.FacetGrid` para crear múltiples gráficos en una sola figura.

4. **Heatmaps:** Representan datos matriciales mediante colores.

   - **Sintaxis básica:**
     ```python
     sns.heatmap(data, annot, cmap)
     ```
   - **Parámetros:**
     - `annot`: Anotaciones en cada celda.
     - `cmap`: Mapa de colores.

### **Notas**

- Todas las gráficas deben tener título.
- Etiquetas de los ejes deben estar en español.
- Se anima a personalizar las gráficas para practicar.

### **Métodos para Modificar las Gráficas:**

| **Modificación**                            | **Método sin subplot**                        | **Método con subplot**                       |
|---------------------------------------------|----------------------------------------------|---------------------------------------------|
| Añadir título                               | `plt.title()`                                | `axes[n].set_title()`                       |
| Cambiar nombre del eje x                    | `plt.xlabel()`                               | `axes[n].set_xlabel()`                      |
| Cambiar nombre del eje y                    | `plt.ylabel()`                               | `axes[n].set_ylabel()`                      |
| Quitar línea de la derecha                  | `plt.gca().spines['right'].set_visible(False)` | `axes[n].spines['right'].set_visible(False)` |
| Limitar el eje x                            | `plt.xlim()`                                 | `axes[n].set_xlim()`                        |
| Limitar el eje y                            | `plt.ylim()`                                 | `axes[n].set_ylim()`                        |
| Cambiar las propiedades de las etiquetas del eje x | `plt.xticks()`                               | `axes[n].set_xticks()`                      |
| Cambiar las propiedades de las etiquetas del eje y | `plt.yticks()`                               | `axes[n].set_yticks()`                      |

_ _ _

Con estos conocimientos, ahora tienes las herramientas necesarias para explorar y visualizar tus datos de manera efectiva utilizando Seaborn y Matplotlib en Python. ¡Continúa practicando y experimentando con diferentes tipos de gráficos para mejorar tus habilidades en la visualización de datos!