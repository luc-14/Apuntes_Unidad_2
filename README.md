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
La rotación gira un objeto alrededor de un punto pivote (por defecto, el origen del plano cartesiano) en un ángulo específico $\theta$. En matemáticas de graficación, los ángulos positivos generalmente representan una rotación en sentido antihorario.

Factor: Ángulo de rotación $\theta$.

Ecuaciones algebraicas (usando trigonometría):

$x' = x \cos(\theta) - y \sin(\theta)$

$y' = x \sin(\theta) + y \cos(\theta)$
# 2.1.4. Sesgado.
El sesgado es una transformación que distorsiona la forma de un objeto deslizando sus capas internas, como si empujaras la parte superior de una caja rectangular hasta convertirla en un paralelogramo. Matemáticamente, desplaza las coordenadas de un eje en función del valor de la coordenada del otro eje.

Sesgado en el eje $X$: La coordenada $x$ cambia dependiendo de $y$.

$x' = x + sh_x \cdot y$

$y' = y$

Sesgado en el eje $Y$: La coordenada $y$ cambia dependiendo de $x$.

$x' = x$

$y' = y + sh_y \cdot x$

# Transformaciones Adicionales
Además de las tres fundamentales, existen otras transformaciones importantes en el diseño y renderizado gráfico:

Reflexión (Espejo): Genera una imagen simétrica del objeto respecto a un eje (por ejemplo, invertir el signo de las coordenadas $X$ crea una reflexión respecto al eje $Y$).

Sesgo (Shear / Deformación): Distorsiona la forma de un objeto deslizando sus capas internas, convirtiendo, por ejemplo, un cuadrado en un paralelogramo.
