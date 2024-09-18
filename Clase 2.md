# Dinámica de Sistemas

La dinámica de sistemas es una rama de la ingeniería que se enfoca en modelar, analizar y controlar sistemas dinámicos, los cuales cambian su comportamiento en el tiempo. En esta clase, se explorarán conceptos clave relacionados con las ecuaciones diferenciales, transformadas y técnicas de análisis de sistemas dinámicos. Estas herramientas son fundamentales para comprender cómo los sistemas responden ante diferentes estímulos.

## 1. Introducción

En esta clase, cubriremos los conceptos básicos de derivadas parciales y transformada de Laplace, los cuales son esenciales para resolver ecuaciones diferenciales en el contexto de sistemas dinámicos. Asimismo, abordaremos un ejemplo de cómo trabajar con sistemas complejos utilizando matrices.

## 2. Definiciones

🔑 **Derivada parcial**: la derivada de una función con respecto a una variable, manteniendo las demás constantes.

> Las derivadas parciales se denotan como:  
> $$ \frac{\partial f}{\partial x} $$

🔑 **Transformada de Laplace**: herramienta que convierte ecuaciones diferenciales en ecuaciones algebraicas, facilitando su resolución en el dominio de la frecuencia.

> La transformada de Laplace de una función \( f(t) \) está definida como:  
> $$ L\{f(t)\} = \int_{0}^{\infty} f(t) e^{-st} dt $$

## 3. Teoría

### 3.1 Derivadas parciales
Las derivadas parciales son fundamentales para describir sistemas dinámicos cuando las variables dependen de más de un parámetro. A continuación se presentan algunas de las fórmulas clave.

💡 Ejemplo 1: Derivada parcial de una función \( f(x, t) \)
$$ \frac{\partial}{\partial t} f = \alpha \frac{\partial}{\partial x} f + \beta f(x) $$

### 3.2 Transformada de Laplace
La transformada de Laplace es una técnica importante para la solución de ecuaciones diferenciales. Es útil para sistemas lineales y puede simplificar problemas que involucran derivadas.

💡 Ejemplo 2: Si tenemos una función \( x(t) \), su transformada de Laplace es:
$$ X(s) = \int_{0}^{\infty} x(t) e^{-st} dt $$

### 3.3 Ecuaciones diferenciales con matrices
En sistemas más complejos, como los representados por varias ecuaciones diferenciales interconectadas, es común utilizar matrices para organizarlas.

💡 Ejemplo 3:
$$
A \cdot X(s) = B \cdot U(s) + C \cdot Y(s)
$$
Donde:
- \( A, B, C \) son matrices.
- \( X(s), U(s), Y(s) \) son vectores de las variables en el dominio de la frecuencia.

### 3.4 Eliminación de variables
En algunos casos, se deben eliminar variables para simplificar la resolución de las ecuaciones. Por ejemplo, se pueden reordenar las ecuaciones para expresar una variable en función de otras y resolver el sistema paso a paso.

💡 Ejemplo 4: Eliminación de variables en un sistema de ecuaciones
$$ X(s) = A(s) \cdot U(s) - B(s) \cdot Y(s) $$

## 4. Ejemplos

💡 Ejemplo 5:
Resuelve el siguiente sistema utilizando matrices:
\[
\begin{align*}
2s U & = A(s_1 + s_2)(s - 1) + B(s_3)(s - 3) \\
2s U & = A(s_1s_2 - 3s) + B(s_4s_5) + C(s_2 + 4)
\end{align*}
\]

### Solución:
\[
U(s) = A \left( s_1 - 2 \right) + B \left( s_3(s - 1) \right) + C \left( s(s_2) \right)
\]

## 5. Conclusiones

En esta clase hemos revisado las herramientas básicas para trabajar con sistemas dinámicos. Desde el cálculo de derivadas parciales hasta la aplicación de la transformada de Laplace, estas técnicas permiten abordar ecuaciones complejas de manera eficiente. En la próxima clase, profundizaremos en el análisis de sistemas de primer y segundo orden.

## 6. Referencias

- Ogata, K. *Ingeniería de Control Moderna*.
- Smith, C. A., & Corripio, A. B. *Control Automático de Procesos*.
