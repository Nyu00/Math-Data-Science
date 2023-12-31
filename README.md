# Math-Data-Science

En estas notas haremos entender el concepto de Estadística Descriptiva

## Estadística descriptiva vs. inferencial

Hablemos de DEPORTES.

Tomando un jugador de futbol por ejemplo, cuando ves sus **Estadisticas** deportivas esos numeros nos quantifican el desempeño de dicho jugador despues de muchos partidos y todos los datos de cada uno de los partidos, despues de cierta cantidad de tiempo quedaría una base de datos del metricas del jugador lo suficientemente grande como para crear metricas resumidas para entender de forma sencilla corta y concreta el desempeño del jugardor sin tener que ver todos y cada uno de los partidos de el jugador

Ahí entendemos el punto fundamental de la estadistica , la **Descriptiva** la cual se basa en:
***RESUMIR***

Por otro lado la Estadistica Inferencial se enfoca mas en la parte de predecir el futuro en datos que ya tenemos disponibles, usando el ejemplo del jugador de futbol de nuevo la estadistica inferecial se enfocaria en predecir como será el desempenho de dicho jugador en proximos partidos

![Estadistica Deportiva](./src/Estadistica.PNG)

Es esa grafica podemos ver como comparan el desempeño de varios jugadores de futbol, nos interesa ver cada uno de los jugadores esta categorizado por varios metricas, n° de partidos jugados, n° de minutos jugados, n° de goles, n° de asistencias, etc apartir de estos numero podemos sacar un unico numero que ellos llamaron Rating

Hay cosas buenas y malas con esto, porque resulta que podemos mentir con este tipo de estadisticas, la estadistica descriptiva apesar de ser una rama de las matematicas, tiene un problema de raiz, que es lo siguiente

**¿Como yo defino que algo es correcto o no?**

En este cas, ¿como defino un metrica unica que defina cual es el mejor jugador?, no existe verdad?´

Pues porque la definicion de "el mejor jugador" puede ser diferente para diferentes personas, por ejemplo hay personas que podrian decir que para ellas el mejor jugador es que hace mas asistencias porque es el estratega, el que se pasa a los defensa y luego hace un pase estrategica que terminaria eventualmente haciendo el gol ,pero para otras podrian decir que el mejor jugador es el que hace mas goles por al final del dia los goles son los que ganan los partidos, etc

Ahora, quien tiene la razon; **AMBOS**

Ambas son metricas validas, solo que cada una de esas metricas de mostratá diferentes lados de una misma moneda, y esto nos da la posibilidad de mentir

![cite](./src/cite.jpg)

**¿Por qué aprender estadística?**

- Resumir grandes cantidades de información. 
- Tomar mejores decisiones (¿o peores?). 
- Responder preguntas con relevancia social. 
- Reconocer patrones en los datos.
- Descubrir a quienes usan estas herramientas con fines nefastos.

## Flujo de trabajo en Data Science

![Flujo de trabajo](./src/flujo.jpg)

En la imagen anterior te puedes percatar que hay una linea de cajas verdes que define el flujo de trabajo en data science leyendose de izquierda a derecha

## Medias de Tendencia Central

Imaginate un salon con estudiantes, estos tienen diferentes edades, y alguna persona te dice que "Oye, en ese salon la edad promedio de los estudiantes es de 7 años", Eso te puede dar varios pensamientos, como por ejemplo, Son estudiantes jovenes pero eso no quiere decir que todos estudiantes tengan 7 años, sino, que sus edades son mas o menos cercanas a 7 años

A lo queremos llegar con esto es a que las medidas de tendencia central son una manera de resumir informacion

Esto tiene sus desventajas y ventajas, puedes extraer informacion valiosa, como por ejemplo suponer que son estudiantes jovenes, la desventaja es, que pasa si hay estudiantes que son demasiado viejos o jovenes en ese salon, el promerio no puede dar informacion de eso, y crees que esos estudiantes estan afectando mi medida de promedio?

Hay que recordar que siempre que querramos "resumir informacion" estamos haciendo invisibles ciertos datos

### ¿Tendencia Central?

Existen tres medidas de tendencia central

