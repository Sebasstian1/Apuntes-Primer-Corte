# Dinámica de Sistemas

La dinámica de sistemas es una rama de la ingeniería que se enfoca en modelar, analizar y controlar sistemas dinámicos, los cuales cambian su comportamiento en el tiempo. En esta clase, se explorarán conceptos clave relacionados con las ecuaciones diferenciales, transformadas y técnicas de análisis de sistemas dinámicos. Estas herramientas son fundamentales para comprender cómo los sistemas responden ante diferentes estímulos.

## 1. Introducción

En esta clase, cubriremos los conceptos básicos de derivadas parciales y transformada de Laplace, los cuales son esenciales para resolver ecuaciones diferenciales en el contexto de sistemas dinámicos. Asimismo, abordaremos un ejemplo de cómo trabajar con sistemas complejos utilizando matrices.

## 2. Definiciones

🔑 **Derivada parcial**: La derivada de una función con respecto a una variable, manteniendo las demás constantes.

> Las derivadas parciales se denotan como:  
> `∂f / ∂x`

🔑 **Transformada de Laplace**: Herramienta que convierte ecuaciones diferenciales en ecuaciones algebraicas, facilitando su resolución en el dominio de la frecuencia.

> La transformada de Laplace de una función `f(t)` está definida como:  
> `L{f(t)} = ∫(0, ∞) f(t) e^(-st) dt`

## 3. Teoría

### 3.1 Derivadas parciales
Las derivadas parciales son fundamentales para describir sistemas dinámicos cuando las variables dependen de más de un parámetro. A continuación se presentan algunas de las fórmulas clave.

💡 **Ejemplo 1**: Derivada parcial de una función `f(x, t)`

$$ \frac{\partial f}{\partial t} = \alpha \frac{\partial f}{\partial x} + \beta f(x) $$

### 3.2 Transformada de Laplace
La transformada de Laplace es una técnica importante para la solución de ecuaciones diferenciales. Es útil para sistemas lineales y puede simplificar problemas que involucran derivadas.

💡 **Ejemplo 2**: Si tenemos una función `x(t)`, su transformada de Laplace es:

$$ X(s) = \int_{0}^{\infty} x(t) e^{-st} \, dt $$

### 3.3 Ecuaciones diferenciales con matrices
En sistemas más complejos, como los representados por varias ecuaciones diferenciales interconectadas, es común utilizar matrices para organizarlas.

💡 **Ejemplo 3**:

$$ A \cdot X(s) = B \cdot U(s) + C \cdot Y(s) $$

Donde:
- `A`, `B`, `C` son matrices.
- `X(s)`, `U(s)`, `Y(s)` son vectores de las variables en el dominio de la frecuencia.

### 3.4 Eliminación de variables
En algunos casos, se deben eliminar variables para simplificar la resolución de las ecuaciones. Por ejemplo, se pueden reordenar las ecuaciones para expresar una variable en función de otras y resolver el sistema paso a paso.

💡 **Ejemplo 4**: Eliminación de variables en un sistema de ecuaciones

$$ X(s) = A(s) \cdot U(s) - B(s) \cdot Y(s) $$

## 4. Ejemplos

### Solución de la Ecuación usando Fracciones Parciales y Transformada de Laplace

Dada la función de transferencia:

$$ \frac{2s^2 - 4}{(s + 1)(s - 2)(s - 3)} $$

### 1. Descomposición en Fracciones Parciales

Primero, descomponemos la función en fracciones parciales. Supongamos que:

$$ \frac{2s^2 - 4}{(s + 1)(s - 2)(s - 3)} = \frac{A}{s + 1} + \frac{B}{s - 2} + \frac{C}{s - 3} $$

Multiplicamos ambos lados por el denominador común \((s + 1)(s - 2)(s - 3)\) para obtener:

$$ 2s^2 - 4 = A(s - 2)(s - 3) + B(s + 1)(s - 3) + C(s + 1)(s - 2) $$

Expandimos y agrupamos términos:

$$ 2s^2 - 4 = A(s^2 - 5s + 6) + B(s^2 - 2s - 3) + C(s^2 - s - 2) $$

Agrupamos términos similares:

$$ 2s^2 - 4 = (A + B + C)s^2 + (-5A - 2B - C)s + (6A - 3B - 2C) $$

Comparando los coeficientes con \(2s^2 - 4\):

1. **Coeficiente de \(s^2\)**:

   A + B + C = 2 

2. **Coeficiente de \(s\)**:

   -5A - 2B - C = 0 

3. **Término constante**:

   6A - 3B - 2C = -4 

