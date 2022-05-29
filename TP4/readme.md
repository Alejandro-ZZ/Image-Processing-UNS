# Transformada Rápida de Fourier (FFT) en imágenes

## 1. Visualización del espectro de una imagen

1. `Carga de la imagen` a procesar. La misma debe estar en escala de grises (o ser transformada en una), es decir, debe ser una matriz de la forma (ancho, alto).
2. `Cálculo del espectro` de la imagen cuya componente, de frecuencia cero,  se encuentre centrada. La magnitud y fase se encuentran en el rango [0, 1] y [$-\pi$, $\pi$].
3. `Transformada logarítmica` a la magnitud del espectro. Esto se hace, ya que los coeficientes de energía del mismo presentan valores pequeños (a comparación de los valores de una imagen común) y con una principal importancia en el 5% de ellos.
4. `Escala de los valores` obtenidos de magnitud y fase en el rango de una imagen común entre 0 y 255.
5. `Visualización` del espectro de la imagen procesada.
6. `Guardado` del espectro y fase en imágenes en escala de grises en formato *bmp*.

## 2. Reconstrucción de una imagen a partir de su espectro

1. `Carga de la magnitud y fase` de la imagen que se desea reconstruir. Estos dos elementos son imágenes en escala de grises guardadas en el proceso anterior.
2. `Escala de las componentes` a sus valores iniciales. Para el caso de la *fase* en el rango de [$-\pi$, $\pi$] y para la *magnitud*, los respectivos arrojados según la transformación logarítmica aplicada.
3. `Transformada logarítmica inversa` para los valores de la magnitud del espectro.
4. `Cálculo de la FFT inversa` a partir de los valores reconstruidos de la fase y magnitud.
5. `Visualización` de la magnitud de la imagen reconstruida.

## 3. Corrección de una imagen con ruido

* Se toma una imagen en escala de grises con interferencia aditiva.
* Se aplica el flujo de trabajo del primer punto.
* Mediante un editor de imágenes, en la magnitud de la imagen, se eliminan las componentes de energía a la frecuencia de la interferencia y se guarda.
* Se aplica una reconstrucción de la imagen (segundo punto) con la magnitud del espectro modificada.
* Se contrasta la imagen original junto a la imagen corregida.  
