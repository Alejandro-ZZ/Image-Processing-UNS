# Procesamiento Morfológico

Generación e implementación de kernels con diferentes tamaños ***'M'*** (*M* debe ser impar) para diferentes tipo de filtros.

## Filtros asimétricos (invariantes a la rotación de 90°)

### 1. Pasa-bajos 

    Todos kernel de este tipo de filtro debe normalizar sus coeficientes para que la suma de los mismos sea igual a la unidad.
    
#### 1.1. Box (cuadrado/plano)

#### 1.2. Circle (Circular)

#### 1.3. Bartlett

#### 1.4. Gaussian

---

### 2. Pasa-bajos
    La suma de los coeficientes que conformal el kernel de este tipo de filtro debe ser igual a cero.

#### 2.1. Laplaciano (3x3): 8 y 4 vecinos