- Media (promedio)

Esta tendencia tiene que ver con una nocion de centralidad de los datos, es resumo de los datos

- Mediana (dato central)

Este es el dato que esta en la mitad, a los dos lados tiene la misma cantidad de gatos

- Moda (dato mas repetido)

Este es simplemtente el dato que mas se repite

## Diagrama de frecuencias

![diagrama](./src/diagrama.PNG)

Tenemos una lista de estudiantes, en este caso 20, con estos podemos considerar que son estudiantes mas viejos de 16, 17, 18 y queremos contar con la frecuencia segunda tabla de frecuencias la construimos asi; la edad mas poequeña tienen 15 años y contar cuantos de ellos tienen 15 años, en este caso nos da 3 entonces en la tabla de frecuencias y asi con las otras edades
ia que se repite cada edad


Ahora, viendo ese diagrama de frecuencia podemos decir que la **Moda** es 18 años, eso es facil, pero ahora como hacemos con la media y la mediana?

### ¿Cuando usar cuál?

- La media es susceptible a varios atípicos.

Si tenemos un cojunto de personas todas tiene edades muy cercanas, la adicion de una persona con una edad mucho mayor, la medida resultante se va a ver fuertemente afectada por esa persona mayor, el ejemplo seria el mismo si es mas joven

- La moda no aplica para datos numéricos continuos

## Metáfora de Bill Gates en un bar



**_{X<sub>1</sub>, X<sub>2</sub>, X<sub>3</sub>, X<sub>4</sub>, ..., X<sub>n</sub>}_ DataSet**

Este dataset se un conjunto que tiene n elementos distintos, como edades, salarios, etc. Si quisiera sacar el promedio de ese dataset se hace de la siguiente manera:

![media](./src/media-formula-normal.jpg)

La **Media** de este dataset se define como = X̅

Esta se calcula como sumar todos los valores del conjunto o Dataset, asi:

X<sub>1</sub>+ X<sub>2</sub>+ X<sub>3</sub>+ X<sub>4</sub>+ ...+ X<sub>n</sub>

Y luego el resultado de esa suma, la dividimos por la cantidad de datos, asi:

```bash
1/n
```

Tambien existe una forma contraria de escrivir esta suma

![media-resumida](./src/media-formula-compacta.jpg)

Esta formula en pocas palabras quiere decir que estoy recorriendo todos los valores de X (Nuestro dataset)

La **mediana** tiene algo peculiar, como queremos definir el dato central, tenemos que tomar en consideracion si la cantidad de datos de nuestro dataset es par o impar, porque si es par tendremos que tomar los dos datos que esten en el medio y si es impar tomaremos un unico dato del medio

![Formula median](./src/median.jpg)

Ahora imaginate un bar, donde hay 10 hombres bebiendo, cada unos de esos hombre tienen un salario, en este ejemplo supondremos que cada unos de estos sujetos tienen curiosamente el mismo salario que sera 35.000$ al año, ahora con estos datos ya podemos calcular el promedio, la media y la moda todos seria 35.000$

Podriamos decir que en ese bar el salario promedio de la personas que van en de 35000$ anuales

Pero, ahora llega Bill Gates y se sienta al lado de los 10 señores, supongas que el tiene un salario anual de 1.000.000$ 

Si ahora quisieramos calcular el salarios promedio de la personas de aquel bar los valores cambiarian mucho

![formula bill gates](./src/formula-billgates.jpg)

El promedio sería ahora 122,727.27 $, o sea 87,727 más por una única persona muy alejada del promedio

Ahora la mediana, si agarramos los valores del medio (estando los salarios organizados) el valor será una aproximación más realista, ya que esta no está tan sesgada por valores atípicos como en ente caso el de Bill Gates

![med](./src/med.jpg){:width="50%"}

## Medidas de dispersion

En temas pasados dijimos que en un grupo de estudiantes deciamos que el promedio de edad era 7 años, pero puede que haya estudiantes muy viejos o muy jovenes en "comparacion al promedio", bueno ahora necesito tener una nocion matematica de como medir esa dispersión de las edades (Datos), para estas existen 3 definiciones fundamentales;

