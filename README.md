# Apuntes_Unidad_2
# Unidad 2 Graficación2D.

# 2.1. Transformación bidimensional.
En la graficación por computadora, una transformación bidimensional (2D) es una operación matemática que altera la posición, tamaño, orientación o forma de un objeto geométrico dentro de un plano cartesiano de dos dimensiones ($x$, $y$).

Estas transformaciones se aplican a los vértices que componen un objeto (por ejemplo, puntos, líneas o polígonos) para generar una nueva vista o posición en la pantalla sin tener que redibujar el objeto desde cero. Matemáticamente, el manejo eficiente de estas transformaciones requiere el uso de álgebra lineal, específicamente de vectores y matrices.Para poder combinar múltiples transformaciones (como rotar un objeto y luego moverlo) mediante una simple multiplicación de matrices, se utiliza un concepto matemático llamado coordenadas homogéneas. 
# 2.1.1. Traslación.
La traslación consiste en mover un objeto de una posición a otra en el plano, sumando distancias a las coordenadas originales a lo largo de los ejes $X$ e $Y$.

Factores:
$T_x$ (desplazamiento en $X$) y $T_y$ (desplazamiento en $Y$).

Ecuaciones algebraicas:

$x' = x + T_x$

$y' = y + T_y$
# 2.1.2. Escalamiento.
El escalamiento cambia el tamaño de un objeto. Se logra multiplicando las coordenadas de cada vértice por factores de escala. Si el factor es mayor a 1, el objeto crece; si está entre 0 y 1, se encoge. Si los factores en $X$ e $Y$ son diferentes, el objeto se deforma (escalamiento diferencial).
Factores: 
$S_x$ (escala en $X$) y $S_y$ (escala en $Y$).

Ecuaciones algebraicas:

$x' = x \cdot S_x$

$y' = y \cdot S_y$
# 2.1.3. Rotación.

# 2.1.4. Sesgado.
