# Dinámica de Sistemas

El curso de Dinámica de Sistemas está enfocado en el estudio de la solución de ecuaciones diferenciales aplicadas a sistemas dinámicos de distintos dominios como la mecánica, la electricidad, la hidráulica y la térmica. Se trabajará con software como MATLAB y simuladores de circuitos para modelar y analizar sistemas de primer y segundo orden, y sus respectivas respuestas en el tiempo.

## 1. Definiciones
> 🔑 _Ecuaciones diferenciales_: Son ecuaciones que relacionan una o más funciones con sus derivadas. En el contexto de dinámica de sistemas, estas ecuaciones modelan el comportamiento de sistemas dinámicos.
> 
> 🔑 _Transformada de Laplace_: Es una técnica matemática que transforma una función del dominio del tiempo en una función en el dominio de la frecuencia, facilitando la resolución de ecuaciones diferenciales.
> 
> 🔑 _Modelamiento Matemático_: Es la representación de un sistema real mediante ecuaciones matemáticas que describen su comportamiento dinámico.

## 2. Subtítulos
### 2.1 Solución de Ecuaciones Diferenciales
La solución de ecuaciones diferenciales es fundamental en el estudio de sistemas dinámicos. En este curso se hará uso de la transformada de Laplace para simplificar el proceso de solución, especialmente cuando se estudian sistemas complejos.

### 2.2 Modelamiento Matemático
El modelamiento matemático de sistemas dinámicos involucra varios dominios como:
- **Mecánica**: Modelado de sistemas físicos como masas, resortes y amortiguadores.
- **Eléctrica**: Modelado de circuitos eléctricos usando resistencias, inductancias y capacitores.
- **Hidráulica**: Modelado de sistemas de fluidos y presión.
- **Térmica**: Modelado de transferencia de calor.
- **Combinaciones**: Sistemas que involucran la interacción de varios dominios.

### 2.3 Funciones de Transferencia
Las funciones de transferencia representan la relación entre la entrada y la salida de un sistema lineal, usualmente descritas en el dominio de la frecuencia.

### 2.4 Diagramas de Bloques
Los diagramas de bloques son una herramienta gráfica utilizada para representar las relaciones funcionales entre los diferentes componentes de un sistema. Se incluirá:
- Álgebra de Bloques.
- Diagramas de Flujo.
- Uso de la Fórmula de Mason.

## 3. Ejemplos
💡 **Ejemplo 1**: La ecuación de la ley de Ohm se puede representar como:

$$ R = \frac{V}{I} $$

La ecuación relaciona la resistencia \( R \), el voltaje \( V \) y la corriente \( I \) en un circuito.

## 4. Ecuaciones
En este curso se utilizarán ecuaciones matemáticas para modelar sistemas dinámicos. Por ejemplo, la ecuación diferencial de un sistema de primer orden es:

$$ \tau \frac{dy(t)}{dt} + y(t) = K u(t) $$

Donde:
- \( \tau \) es la constante de tiempo.
- \( y(t) \) es la salida del sistema.
- \( u(t) \) es la entrada al sistema.

## 6. Referencias
  
  - Ogata K. Sistemas Dinámicos.
  - Ogata, K. Ingeniería de Control Moderna.
  - Smith, C. A., & Corripio, A. B. Control Automático de Procesos.
  

## 6. Código
💡 **Ejemplo 3**: Código simple en MATLAB para resolver una ecuación diferencial.

```matlab
syms y(t)
Dy = diff(y);
eqn = Dy + 2*y == cos(t);
ySol = dsolve(eqn)



