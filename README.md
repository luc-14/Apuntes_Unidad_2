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

# 2.2.Representación matricial de las transformaciones bidimensionales.
Ejercicio Práctico: Control con Teclas de Dirección

La representación matricial es la base matemática para la interactividad en el software. Para implementar un objeto controlado por las flechas del teclado:

1. Se define una variable de estado para la posición del objeto (por ejemplo, una matriz de vértices).
2. Se configura un "Listener" (escuchador de eventos) en el entorno de desarrollo que detecte la pulsación de teclas.
3. Al presionar una tecla (ej. Flecha Derecha), se construye una matriz de traslación donde $T_x = \text{velocidad}$ y $T_y = 0$.
4. Se multiplica la matriz de los vértices del objeto por esta matriz de traslación y se invoca la función de repintado (repaint(), update(), etc.) para actualizar la pantalla, creando la ilusión de movimiento.
# 2.3. Trazo de líneas curvas.
En graficación, las curvas no se dibujan pixel por pixel de forma manual, sino que se generan algorítmicamente mediante ecuaciones paramétricas. Se utilizan "puntos de control" para influir en la forma de la curva, evaluando un parámetro $t$ que va de $0$ a $1$.
# 2.3.1. Bézier.
Desarrolladas por Pierre Bézier para el diseño automotriz, estas curvas interpolan entre un conjunto de puntos de control. La curva siempre pasa por el primer y último punto de control, mientras que los puntos intermedios actúan como "imanes" que tiran de la curva hacia ellos.La ecuación para una curva de Bézier cúbica (4 puntos de control: $P_0, P_1, P_2, P_3$), basada en los polinomios de Bernstein, es:

$$P(t) = (1-t)^3 P_0 + 3t(1-t)^2 P_1 + 3t^2(1-t) P_2 + t^3 P_3$$

(Donde $0 \le t \le 1$).

Si modificas un solo punto de control, toda la curva cambia de forma (control global).
# 2.3.2. B-spline.
(colocar el ejercicio dibujo de la animación)

# 2.4. Fractales

# 2.5. Uso y creación de fuentes de texto.
