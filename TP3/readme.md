# Histograma de una imagen

## 1. Gráfico de histogramas
Se representa la distribución de las luminancias de los píxeles de una imagen en una gráfica para posterior interpretación.

## 2. Normalización de histogramas
Se normaliza el histograma de valores de una imagen al rango $[0, 1]$. Esto se realiza de dos maneras:

1. **MinMax:** el valor mínimo de las luminancias de la imagen, adquiere el valor de $0$ y el máximo $1$.
2. **Percentil:** los pixeles inferiores al percentil $P$ vale $0$ y los pixeles con luminancias superiores al percentil $(100 - P)$ valen $1$.

## 3. Corrección Gamma
Aplicación de la corrección gamma $(\gamma)$ a una imagen. Esto significa que, los valores para las luminancias de la imagen de salida $(Y_{out})$ son 
equivalentes a los valores de luminancia de la imagen de entrada $(Y_{in})$ potencia de un factor denominado gamma $(Y_{out} = Y_{in}^\gamma)$. En función 
de los valores asignado a $\gamma$ la imagen completa se aclara u oscurece. Dos de los valores más conocidos son:

1. **Filtro de raíz cuadrada $(\gamma = 1/2)$:** realza los pixeles oscuros y modifica levemente los pixeles con alta luminosidad.
2. **Filtro cuadrático $(\gamma = 2)$:** presenta un comportamiento inverso al filtro de raíz cuadrada.

## 4. Corrección con una función definida a tramos
Este tipo de corrección permite oscurecer los pixeles oscuros y viceversa con los pixeles de alta luminosidad. De esta forma, no se oscurece ni aclara toda
la imagen (implementado a imágenes con mal contraste o mal rango dinámico). En función de los valores de luminancia de la imagen de entrada $(Y_{in})$, 
los valores de luminancia para la imagen de salida $(Y_{out})$ se definen de la siguiente manera:

$$Y_{out} = \begin{Bmatrix}
 0,&Y_{in} < Y_{min}  \\
 1,&Y_{in} > Y_{max}  \\
 f(Y_{in}),&Y_{min} < Y_{in} < Y_{max} \\
\end{Bmatrix}$$

Donde $Y_{min}$ es el valor de luminancia que permite oscurecer los pixeles oscuros lo cual define una región denominada *Black Out*; $Y_{max}$ es el umbral 
en el cual se aclaran los pixeles con alta luminosidad y define una región llamada *White Out* y por último, $f(Y_{in})$ es la interpolación entre las 
luminancias de entrada y la recta formada por los puntos de $Y_{min}$ y $Y_{max}$ (como se muestra en la imagen a continuación).

![índice](https://user-images.githubusercontent.com/71833624/170558610-e5915c30-2504-4595-8357-af82a7246624.png)

## 5. Ecualización del histograma
Se asigna a cada pixel un valor de luminancia proporcional a la cantidad de pixeles menos luminosos que él mismo

## 6. Normalización del histograma
Se ajusta la media y varianza del histograma original a la Gaussiana.
