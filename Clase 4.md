# Dinámica de Sistemas Mecánicos

Este documento trata sobre el análisis de un sistema mecánico compuesto por dos masas conectadas a resortes, considerando la dinámica de este sistema bajo la aplicación de una fuerza externa a una de las masas. El objetivo es modelar el sistema con ecuaciones de movimiento y resolver el sistema de ecuaciones. En este caso, no existe fricción en el sistema, y se aplica una fuerza externa \( F \) sobre la masa \( M_1 \).

## 1. Modelo del Sistema

Se trata de un sistema de dos grados de libertad (DOF) con masas conectadas por resortes. La masa \( M_1 \) está sujeta a una fuerza externa \( F \), y ambas masas están conectadas a resortes con constantes \( K_1 \), \( K_2 \), y \( K_3 \). El sistema no tiene fricción. Las posiciones de las masas están dadas por \( x_1 \) para \( M_1 \) y \( x_2 \) para \( M_2 \).

## 2. Definiciones

> 🔑 *Sistema de masas*: Es un conjunto de masas conectadas entre sí mediante elementos elásticos (resortes) o amortiguadores que pueden ser modeladas mediante ecuaciones diferenciales.
>
> 🔑 *Resorte*: Es un elemento elástico cuya fuerza es proporcional al desplazamiento, descrita por la ley de Hooke \( F = -kx \).

## 3. Ecuaciones del Sistema

### 3.1. Ecuaciones de movimiento

Al aplicar la segunda ley de Newton a cada una de las masas, obtenemos las siguientes ecuaciones:

Para \( M_1 \), considerando la fuerza externa \( F \), la constante del resorte \( K_1 \), y el resorte entre las masas con constante \( K_2 \):

$$
M_1 \ddot{x}_1 = F - K_1 x_1 - K_2 (x_1 - x_2)
$$

Para \( M_2 \), considerando la fuerza del resorte con constante \( K_2 \) y el resorte con constante \( K_3 \):

$$
M_2 \ddot{x}_2 = -K_2 (x_2 - x_1) - K_3 x_2
$$

Estas ecuaciones son las ecuaciones diferenciales que describen el movimiento del sistema.

### 3.2. Resolución del sistema

Si queremos resolver estas ecuaciones, podemos organizarlas en forma matricial de la siguiente manera:

$$
\begin{pmatrix}
M_1 & 0 \\
0 & M_2
\end{pmatrix}
\begin{pmatrix}
\ddot{x}_1 \\
\ddot{x}_2
\end{pmatrix}
=
\begin{pmatrix}
F - K_1 x_1 - K_2 (x_1 - x_2) \\
-K_2 (x_2 - x_1) - K_3 x_2
\end{pmatrix}
$$

Esta es la forma matricial del sistema de ecuaciones diferenciales.

## 4. Solución del sistema

Para resolver el sistema de ecuaciones diferenciales, es necesario utilizar métodos numéricos o aplicar la transformada de Laplace. Aquí, usaremos la transformada de Laplace para resolver las ecuaciones en el dominio de la frecuencia.

### 4.1. Aplicando la transformada de Laplace

Tomamos la transformada de Laplace de ambas ecuaciones suponiendo condiciones iniciales \( x_1(0) = 0 \) y \( x_2(0) = 0 \):

Para \( M_1 \):

$$
M_1 s^2 X_1(s) = F(s) - K_1 X_1(s) - K_2 (X_1(s) - X_2(s))
$$

Para \( M_2 \):

$$
M_2 s^2 X_2(s) = -K_2 (X_2(s) - X_1(s)) - K_3 X_2(s)
$$

### 4.2. Resolviendo en el dominio de Laplace

Reordenamos ambas ecuaciones para resolverlas simultáneamente:

Para \( X_1(s) \):

$$
(M_1 s^2 + K_1 + K_2) X_1(s) - K_2 X_2(s) = F(s)
$$

Para \( X_2(s) \):

$$
-K_2 X_1(s) + (M_2 s^2 + K_2 + K_3) X_2(s) = 0
$$

Estas dos ecuaciones pueden resolverse algebraicamente para obtener \( X_1(s) \) y \( X_2(s) \), y luego se aplica la transformada inversa de Laplace para obtener las soluciones en el dominio del tiempo \( x_1(t) \) y \( x_2(t) \).

## 5. Conclusiones

En este análisis, hemos modelado un sistema mecánico compuesto por dos masas conectadas mediante resortes sin fricción, y bajo la acción de una fuerza externa. Las ecuaciones diferenciales obtenidas describen el movimiento de las masas en función del tiempo, y la resolución mediante la transformada de Laplace permite analizar el comportamiento del sistema en el dominio de la frecuencia.

Este tipo de modelado es fundamental en la dinámica de sistemas, ya que permite predecir el comportamiento de sistemas mecánicos complejos en diferentes condiciones. Para resolver estas ecuaciones en la práctica, a menudo se recurre a herramientas computacionales como MATLAB o Python.

## 6. Referencias

- Sistemas mecánicos: ecuaciones de movimiento. (n.d.). Recuperado de [sitio web académico].
- Dorf, R. C., & Bishop, R. H. (2011). *Sistemas de control moderno*. Pearson.
- Ogata, K. (2010). *Ingeniería de control moderno*. Prentice Hall.
