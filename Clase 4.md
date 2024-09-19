# Dinámica de Sistemas

En esta clase se estudia la dinámica de un sistema mecánico con dos masas, \(M_1\) y \(M_2\), conectadas a través de resortes con constantes \(K_1\), \(K_2\), y \(K_3\). El objetivo es formular y resolver las ecuaciones que gobiernan el movimiento de este sistema, considerando las fuerzas que actúan sobre las masas. Se parte del principio de que no existe fricción en el sistema y hay una fuerza externa aplicada a la masa \(M_1\).

## 1. Introducción

El análisis de sistemas mecánicos implica la aplicación de las leyes de Newton para describir cómo las masas interactúan con las fuerzas y los elementos elásticos (resortes). En este caso, se trata de un sistema compuesto por dos masas conectadas a través de resortes en un entorno sin fricción. Se presentarán las ecuaciones del sistema, se resolverán para los desplazamientos de las masas y se explorarán diferentes configuraciones de entrada y salida.

## 2. Definiciones

> 🔑 *Sistema mecánico*: Es un conjunto de elementos físicos que interactúan entre sí mediante fuerzas para producir un movimiento en respuesta a fuerzas aplicadas. En este caso, el sistema está compuesto por dos masas y tres resortes.

> 🔑 *Fuerza externa*: Una fuerza aplicada desde fuera del sistema, que en este ejemplo actúa sobre la masa \(M_1\).

> 🔑 *MISO*: Acrónimo de *Multiple Input Single Output*. Se refiere a sistemas con múltiples entradas y una única salida.

## 3. Modelado del Sistema Mecánico

### 3.1. Ecuaciones de Movimiento

Para describir el movimiento del sistema se utiliza la segunda ley de Newton. Consideramos que:

1. La fuerza neta que actúa sobre una masa es igual a la masa multiplicada por su aceleración.
2. Los resortes generan fuerzas que dependen de la diferencia de desplazamientos de las masas.

Las ecuaciones de movimiento para las masas \(M_1\) y \(M_2\) son las siguientes:

$$
M_1 \ddot{x}_1 = F - K_1 x_1 - K_2 (x_1 - x_2)
$$

$$
M_2 \ddot{x}_2 = - K_2 (x_2 - x_1) - K_3 x_2
$$

Donde:

- \(x_1\) y \(x_2\) son los desplazamientos de las masas \(M_1\) y \(M_2\), respectivamente.
- \(F\) es la fuerza externa aplicada a \(M_1\).
- \(K_1\), \(K_2\), y \(K_3\) son las constantes de los resortes.

### 3.2. Representación en Forma Matricial

Para facilitar la resolución del sistema, podemos expresar las ecuaciones en forma matricial. Definimos el vector de desplazamientos y aceleraciones como:

$$
\mathbf{x} = \begin{pmatrix}
x_1 \\
x_2
\end{pmatrix}
$$

$$
\mathbf{\ddot{x}} = \begin{pmatrix}
\ddot{x}_1 \\
\ddot{x}_2
\end{pmatrix}
$$

La representación en forma matricial de las ecuaciones de movimiento es:

$$
\mathbf{M} \mathbf{\ddot{x}} = \mathbf{F} - \mathbf{K} \mathbf{x}
$$

Donde:

$$
\mathbf{M} = \begin{pmatrix}
M_1 & 0 \\
0 & M_2
\end{pmatrix}
$$

$$
\mathbf{F} = \begin{pmatrix}
F \\
0
\end{pmatrix}
$$

$$
\mathbf{K} = \begin{pmatrix}
K_1 + K_2 & -K_2 \\
-K_2 & K_2 + K_3
\end{pmatrix}
$$

Entonces, la ecuación matricial es:

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
F - (K_1 + K_2)x_1 + K_2 x_2 \\
-K_2 x_1 - (K_2 + K_3)x_2
\end{pmatrix}
$$

Esta representación es útil para implementar el sistema en un programa o resolverlo numéricamente.

## 4. Ejemplo Resuelto

💡 **Ejemplo 1:** Resolución del sistema de ecuaciones para un caso particular donde:

- \( M_1 = 1 \, \text{kg} \)
- \( M_2 = 2 \, \text{kg} \)
- \( K_1 = 3 \, \text{N/m} \)
- \( K_2 = 2 \, \text{N/m} \)
- \( K_3 = 1 \, \text{N/m} \)
- \( F = 10 \, \text{N} \)

Sustituyendo estos valores en las ecuaciones, obtenemos:

Para la masa \(M_1\):

$$
1 \ddot{x}_1 = 10 - 3 x_1 - 2 (x_1 - x_2)
$$

Simplificando:

$$
\ddot{x}_1 = 10 - 5x_1 + 2x_2
$$

Para la masa \(M_2\):

$$
2 \ddot{x}_2 = - 2 (x_2 - x_1) - 1 x_2
$$

Simplificando:

$$
2 \ddot{x}_2 = -3x_2 + 2x_1
$$

### 4.1. Sistema Completo

El sistema de ecuaciones es:

$$
\ddot{x}_1 = 10 - 5x_1 + 2x_2
$$

$$
\ddot{x}_2 = -\frac{3}{2}x_2 + x_1
$$

Este sistema puede ser resuelto numéricamente para obtener los desplazamientos \(x_1(t)\) y \(x_2(t)\) a lo largo del tiempo.

## 5. Conclusiones

En esta clase hemos modelado un sistema mecánico de dos masas conectadas por resortes. Hemos deducido las ecuaciones de movimiento tanto de forma directa como en forma matricial. Este tipo de sistemas son comunes en el estudio de la dinámica de sistemas físicos y pueden resolverse mediante métodos numéricos para obtener las trayectorias de las masas.

## 6. Referencias

- Ogata, K. (1997). *Ingeniería de Control Moderna*. Prentice Hall.
- Dorf, R. C., & Bishop, R. H. (2010). *Sistemas de Control Moderno*. Pearson.
