# 🎰 **ESTADÍSTICA DESCRIPTIVA** 🎰

Es la recopilación, resumen, organización y presentación de datos.

## ⭐ **Medidas de Centralización** ⭐

Responden a la necesidad de entender el punto central o típico en un conjunto de datos. Estas medidas permiten identificar el valor alrededor del cual los datos tienden a agruparse. Aquí están las principales preguntas que responden las medidas de centralización:

1. **¿Cuál es el valor central o promedio de los datos?** 🧐  
   Indican el valor típico o representativo del conjunto de datos. Esto es útil para tener una idea general del nivel alrededor del cual se concentran los datos.
   
2. **¿Dónde se sitúa el centro de los datos?** 🎯  
   Ayudan a determinar el punto medio o central de la distribución de los datos, lo cual es fundamental para resumir y describir el conjunto de datos.
   
3. **¿Cuál es el valor más frecuente en los datos?** 🔄  
   Permiten identificar el valor que aparece con mayor frecuencia, lo que puede ser útil para entender el comportamiento típico en el conjunto de datos.

### 📶 **Tipos** 📶

- **Media (promedio):** 🧮  
  Es la suma de todos los valores dividida por el número total de valores. Proporciona un valor central, pero puede verse afectada por valores extremos (outliers).
  
- **Mediana:** 📏  
  Es el valor que divide el conjunto de datos en dos partes iguales. La mitad de los valores son menores que la mediana y la otra mitad son mayores. Es una medida robusta que no se ve afectada por valores extremos.
  
- **Moda:** 🥇  
  Es el valor que ocurre con mayor frecuencia en el conjunto de datos. Un conjunto de datos puede tener más de una moda (bimodal o multimodal) si varios valores tienen la misma frecuencia máxima.

## 🔍 **Medidas de Dispersión** 🔍

Responden a la necesidad de entender cómo se distribuyen los datos alrededor de un valor central (como la media) en un conjunto de datos. En otras palabras, nos dicen qué tan extendidos o agrupados están los datos. Aquí están las principales preguntas que responden las medidas de dispersión:

1. **¿Qué tan lejos están los datos entre sí?** 📏  
   Las medidas de dispersión indican la extensión total de los datos, mostrando si los datos están muy separados (dispersos) o muy cercanos entre sí.
   
2. **¿Cómo se distribuyen los datos respecto a la media?** 📊  
   Ayudan a comprender la variabilidad de los datos en relación con la media, revelando si los datos están muy dispersos alrededor de la media o si están más concentrados cerca de ella.
   
3. **¿Cuánta variabilidad existe en los datos?** 🔄  
   Proveen una idea de la variabilidad o inconsistencia en los datos, lo cual es crucial para tomar decisiones informadas. Por ejemplo, en una serie de mediciones, una baja dispersión indica mediciones consistentes.
   
4. **¿Cuál es la extensión total de los datos?** 🌐  
   Responden a la amplitud de los datos, es decir, la diferencia entre el valor más alto y el valor más bajo.

### 📶 **Tipos** 📶

- **Rango:** 📏  
  Es la diferencia entre el valor más alto y el valor más bajo en un conjunto de datos. Te dice cuánto varían los datos.
  
- **Varianza:** 🔄  
  Es una medida de dispersión que indica cuánto se dispersan o se alejan los valores de un conjunto de datos respecto a su media. En términos sencillos, la varianza calcula el promedio de las diferencias al cuadrado entre cada valor y la media.
  
  1. Se encuentra la media (promedio) del conjunto de datos.
  2. Se resta la media a cada valor para obtener las diferencias.
  3. Se elevan al cuadrado estas diferencias.
  4. Se calcula el promedio de estos valores al cuadrado.
  
- **Desviación estándar:** 📊  
  Es una medida que indica cuánto varían los datos respecto a la media. Una desviación estándar alta significa que los datos están muy dispersos, mientras que una baja indica que están más agrupados cerca de la media. Es la raíz cuadrada de la varianza.

## 🔗 **Medidas de Correlación** 🔗

Responden a la necesidad de entender la relación entre dos variables. Aquí están las principales preguntas que responden las medidas de correlación:

