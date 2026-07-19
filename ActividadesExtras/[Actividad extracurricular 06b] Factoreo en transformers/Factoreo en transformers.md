# Escuela Politécnica Nacional
## Métodos Numéricos
#### Erick Cuichán 
#### Actividad extracurricular 06b - Factoreo en transformers


#### link repositorio: [Actividad extracurricular 6b]()
---



Los Transformers son una arquitectura de redes neuronales ampliamente utilizada en tareas de procesamiento de lenguaje natural, visión por computadora y modelos generativos.

Su funcionamiento se basa principalmente en operaciones matriciales de gran escala, especialmente dentro del mecanismo de autoatención. Debido al alto costo computacional que implican estas operaciones, el factoreo de matrices se ha convertido en una técnica importante para mejorar la eficiencia de los modelos sin afectar significativamente su desempeño.

---

## ¿Qué es el factoreo de matrices?

El factoreo de matrices consiste en descomponer una matriz grande en el producto de dos o más matrices de menor dimensión.

Matemáticamente, una matriz de pesos \(W\), de tamaño \(m \times n\), puede aproximarse como:

$$
W \approx A \cdot B
$$

donde:

$$
W \in \mathbb{R}^{m \times n}
$$

$$
A \in \mathbb{R}^{m \times k}
$$

$$
B \in \mathbb{R}^{k \times n}
$$

y el valor \(k\) cumple:

$$
k \ll \min(m,n)
$$

Esto significa que \(k\) es mucho menor que \(m\) y \(n\). De esta manera, la transformación lineal puede representarse utilizando menos parámetros y menos operaciones computacionales.

---

## Uso del factoreo en la arquitectura Transformer

- Factoreo en las proyecciones lineales

En la arquitectura Transformer se utilizan matrices asociadas a las operaciones de **Query**, **Key** y **Value**.

Estas matrices suelen ser de gran tamaño. Al aplicar factoreo, pueden representarse mediante matrices más pequeñas, reduciendo el número de parámetros y operaciones necesarias durante el cálculo de la atención.

- Atención de bajo rango

El mecanismo de atención estándar presenta una complejidad cuadrática con respecto al tamaño de la secuencia.

Mediante aproximaciones de bajo rango es posible reducir parte de este costo computacional, lo cual resulta especialmente útil cuando se trabaja con secuencias largas.

- Compresión del modelo

El factoreo de matrices también se utiliza como una técnica de compresión.

Al reemplazar matrices grandes por matrices de menor dimensión, se reduce el tamaño total del modelo y se facilita su ejecución en equipos con recursos computacionales limitados.

## Razones para aplicar factoreo de matrices en Transformers

- Reducción del costo computacional

Al reemplazar una multiplicación matricial grande por operaciones con matrices más pequeñas, se disminuye el número total de cálculos necesarios.

-  Menor uso de memoria

El almacenamiento de matrices de menor dimensión reduce el consumo de memoria RAM y VRAM, lo cual es especialmente importante en modelos de gran tamaño.

-  Mejor escalabilidad

El factoreo permite entrenar y ejecutar modelos Transformer más grandes, profundos o capaces de procesar secuencias más largas sin aumentar excesivamente el costo computacional.

- Mayor facilidad de implementación

Las matrices reducidas permiten adaptar modelos grandes a computadoras con menos recursos, facilitando su uso en distintos entornos.

## Ventajas del factoreo en Transformers

- Disminuye el número de parámetros del modelo.
- Reduce el consumo de memoria.
- Puede acelerar el entrenamiento y la inferencia.
- Facilita la compresión del modelo.
- Permite trabajar con secuencias más largas.
- Favorece el despliegue en hardware con recursos limitados.

## En Conclusión

El factoreo de matrices es una técnica importante dentro de la arquitectura Transformer porque permite representar matrices grandes mediante matrices más pequeñas.

Gracias a esta operación es posible reducir el número de parámetros, disminuir el consumo de memoria y mejorar la eficiencia computacional.

Por esta razón, el factoreo es especialmente útil en mPodelos modernos de inteligencia artificial, donde las matrices utilizadas pueden alcanzar dimensiones muy grandes.