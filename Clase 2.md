# Dinámica de Sistemas

La dinámica de sistemas es una rama de la ingeniería que se enfoca en modelar, analizar y controlar sistemas dinámicos, los cuales cambian su comportamiento en el tiempo. En esta clase, se explorarán conceptos clave relacionados con las ecuaciones diferenciales, transformadas y técnicas de análisis de sistemas dinámicos. Estas herramientas son fundamentales para comprender cómo los sistemas responden ante diferentes estímulos.

## 1. Introducción

En esta clase, cubriremos los conceptos básicos de derivadas parciales y transformada de Laplace, los cuales son esenciales para resolver ecuaciones diferenciales en el contexto de sistemas dinámicos. Asimismo, abordaremos un ejemplo de cómo trabajar con sistemas complejos utilizando matrices.

## 2. Definiciones

🔑 **Derivada parcial**: La derivada de una función con respecto a una variable, manteniendo las demás constantes.

> Las derivadas parciales se denotan como:
> 
> `∂f / ∂x`

🔑 **Transformada de Laplace**: Herramienta que convierte ecuaciones diferenciales en ecuaciones algebraicas, facilitando su resolución en el dominio de la frecuencia.

> La transformada de Laplace de una función `f(t)` está definida como:  
> 
> `L{f(t)} = ∫(0, ∞) f(t) e^(-st) dt`

## 3. Teoría

### 3.1 Derivadas parciales
Las derivadas parciales son fundamentales para describir sistemas dinámicos cuando las variables dependen de más de un parámetro. A continuación se presentan algunas de las fórmulas clave.

💡 **Ejemplo 1**: Derivada parcial de una función `f(x, t)`

`∂f / ∂t = α (∂f / ∂x) + β f(x)`

### 3.2 Transformada de Laplace
La transformada de Laplace es una técnica importante para la solución de ecuaciones diferenciales. Es útil para sistemas lineales y puede simplificar problemas que involucran derivadas.

💡 **Ejemplo 2**: Si tenemos una función `x(t)`, su transformada de Laplace es:

`X(s) = ∫(0, ∞) x(t) e^(-st) dt`

### 3.3 Ecuaciones diferenciales con matrices
En sistemas más complejos, como los representados por varias ecuaciones diferenciales interconectadas, es común utilizar matrices para organizarlas.

💡 **Ejemplo 3**:

`A * X(s) = B * U(s) + C * Y(s)`

Donde:
- `A`, `B`, `C` son matrices.
- `X(s)`, `U(s)`, `Y(s)` son vectores de las variables en el dominio de la frecuencia.

### 3.4 Eliminación de variables
En algunos casos, se deben eliminar variables para simplificar la resolución de las ecuaciones. Por ejemplo, se pueden reordenar las ecuaciones para expresar una variable en función de otras y resolver el sistema paso a paso.

💡 **Ejemplo 4**: Eliminación de variables en un sistema de ecuaciones

`X(s) = A(s) * U(s) - B(s) * Y(s)`

## 4. Ejemplos

### Solución de la Ecuación usando Fracciones Parciales y Transformada de Laplace

Dada la función de transferencia:

`(2s^2 - 4) / ((s + 1)(s - 2)(s - 3))`

### 1. Descomposición en Fracciones Parciales

Primero, descomponemos la función en fracciones parciales. Supongamos que:

`(2s^2 - 4) / ((s + 1)(s - 2)(s - 3)) = A / (s + 1) + B / (s - 2) + C / (s - 3)`

Multiplicamos ambos lados por el denominador común `(s + 1)(s - 2)(s - 3)` para obtener:

`2s^2 - 4 = A(s - 2)(s - 3) + B(s + 1)(s - 3) + C(s + 1)(s - 2)`

Expandimos y agrupamos términos:

`2s^2 - 4 = A(s^2 - 5s + 6) + B(s^2 - 2s - 3) + C(s^2 - s - 2)`

Agrupamos términos similares:

`2s^2 - 4 = (A + B + C)s^2 + (-5A - 2B - C)s + (6A - 3B - 2C)`

Comparando los coeficientes con `2s^2 - 4`:

1. Coeficiente de `s^2`:

    `A + B + C = 2`

2. Coeficiente de `s`:

    `-5A - 2B - C = 0`

3. Término constante:

    `6A - 3B - 2C = -4`

Resolvemos este sistema de ecuaciones:

De `A + B + C = 2`:

    `C = 2 - A - B`

Sustituyendo en las otras dos ecuaciones:

`-5A - 2B - (2 - A - B) = 0`

`-5A - 2B - 2 + A + B = 0`

`-4A - B = 2`

Y:

`6A - 3B - 2(2 - A - B) = -4`

`6A - 3B - 4 + 2A + 2B = -4`

`8A - B = 0`

Resolviendo el sistema:

De `8A - B = 0`:

    `B = 8A`

Sustituyendo en `-4A - B = 2`:

    `-4A - 8A = 2`

    `-12A = 2`

    `A = -1/6`

    `B = 8A = -4/3`

Y:

    `C = 2 - A - B`

    `C = 2 - (-1/6) - (-4/3)`

    `C = 2 + 1/6 + 4/3`

    `C = 2 + (1 + 8) / 6`

    `C = 2 + 3/2 = 7/2`

Por lo tanto:

    `A = -1/6`
    `B = -4/3`
    `C = 7/2`

### 2. Transformada Inversa de Laplace

La descomposición en fracciones parciales es:

`(2s^2 - 4) / ((s + 1)(s - 2)(s - 3)) = (-1/6) / (s + 1) + (-4/3) / (s - 2) + (7/2) / (s - 3)`

Tomamos la transformada inversa de Laplace:

`L^-1{(-1/6) / (s + 1)} = -1/6 * e^(-t)`

`L^-1{(-4/3) / (s - 2)} = -4/3 * e^(2t)`

`L^-1{(7/2) / (s - 3)} = 7/2 * e^(3t)`

Por lo tanto, la solución en el dominio del tiempo es:

`y(t) = -1/6 * e^(-t) - 4/3 * e^(2t) + 7/2 * e^(3t)`

## 5. Conclusiones

En esta clase hemos revisado las herramientas básicas para trabajar con sistemas dinámicos. Desde el cálculo de derivadas parciales hasta la aplicación de la transformada de Laplace, estas técnicas permiten abordar ecuaciones complejas de manera eficiente. En la próxima clase, profundizaremos en el análisis de sistemas de primer y segundo orden.

## 6. Referencias

- Ogata, K. *Ingeniería de Control Moderna*.
- Smith, C. A., & Corripio, A. B. *Control Automático de Procesos*.
