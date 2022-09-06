# Remuestreo, reconstrucción y cuantización

## 1. Downsampling 2x2

**1.1. `Nearest neighbour (NN)`** Se reduce la resolución de la imagen muestreando la misma cada 2 píxeles.

**1.2. `Average`** Se reduce la resolución de la imagen muestreando la misma en una grilla de 2x2 y extrayendo el promedio de los cuatro valores.

![downsampling](https://user-images.githubusercontent.com/71833624/188714758-019ce1e5-b3bc-4ffa-8987-8acf1aa47071.png)

**1.3. `Gaussian Filter + Nearest neighbour (NN)`** Se aplica un filtro pasabajos (gaussiano) a la imagen seguido de una reducción de resolución por medio del método *Nearest neighbour (NN)*

![índice](https://user-images.githubusercontent.com/71833624/188710883-413e1ed3-1fd4-4515-b9b4-c99bb6735df4.png)

## 2. Upsampling 2x2

**2.1. `Nearest neighbour (NN)`** Se aumenta la resolución de la imagen repitiendo los píxeles en una grilla de 2x2.

**2.2. `Bilinear`** Aumento de resolución de la imagen por medio de una interpolación bilineal.

**2.3. `Bicúbica`** Aumento de resolución de la imagen por medio de una interpolación bicúbica.

![upsampling](https://user-images.githubusercontent.com/71833624/188713850-0ef164a9-1c62-4898-b988-40452cdc87c4.png)

**2.4. `Nearest neighbour (NN) X2 + Gaussian Filter`** Se aumenta la resolución por medio del método *Nearest neighbour (NN)* y seguido se aplica un filtro pasabajos (gaussiano) a la imagen.

![índice](https://user-images.githubusercontent.com/71833624/188715441-c3d47c9f-0690-4fc8-9d91-775d11cc9b94.png)

## 3. Resampling using Fast Fourier Transform (FFT)

**3.1. `Downsampling`** Se calcula la FFT de la imagen (con la frecuencia cero centrada), se recorta simétricamente al tamaño deseado y finalmente se calcula la FFT inversa.

![resampling_FFT](https://user-images.githubusercontent.com/71833624/188717027-ab23f4e6-1075-4f45-b9e9-9d8757289d6c.png)

**3.2. `Upsampling`** Se calcula la FFT de la imagen (con la frecuencia cero centrada), se añaden ceros al rededor de las frecuencias más altas (tanto positivas como negativas) hasta obtener el tamaño deseado y finalmente se calcula la FFT inversa.

![resampling_FFT2](https://user-images.githubusercontent.com/71833624/188718738-315774b8-ced9-4f0a-a6a6-08e139a0be77.png)
