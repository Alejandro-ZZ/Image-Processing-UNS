# TP1: Introducción, espacios cromáticos y manipulación de luminancia y saturación

## *1-1_Management_methods.ipynb*

Desarrollo de ejemplos básicos de manipulación de imágenes con la libreria PIL y mediante operaciones en la imagen como matriz.

* Lectura de una imagen.
* Extracción de atributos de una imagen.
* Gráfica de una imagen.
* Modificación de una imagen: cortar, cambiar resolución, extraer canales, cuantificación y rotación.
* Exportar imagen como archivo en una ruta específica.
* Análisis de píxeles: muestreo horizontal.
* Manipulación de imagen como matriz.

## 1-2_Luminance_Saturation.ipynb

* Conversión de una imagen en el espacio RGB y YIQ.
* Manipulación de la luminancia y saturación de una imagen por medio del espacio YIQ.
* Implementación de mapas cromáticos en imágenes.


###  Espacio YIQ

* **Luminancia (canal Y, 80% de importancia):** brillo del estímulo cromático. Combinación ponderada de la energía de la componente acromática y cromática.

* **Saturación (canal I, 15% de la varianza):** pureza del color. Relación entre la energía de las componentes cromáticas y acromáticas.

* **Crominancia (canal Q, 5% de la varianza):** longitud de onda dominante que define el color propio del estímulo (gama de rojos, amarillos, verdes, etc).


**Matrices de conversión entre el espacio RGB y YIQ**

<img src="https://user-images.githubusercontent.com/71833624/165201459-a611bdd4-f881-47f6-a045-0f0441756dab.png" width="600"/>
</div>
