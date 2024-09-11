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

1. Multiplicamos ambos lados por \( (s+1)(s^2+2s+2) \) y obtenemos:

$$
s^3 + 2s + 3 = A(s^2 + 2s + 2) + (Bs + C)(s+1)
$$

2. Expandimos y agrupamos términos:

$$
s^3 + 2s + 3 = A(s^2 + 2s + 2) + (Bs^2 + (B + C)s + C)
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
x(t) = 2e^{-t} - e^{-t}\cos(t)
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
F(s) = \frac{10}{(s+1)(s^2 + 4s + 5)}
$$

**Solución:**

Primero, vamos a descomponer la función \( F(s) \) en fracciones parciales. Consideramos la expresión:

$$
\frac{10}{(s+1)(s^2 + 4s + 5)}
$$

Sabemos que podemos escribir esta fracción como una suma de términos de la forma:

$$
\frac{10}{(s+1)(s^2 + 4s + 5)} = \frac{A}{s+1} + \frac{Bs + C}{s^2 + 4s + 5}
$$

Multiplicamos ambos lados por \( (s+1)(s^2 + 4s + 5) \) para eliminar los denominadores:

$$
10 = A(s^2 + 4s + 5) + (Bs + C)(s+1)
$$

Expandimos ambos lados:

$$
10 = A(s^2 + 4s + 5) + Bs(s+1) + C(s+1)
$$

$$
10 = A s^2 + 4A s + 5A + B s^2 + B s + C s + C
$$

Agrupamos los términos similares:

$$
10 = (A + B) s^2 + (4A + B + C) s + (5A + C)
$$

Ahora igualamos los coeficientes de los términos de \( s^2 \), \( s \), y el término constante con el lado derecho, que es 10:

1. Para \( s^2 \): \( A + B = 0 \)
2. Para \( s \): \( 4A + B + C = 0 \)
3. Para el término constante: \( 5A + C = 10 \)

Resolvemos este sistema de ecuaciones:

- De \( A + B = 0 \), obtenemos \( B = -A \).
- Sustituimos \( B = -A \) en la segunda ecuación \( 4A + B + C = 0 \):

$$
4A - A + C = 0 \implies 3A + C = 0 \implies C = -3A
$$

- Sustituimos \( C = -3A \) en la tercera ecuación \( 5A + C = 10 \):

$$
5A - 3A = 10 \implies 2A = 10 \implies A = 5
$$

- Como \( A = 5 \), entonces:

$$
B = -5 \quad \text{y} \quad C = -15
$$

Así, la descomposición en fracciones parciales es:

$$
\frac{10}{(s+1)(s^2 + 4s + 5)} = \frac{5}{s+1} + \frac{-5s - 15}{s^2 + 4s + 5}
$$

Ahora aplicamos la transformada inversa de Laplace a cada término por separado:

1. Para el término \( \frac{5}{s+1} \), sabemos que la transformada inversa es:

$$
\mathcal{L}^{-1}\left\{ \frac{5}{s+1} \right\} = 5 e^{-t}
$$

2. Para el término \( \frac{-5s - 15}{s^2 + 4s + 5} \), primero reescribimos el denominador como:

$$
s^2 + 4s + 5 = (s+2)^2 + 1
$$

Entonces, tenemos que:

$$
\frac{-5s - 15}{s^2 + 4s + 5} = \frac{-5(s+2) + (-5)}{(s+2)^2 + 1}
$$

Ahora, descomponemos esto en dos términos:

$$
\frac{-5(s+2)}{(s+2)^2 + 1} + \frac{-5}{(s+2)^2 + 1}
$$

Sabemos que la transformada inversa de \( \frac{s+a}{(s+a)^2 + b^2} \) es \( e^{-at} \cos(bt) \), y que la transformada inversa de \( \frac{b}{(s+a)^2 + b^2} \) es \( e^{-at} \sin(bt) \).

Aplicando estas fórmulas, obtenemos:

- Para \( \frac{-5(s+2)}{(s+2)^2 + 1} \), la transformada inversa es:

$$
-5 e^{-2t} \cos(t)
$$

- Para \( \frac{-5}{(s+2)^2 + 1} \), la transformada inversa es:

$$
-5 e^{-2t} \sin(t)
$$

Por lo tanto, la transformada inversa completa es:

$$
f(t) = 5 e^{-t} - 5 e^{-2t} \cos(t) - 5 e^{-2t} \sin(t)
$$

Este es el resultado final de la transformada inversa.
