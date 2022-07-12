# Procesamiento Morfológico

Desarrollo de métodos en python que permitan procesar funciones morfológicas para imagenes en escala de grises o RGB, con elementos estructurantes (SE) cuadrados y circulares.

## Elementos estructurantes (SE)

Kernel convolucionales con coeficientes de tipo **bool** con dos formas:

1. Cuadrado (Box)
2. Circular (Disk)

## Operaciones básicas (Nivel 1)

### 1. Dilatación (Dilation)
![dilatacion](https://user-images.githubusercontent.com/71833624/178403723-80b6fdb0-2fc4-40b3-994e-359690e6eeba.png)

### 2. Erosión (Erosion)
![erosion](https://user-images.githubusercontent.com/71833624/178403674-348f0e08-88be-43a1-9638-b0444d8ccdaa.png)

### 3. Filtro mediana (Median)
![filtro_mediana](https://user-images.githubusercontent.com/71833624/178403741-883314c3-bf01-4aa7-a6fa-9a34c922b9ce.png)

## Operaciones entre erosión y dilatación

1. Borde externo (Outer edges)
2. Borde interno (Inner edges)
3. Gradiente (Gradient)

![nivel2_1](https://user-images.githubusercontent.com/71833624/178404493-2425ea22-9cb1-421d-bcd3-a0064b6895a0.png)

![nivel2_2](https://user-images.githubusercontent.com/71833624/178404517-7b125353-14d7-44ba-b260-1bc8c09b9935.png)

## Concatenado de erosión y dilatación (Nivel 2)

1. Apertura (Opening)
2. Cierre (Closing)

![apertura_cierre](https://user-images.githubusercontent.com/71833624/178404566-a0eaa5f1-6458-47f4-a179-9f15ec741eef.png)

3. Top-Hat (White top-hat)
4. Bottom-Hat (Black top-hat)

![top_hat](https://user-images.githubusercontent.com/71833624/178404571-30f0d5aa-d541-4b23-80a7-9bf8ea2a5b84.png)

## Concatenado de cierre y apertura

1. OC (Opening-Closing)
2. CO (Closing-Opening)

## Funciones con operaciones morfológicas

1. Suavizado (Smoothing)

![smoothing_disk](https://user-images.githubusercontent.com/71833624/178404593-77c0ac84-5c1e-428a-b59e-c6659e734da8.png)

2. Realce de contraste (edge enhance)

![realce1](https://user-images.githubusercontent.com/71833624/178404849-770129c7-ef91-4682-8db2-05e99e9d24a6.png)

## Algunas aplicaciones

### 1. Extracción de texto

![text_extraction](https://user-images.githubusercontent.com/71833624/178132291-24575d98-c839-4abd-8db8-97c0ecb535e8.png)

### 2. Eliminación de texto

![text_elimination](https://user-images.githubusercontent.com/71833624/178132296-1318d632-ef59-400b-aafc-e6ec14323f92.png)

### 3. Análisis de retina

![retina_extraction](https://user-images.githubusercontent.com/71833624/178132305-ba878d08-10f0-4e9f-bbae-f60cf458e938.png)