1. **¿Existe una relación entre dos variables?** 🔗  
   Las medidas de correlación indican si hay una conexión o asociación entre dos variables. Esto puede ayudar a determinar si los cambios en una variable pueden estar relacionados con cambios en otra.
   
2. **¿Qué tan fuerte es la relación entre las variables?** 💪  
   Miden la fuerza de la relación, mostrando si la conexión es débil, moderada o fuerte. Una correlación fuerte implica que los valores de una variable están muy relacionados con los valores de la otra.
   
3. **¿Cuál es la dirección de la relación?** 🔄  
   Indican si la relación es positiva o negativa. En una relación positiva, ambas variables aumentan o disminuyen juntas. En una relación negativa, cuando una variable aumenta, la otra disminuye.
   
4. **¿Qué tipo de relación existe entre las variables?** 🔍  
   Las medidas de correlación pueden sugerir si la relación es lineal (como lo mide el coeficiente de correlación de Pearson) o no lineal (como lo mide el coeficiente de correlación de Spearman).

**Entre qué valores pueden tomar esas relaciones: -1 y 1.**

- **Relación -1:** ➖ Indica una relación inversa (una variable sube mientras la otra baja).
- **Relación 1:** ➕ Indica que ambas variables van en el mismo sentido (una sube y la otra también).

### 📶 **Tipos** 📶

#### 📏 **Coeficiente de Correlación de Pearson** 📏

- **Qué mide:** La fuerza y dirección de la relación lineal entre dos variables.
- **Rango:** Va de -1 a 1.
  - 1 indica una correlación positiva perfecta (ambas variables se mueven en la misma dirección).
  - -1 indica una correlación negativa perfecta (una variable sube mientras la otra baja).
  - 0 indica que no hay correlación lineal.
- **Uso:** Es útil para variables que tienen una relación lineal y están en una escala de intervalo o razón.

#### 🔄 **Coeficiente de Correlación de Spearman** 🔄

- **Qué mide:** La fuerza y dirección de la relación monotónica entre dos variables (basada en rangos).
- **Rango:** También va de -1 a 1.
  - 1 indica una correlación positiva perfecta en términos de rangos.
  - -1 indica una correlación negativa perfecta en términos de rangos.
  - 0 indica que no hay correlación en los rangos.
- **Uso:** Es útil para variables ordinales o cuando la relación entre las variables no es lineal pero es monotónica.

#### 🔍 **Coeficiente de Correlación de Kendall** 🔍

- **Qué mide:** La fuerza y dirección de la relación monotónica entre dos variables, basado en la concordancia y discordancia de pares de observaciones.
- **Rango:** Va de -1 a 1.
  - 1 indica una concordancia perfecta.
  - -1 indica una discordancia perfecta.
  - 0 indica que no hay concordancia.
- **Uso:** Es útil para pequeñas muestras de datos y para datos ordinales o cuando se espera una relación monotónica.

#### 🔗 **Covarianza** 🔗

- **Qué mide:** Cómo dos variables cambian juntas.
- **Valor:** No tiene un rango fijo, y su valor depende de las unidades de las variables.
  - Un valor positivo indica que las variables tienden a aumentar juntas.
  - Un valor negativo indica que una variable tiende a aumentar mientras la otra disminuye.
- **Uso:** Aunque no es una medida estandarizada, es la base para calcular el coeficiente de correlación de Pearson.

### 📶 **Tipos** 📶

#### ✅ **Relación Positiva** ✅

En este gráfico, ambas variables aumentan juntas. Un ejemplo podría ser:
- **Variable X:** Horas de estudio.
- **Variable Y:** Puntuación en un examen.