- Rango
- Rango intercuartil
- Desviacion Estandar

![RRD](./src/rrd.jpg)

Tenemos un histogramas con una forma de campana (o distribución gaussiana) con unos datos de ejemplo ahora para entender las medidas de dispercion debemos enterder esto;

La manera mas rapida de medir un conjunto de datos es agarrar el valor minimo y el valor maximo, y restarlos, y esa medida es lo que llamanos el **rango**

El **Rango intercuartil** se basa en los cuartiles, estos tienen como proposito definir 4 grupos de datos de manera uniforme o sea la misma cantidas de datos en cada unos de estos grupos de datos (cuartiles) como sale en la parte de abajo del ejemplo

En este prodriamos agarra la mediana que ya conocemos y este seria el Q2, ¿porque? porque nosotros queremos las cuartas partes ahora esas dos mitades las partimos por la mitas y donde queda la linea de divicion los definiremos como Q1 y Q3

La distancia entre el Q1 y el Q3 es el **Rango intercuartil**

###### Nota: IQR con las siglas de rango intercuartil en ingles

## Desviacion estándar

Tenemos un dataset aleatorio, la media de esas data set set la suma de todo los valores divido por la cantidad de valores, de la siguiente manera:

![media](./src/media.jpg)

Los primeros caracteres significan lo mismo "la media"

Ahora imaginate una grafica con los valores organizados horizonantalmente, imaginemos que el μ (media) es cercado al medio 

![mediaerror](./src/masnemoserror.jpg)

Una buena medida de dispercion es calcular la variacion de cada punto, lo que pasaria es que algunos saldrian negativo o positivos en comparacion al μ, y eso esta mal, para evitarlo

Tomamos cada unos de los valores y la diferencia con el μ, su resultado lo elevamos al cuadrado, despues hacemos esos con todos los valores y lo dividimos por la cantidad de elementos

Esto nos daria lo que conocemos como la varianza o sigma al cuadrado

### Distrubucion normal

![normdist-1](./src/normdist-1.jpg)

El σ (desviacion estandar) el representa la disperciones en este caso (gausianamente), cuando consideramos al rededor de la media y la mediana, 3 distancias hacia adelante y 3 distancias hacia atras de la μ, de esa manera estariamos tomando en cosideracion un 99.72% de los datos

![9972](./src/9972.jpg)

En terminos de rango intercuartil seria asi:

min = Q¹ - 1.5IQR
max = Q¹ - 1.5IQR

## Medidas de dispersión PY