Resolvemos este sistema de ecuaciones:

  $$ \(A + B + C = 2\) $$

$$ C = 2 - A - B $$

Sustituyendo en las otras dos ecuaciones:

- Para el coeficiente de \(s\):

   $$ -5A - 2B - (2 - A - B) = 0 $$
   $$ -5A - 2B - 2 + A + B = 0 $$
   $$ -4A - B = 2 $$

- Para el término constante:

   $$ 6A - 3B - 2(2 - A - B) = -4 $$
   $$ 6A - 3B - 4 + 2A + 2B = -4 $$
   $$ 8A - B = 0 $$

Resolviendo el sistema:

De \(8A - B = 0\):

$$ B = 8A $$

Sustituyendo en \(-4A - B = 2\):

$$ -4A - 8A = 2 $$
$$ -12A = 2 $$
$$ A = -\frac{1}{6} $$

$$ B = 8A = -\frac{4}{3} $$

Y:

$$ C = 2 - A - B $$
$$ C = 2 - \left(-\frac{1}{6}\right) - \left(-\frac{4}{3}\right) $$
$$ C = 2 + \frac{1}{6} + \frac{4}{3} $$
$$ C = 2 + \frac{1 + 8}{6} $$
$$ C = 2 + \frac{3}{2} = \frac{7}{2} $$

Por lo tanto:

$$ A = -\frac{1}{6} $$
$$ B = -\frac{4}{3} $$
$$ C = \frac{7}{2} $$

### 2. Transformada Inversa de Laplace

La descomposición en fracciones parciales es:

$$ \frac{2s^2 - 4}{(s + 1)(s - 2)(s - 3)} = \frac{-\frac{1}{6}}{s + 1} + \frac{-\frac{4}{3}}{s - 2} + \frac{\frac{7}{2}}{s - 3} $$

Tomamos la transformada inversa de Laplace:

$$ L^{-1} \left( \frac{-\frac{1}{6}}{s + 1} \right) = -\frac{1}{6} e^{-t} $$

$$ L^{-1} \left( \frac{-\frac{4}{3}}{s - 2} \right) = -\frac{4}{3} e^{2t} $$

$$ L^{-1} \left( \frac{\frac{7}{2}}{s - 3} \right) = \frac{7}{2} e^{3t} $$

Por lo tanto, la solución en el dominio del tiempo es:

$$ y(t) = -\frac{1}{6} e^{-t} - \frac{4}{3} e^{2t} + \frac{7}{2} e^{3t} $$

## 5. Herramientas en MATLAB

### 5.1 MATLAB
MATLAB es un entorno de programación y un lenguaje de alto nivel utilizado para el análisis numérico, la visualización de datos y el desarrollo de algoritmos. Es ampliamente utilizado en ingeniería y ciencias para realizar cálculos matemáticos complejos y visualizar resultados.

**Introducción a MATLAB**:

MATLAB proporciona una serie de funciones y herramientas para realizar cálculos matemáticos, manipular datos, y crear gráficos. Su sintaxis y entorno permiten a los usuarios desarrollar scripts y funciones que simplifican el análisis y la resolución de problemas complejos.


### 5.2 Simulink
Simulink es una plataforma de simulación y diseño de sistemas en MATLAB. Permite modelar, simular y analizar sistemas dinámicos utilizando diagramas de bloques. Es útil para visualizar la interacción de diferentes componentes de un sistema y para realizar análisis de respuesta en el dominio del tiempo y de la frecuencia.

Introducción a Simulink:

Simulink proporciona un entorno gráfico basado en bloques donde puedes arrastrar y soltar componentes para construir modelos de sistemas. Cada bloque representa un componente o una operación matemática, y las conexiones entre bloques representan las señales que fluyen a través del sistema. Esto permite a los ingenieros y científicos diseñar y probar sistemas complejos de manera intuitiva.

Ejemplo:

Para modelar un sistema en Simulink, creamos un modelo utilizando bloques que representan diferentes componentes del sistema (por ejemplo, sumadores, integradores, etc.) y conectamos estos bloques para formar un diagrama de flujo de señales. Luego, ejecutamos la simulación y analizamos los resultados.

## 6. Conclusiones
En la dinámica de sistemas, la comprensión de derivadas parciales, la transformada de Laplace, y el uso de herramientas como MATLAB y Simulink son fundamentales para el análisis y diseño de sistemas dinámicos. Estos conceptos y herramientas permiten modelar, simular y controlar sistemas complejos de manera efectiva, facilitando la resolución de problemas y la optimización de sistemas en diversas aplicaciones de ingeniería.