![Relación Positiva](https://github.com/MabelMaff/Apuntes_Adalab/blob/main/M%C3%B3dulo%2003/relaciones.png)

#### ❌ **Relación Negativa** ❌

En este gráfico, una variable aumenta mientras la otra disminuye. Un ejemplo podría ser:
- **Variable X:** Cantidad de cigarrillos fumados por día.
- **Variable Y:** Capacidad pulmonar.

![Relación Negativa](https://github.com/MabelMaff/Apuntes_Adalab/blob/main/M%C3%B3dulo%2003/relaciones.png)

#### ⤵ **Relación Débil** ⤵

En este gráfico, no hay una relación clara entre las variables. Un ejemplo podría ser:
- **Variable X:** Número de zapatos en el armario.
- **Variable Y:** Tiempo dedicado a ver televisión por día.

![Relación Débil](https://github.com/MabelMaff/Apuntes_Adalab/blob/main/M%C3%B3dulo%2003/relaciones.png)

#### 📏 **Sin Correlación** 📏

En este gráfico, no hay una relación significativa entre las variables. Un ejemplo podría ser:
- **Variable X:** Tamaño del pie.
- **Variable Y:** Nivel de inteligencia.

Claro, aquí tienes la sección actualizada con las medidas categóricas y relativas:

## 🏷️ **Medidas Categóricas** 🏷️

Responden a la necesidad de entender y resumir datos que se clasifican en categorías. Estas medidas permiten analizar la frecuencia y distribución de las categorías en un conjunto de datos. Aquí están las principales preguntas que responden las medidas categóricas:

1. **¿Cuántos datos pertenecen a cada categoría?** 📊  
   Indican la frecuencia de cada categoría, lo que ayuda a entender la distribución de los datos en diferentes grupos.

2. **¿Cuál es la categoría más frecuente?** 🥇  
   Permiten identificar la categoría que aparece con mayor frecuencia, proporcionando información sobre la moda en datos categóricos.

3. **¿Cómo se distribuyen los datos en diferentes categorías?** 🌍  
   Ayudan a visualizar y comprender la proporción de datos en cada categoría, facilitando comparaciones entre diferentes grupos.

### 📶 **Tipos** 📶

- **Frecuencia Absoluta:** 📈  
  Es el número de veces que aparece cada categoría en el conjunto de datos. Permite conocer el conteo exacto de cada categoría.

- **Frecuencia Relativa:** 🔢  
  Es la proporción de veces que aparece cada categoría respecto al total de datos. Se calcula dividiendo la frecuencia absoluta de una categoría por el número total de observaciones.

- **Tabla de Frecuencias Cruzadas:** 📊  
  Es una tabla que muestra la frecuencia con la que ocurren combinaciones de categorías de dos variables. Es útil para analizar la relación entre dos variables categóricas.

- **Moda:** 🥇  
  Es el valor que ocurre con mayor frecuencia en un conjunto de datos. En datos categóricos, la moda es la categoría más común.

## 📊 **Medidas Relativas** 📊

Responden a la necesidad de comparar datos entre sí de manera proporcional. Estas medidas permiten evaluar datos en términos relativos, facilitando comparaciones y análisis más precisos. Aquí están las principales preguntas que responden las medidas relativas:

1. **¿Cuál es la relación entre dos valores?** 📏  
   Permiten comparar dos valores para entender su relación proporcional, como ratios o índices.

2. **¿Qué porcentaje del total representa un valor?** 💯  
   Ayudan a calcular qué proporción de un total representa un valor específico, proporcionando información sobre su importancia relativa.

3. **¿Cómo se comparan los datos en diferentes contextos?** 🌐  
   Facilitan la comparación de datos en diferentes contextos o grupos, utilizando proporciones o tasas para estandarizar los resultados.

### 📶 **Tipos** 📶

- **Percentiles:** 📊  
  Dividen un conjunto de datos ordenados en 100 partes iguales. Cada percentil indica el valor por debajo del cual se encuentra un cierto porcentaje de observaciones.

- **Cuartiles:** 🔢  
  Dividen un conjunto de datos ordenados en cuatro partes iguales. El primer cuartil (Q1) es el valor que separa el 25% inferior del resto, el segundo cuartil (Q2) es la mediana, y el tercer cuartil (Q3) separa el 75% inferior del 25% superior.

- **Deciles:** 📉  
  Dividen un conjunto de datos ordenados en diez partes iguales. Cada decil indica el valor por debajo del cual se encuentra un cierto 10% de observaciones.

Espero que esto cumpla con tus expectativas y se ajuste a la estructura deseada.
![Sin Correlación](https://github.com/MabelMaff/Apuntes_Adalab/blob/main/M%C3%B3dulo%2003/relaciones.png)