Dataset (https://www.kaggle.com/lepchenkov/usedcarscatalog)

Usaremos las librerias pandas, meatplotlib y seaborn y usarmos de dataset de carros

creamos un dataframe con pandas sobre nuestro dataset y lo llamamos df


```python
import pandas as pd 
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv('cars.csv')
```
Calcularemos la desviación estándar de la columna de datos de price_usd que contiene el precio de los autos usando el metodo .std()

```python
# Desviación estandar
df['price_usd'].std()
#/////////////////////////////////////////
6428.1520182029035
```

ahora queremos definir el rango de esta columna, esto se hace de la siguiente manera

```python
# Rango = valor max - valor min
rango = df['price_usd'].max() - df['price_usd'].min()
rango
#/////////////////////////////////////////
49999.0
```

ahora definimos por cuartiles, el valor mínimo y el valor máximo

```python
# Quartiles
median = df['price_usd'].median()
Q1 = df['price_usd'].quantile(q=0.25)
Q3 = df['price_usd'].quantile(q=0.75)
min_val = df['price_usd'].quantile(q=0)
max_val = df['price_usd'].quantile(q=1.0)
print(min_val, Q1, median, Q3, max_val)
#/////////////////////////////////////////
1.0 2100.0 4800.0 8990.0 50000.0
```

Y el rango inter cuartil o IQR

```python
iqr = Q3 - Q1
iqr
#/////////////////////////////////////////
6890.0
```

Límites para detección de outliers (datos simétricamente distribuidos)
Datos entre Q₁ - 1.5 x IQR y Q₃ + 1.5 x IQR


```python
minlimit = Q1 - 1.5*iqr
maxlimit = Q3 + 1.5*iqr
print('rango para detección de outliers: {}, {}'.format(minlimit, maxlimit))
#/////////////////////////////////////////
rango para detección de outliers: -8235.0, 19325.0
```

Esto no tiene sentido como nos referimos a variables de precio, esto pasa cuando intentamos el metodo de cuando el dataframe tiene una distribución gausiana en un dataframe que no lo es, para hacerlo con distribuciones no normales

```python
sns.set(rc={'figure.figsize':(11.7,8.27)})
f, (ax_hist, ax_box) = plt.subplots(2, sharex=True, gridspec_kw={"height_ratios": (.6, .4)})
sns.histplot(df['price_usd'], ax=ax_hist)
sns.boxplot(df['price_usd'], ax=ax_box)
ax_hist.set(xlabel='')
```

![grafico2](./src/grafico1.jpg)

Es posible calcular varios box-plot separando por una cierta variable categórica:

```python
sns.boxplot(x = 'engine_fuel', y = 'price_usd', data = df)
```
![grafico2](./src/grafico2.jpg)

## Diagrama de dispersión

Usaremos las librerias pandas y seaborn con una dataset iris que es un dataset que corresponde a atributos especiales de unas flores llamadas **iris** en tres especies diferentes

```python
import pandas as pd 
import seaborn as sns

iris = sns.load_dataset('iris')

iris.head()
```

![iris-head](/src/iris-head.jpg)

podemos ver características como longitud del sépalo, anchura del sépalo, longitud del pétalo, anchura del pétalo y especies 

```python
# scatterplot 
sns.scatterplot(data=iris, x = 'sepal_length', y = 'petal_length', hue = 'species')
```

Aqui cada punto hace tiene un eje Y y X que hace referencia a las variables petal_length y sepal_length y separa cada unos de esos puntos por colores segun la categoria que lo llamamos el **Hue** en el codigo usando sns  

![scatterplot](./src/scatterplot.jpg)

Ahora tambien podemos haciendolo de la siguiente manera podemos hacer un histograma o grafico de frecuencia cada unos de los eje X y Y

```python
sns.jointplot(data=iris, x = 'sepal_length', y = 'petal_length', hue = 'species')
```

![sns-histograma](./src/sns-histograma.jpg)

Lo importante de este sector es entender el diagrama de dispercio por que este nos ayuda a ver posibles patrones entre dos varibles y encontrar posibles correlaciones

## Procesamiento de datos

El primer proceso que utiliza estadísticas y requiere elementos que ya hemos estudiado en clases previas, especialmente cuando se trata de datos numéricos, se llama **Escalamiento lineal**

Porque debemos escalar o normalizar los datos? Resulta que los modelos de machine learning son son optimos siempre y cuando los atributos que se les da a ese modelo tengan las mismas dimenciones, por ejemplo no tendria sentido que yo tenga un atributo que vaya de 0 a 1 y otro que vaya de 1 a 1.000.000, lo hace insostenible porque los factores son medidos de formas distintas, quitando el hecho que se necesitaria mas computo, estos estan normalizados a un rango de -1 á 1

##### OJO:
los diferentes tipos de escalmeinto se usan siempre y cuando estan uniformemente más o menos distribuidos, de manera gauseana o normal

Hay varios tipos de escalamiento

- Escalamiento Min-Max

Este escalamiento nos dice que cada dato lo tenemos que tranformar a un valor normalizado de ese dato

La tranformacion seria esta

![minmax](./src/min-max.jpg)

- Escalamiento Clipping

Es uno muy usado pero no muy recomendado

Este nos deci que debemos tomar la distribucion y definimos 2 valores limite, los datos que esten dentro de ese rango no se ran cambiados mientras los que no esten, seran condensados

- Z-Score

Este es uno me los mas correctos porque toman en considerancion la desviacion de estandar

Esta es su formula:

![z-score](./src/z-score.jpg)

Ahora para transformar datos cuando  no estas distribuidos de manera normal una usaremos **Transformación no lineal**

Realmente lo que haremos es transformar los datos con una distrubucion no lineal en datos con una distrucion lineal para luego pasarle algunos de los escalamientos convencionales

## Transformación no lineal


Los usamos para dataset fuertemente sesgados o no simetricos

Estos los usamos antes de hacer una escalacion para un modelo de ML

Existen varios tipo como Logaritmos, Sigmoides, Polinomiales, etc para transformar los datos en lineales

### Distribuion sesgada

![distribucion sesgada](./src/distribuionsesgadajpg)

Ahora vamos a ver como es efecto de una transformacion no lineal en terminos de una funcion no lineal, usaremos la tanhente hiperbolica

![hiperbolica](./src/hiperbolica.jpg)

![formulatan](./src/formulatanhente.jpg)

La idea detras de esta tranformacion es que esta entre 1 y -1, lo queremos hacer es interpretar la X como los datos originales y la Y como los datos trandormados

### Pipelines de procesamiento para variables categóricas

Existen dos metodos para procesar variables categoricas de manera facilmente interpretables

- Dummy
Esta es una representacion compacta por eso es mejor usarla cuando tus inputs son linealmente independientes (no tienen un grado de relacion significativa)

- One-hot
Es uma mapeo mas grande que puede resultar en atriutos numericos que van a ser mas extensos para las variables categoricas

La diferencia que tienes este sobre el dummy es que este permite incluir categorias que no estaban en el data set inicialmente


Ambos sigues las reglas de tienes que mapear numericamente las categorias de cadenas de texto

Estas categorias representan algo llamado no ordinal (porque no tiene algun tipo de orden)

![one-hot](./src/one-hot.jpg)

Los podemos aplicar en python de la siguiente forma

```py
import pandas as py

df = pd.read_csv('cars.csv')

pd.get_dummies(df["engine_type"])

```

![dummy](./src/dummy.jpg)

Aqui este nos crea tres columnas porque solo existen 3 tipos de motor, diesel, electricos y a gasolina, cuando en carro en cuestion especifique que tipo de motor tiene tendra un 1 en la comundo del tipo de motor

en el ejemplo de la imagen solo tiene gasolina pero es solo porque es el mas comun

```py
import sklearn.preprocessing as preprocessiing


# Creamos un metodo codifacion de variables categoricas (texto)
# Le daremos el argumento de handle_unknow que sirve para manejar categorias nuevas que no estaban anteriormente contempladas
encoder = preprocessing.OneHotEncoder(handle_unknow="ignore")

encoder.fit(df[['engine_type']].values)

encoder.transform([['gasoline'], ['diesel'], ['aceite']]).toarray()
```

![onehot](./src/onehot.jpg)

# Correlaciones

Como hemos visto en lo graficos de dispercion nos permite visualzar como variaba la variacion de varible sobre otras en nuestro conjunto de datos, y ver varias varibles que parecen que tienen el mismo compartamiento, ahí decimos que estan relacionadas, de manera informal que estan corelacionadas

Entonces no tendria sentido usar las dos varibles porque las dos varibles esten aportando la misma informacion si su coorelaion es muy alta

Por eso hau eliminar varios datos tomando en considerancion esos datos de correlacion

En otro caso cuando tenemos variables categorias y las convertimos a numeros eso extande el espacion de atributos numericos, hay tambien podriamos ver si eciste algun tipo de correlacion y eliminar ciertos datos

![formlavarianza](./src/formlavarianza.jpg)

El concepto de correlacion tiene que ver con medir las deviaciones o variaciones un una variable x en relacion a otra variable

nosotros agarramos las variaciones de cada elemento X que tiene de su elemento, lo multiplicamos por x,  ahora agarramos las variaciones de cada elemento Y que tiene de su elemento

Es como si tuvieramos dos listas una de las variables x y una de las variables y 

![cov](./src/cov.jpg)

Algo para tener prensente es que enten en direrenten proporciones las Y podrias llegar hasta el millon y las X llegar solo al 5

por esto es que cada vez que hagamos la diferencia Yⁱ y el promedio de las Y las debemos dividir por la desviacion estandar, para entandarizar las variables

Esto lleva a un nuevo concepto llamada 






