# Dinámica de Sistemas

## Pre-requisitos
- Ecuaciones Diferenciales

## Software
- Matlab
- Simulador de Circuitos

## Contenido
- Definiciones
- Solución de Ecuaciones Diferenciales (Transformada de la Laplace)
- Modelamiento Matemático
  - Mecánica
  - Eléctrica
  - Hidráulica
  - Térmica
- Funcional de Transferencia
- Diagramas de Bloques
  - Álgebra de Bloques
  - Diagramas de Flechas
  - Fórmula de Mason
- Análisis de Sistemas 1er y 2do Orden

## Evaluación
- Autoevaluación: 10%
- Coevaluación: 10%
- Parcial: 40%
- Tareas: 30%
- Apuntes: 10%

## Bibliografía
- **Sistemas Dinámicos** - Ogata
- **Ingeniería de Control Moderna** - Ogata
- **Control Automático de Procesos** - Smith y Corripio

## Apuntes
- Plantilla (Markdown), Completos, 2 ejercicios Aparte
- GitHub → Entrega

---

### Derivadas

$$
\lim_{{h \to 0}} \frac{{f(x+h) - f(x)}}{h}
$$

$$
f(x) = x^2
$$

$$
\frac{d}{dx} = 2x
$$

$$
\frac{d}{dt} + a_1 \frac{d}{dt} + a_n f = u(t)
$$

---

### Transformada de la Laplace

$$
X(s) = \int_0^{\infty} x(t) e^{-st} dt
$$

$$
f(t) \rightarrow F(s)
$$

$$
\frac{1}{s^2} \quad \frac{1}{(s-a)} \quad \frac{A}{s} + \frac{B}{s^2}
$$

---

### Ejemplo de Fracciones Parciales

Resolver la expresión:

$$
\frac{s^3 + 2s + 3}{(s+1)(s^2+2s+2)} = \frac{2}{s+1} + \frac{-s-1}{s^2+2s+2}
$$

1. Multiplicamos ambos lados por $$(s+1)(s^2+2s+2)$$ y obtenemos:
   
   $$
   s^3 + 2s + 3 = A(s^2 + 2s + 2) + (B s + C)(s+1)
   $$

2. Expandimos y agrupamos términos:

   $$
   s^3 + 2s + 3 = (A s^2 + 2A s + 2A) + (B s^2 + (B + C) s + C)
   $$

   $$
   s^3 + 2s + 3 = (A + B)s^2 + (2A + B + C)s + (2A + C)
   $$

3. Igualamos coeficientes y términos constantes:
   
   $$
   A + B = 1
   $$

   $$
   2A + B + C = 2
   $$

   $$
   2A + C = 3
   $$

4. Resolviendo el sistema de ecuaciones obtenemos:

$$
A = 2, \quad B = -1, \quad C = -1
$$

5. Transformada inversa de Laplace:

$$
x(t) = 2 e^{-t} - e^{-t} \cos(t)
$$

---

## **Ejercicios Extras**

### Ejercicio 1: Transformada de Laplace

Dada la siguiente función en el dominio del tiempo:

$$
f(t) = 3 e^{-2t} \sin(4t)
$$

Encuentra su transformada de Laplace.

**Solución:**

Sabemos que la transformada de Laplace de una función del tipo:

$$
e^{at} \sin(bt)
$$

es:

$$
\mathcal{L}\{e^{at} \sin(bt)\} = \frac{b}{(s-a)^2 + b^2}
$$

En este caso, tenemos \( a = -2 \) y \( b = 4 \), por lo tanto, la transformada de \( f(t) = 3 e^{-2t} \sin(4t) \) es:

$$
\mathcal{L}\{f(t)\} = 3 \cdot \frac{4}{(s + 2)^2 + 4^2}
$$

Simplificando:

$$
\mathcal{L}\{f(t)\} = \frac{12}{(s+2)^2 + 16}
$$

---

### Ejercicio 2: Transformada Inversa de Laplace

Encuentra la transformada inversa de la siguiente función en el dominio de \( s \):

$$
F(s) = \frac{5}{s^2 + 9}
$$

**Solución:**

Sabemos que la transformada de Laplace de una función del tipo:

$$
\sin(at)
$$

es:

$$
\mathcal{L}\{\sin(at)\} = \frac{a}{s^2 + a^2}
$$

En este caso, tenemos que \( a = 3 \), por lo que la transformada inversa de \( F(s) = \frac{5}{s^2 + 9} \) es:

$$
f(t) = \frac{5}{3} \sin(3t)
$$

---

Estos dos ejercicios adicionales cubren tanto una transformada de Laplace directa como una inversa. Si tienes más ejercicios o necesitas más ejemplos, ¡no dudes en pedírmelo!
