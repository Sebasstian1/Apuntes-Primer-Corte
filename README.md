# Dinámica de Sistemas

### Pre-requisitos
- Ecuaciones Diferenciales

### Software
- Matlab
- Simulador de Circuitos

## Contenido

### 1. Definiciones
### 2. Solución de Ecuaciones Diferenciales (Transformada de la Laplace)
### 3. Modelamiento Matemático
- Mecánica
- Eléctrica
- Hidráulica
- Térmica
### 4. Función de Transferencia
### 5. Diagramas de Bloques
- Álgebra de Bloques
- Diagramas de Flechas
- Fórmula de Mason
### 6. Análisis de Sistemas 1er y 2do Orden

## Evaluación

- Autoevaluación: 10%
- Coevaluación: 10%
- Examen parcial: 40%
- Tareas: 30%
- Apuntes: 10%

## Bibliografía

- **Sistemas Dinámicos** - Ogata
- **Ingeniería de Control Moderna** - Ogata
- **Control Automático de Procesos** - Smith y Corripio

## Apuntes

- Plantilla en Markdown, apuntes completos con dos ejercicios adicionales.
- La entrega se hará a través de GitHub.

---

## Derivadas

Recordemos la definición de derivada:

\[
\lim_{{h \to 0}} \frac{{f(x+h) - f(x)}}{h}
\]

Por ejemplo, si tenemos la función \( f(x) = x^2 \), su derivada es:

\[
\frac{d}{dx} = 2x
\]

En ecuaciones diferenciales más complejas, podríamos tener algo como:

\[
\frac{d}{dt} + a_1 \frac{d}{dt} + a_n f = u(t)
\]

---

## Transformada de la Laplace

La transformada de Laplace es una herramienta importante para resolver ecuaciones diferenciales. Su fórmula general es:

\[
X(s) = \int_0^{\infty} x(t) e^{-st} dt
\]

Por ejemplo, si aplicamos la transformada de \( f(t) \), obtenemos \( F(s) \):

\[
f(t) \rightarrow F(s)
\]

Algunos ejemplos comunes son:

\[
\frac{1}{s^2} \quad \frac{1}{(s-a)} \quad \frac{A}{s} + \frac{B}{s^2}
\]

---

### Ejemplo: Fracciones Parciales

Veamos un ejemplo de cómo resolver fracciones parciales:

\[
\frac{s^3 + 2s + 3}{(s+1)(s^2+2s+2)} = \frac{2}{s+1} + \frac{-s-1}{s^2+2s+2}
\]

1. Multiplicamos ambos lados por \( (s+1)(s^2+2s+2) \):

\[
s^3 + 2s + 3 = A(s^2 + 2s + 2) + (Bs + C)(s+1)
\]

2. Expandimos y agrupamos términos:

\[
s^3 + 2s + 3 = A(s^2 + 2s + 2) + (Bs^2 + (B + C)s + C)
\]
\[
s^3 + 2s + 3 = (A + B)s^2 + (2A + B + C)s + (2A + C)
\]

3. Igualamos coeficientes:

\[
A + B = 1, \quad 2A + B + C = 2, \quad 2A + C = 3
\]

4. Resolviendo el sistema, obtenemos \( A = 2 \), \( B = -1 \), y \( C = -1 \). Por lo tanto, la transformada inversa es:

\[
x(t) = 2e^{-t} - e^{-t}\cos(t)
\]

---

## **Ejercicios Extras**

### Ejercicio 1: Transformada de Laplace

Dada la función \( f(t) = 3 e^{-2t} \sin(4t) \), su transformada de Laplace se puede encontrar usando la fórmula:

\[
\mathcal{L}\{e^{at} \sin(bt)\} = \frac{b}{(s-a)^2 + b^2}
\]

Donde \( a = -2 \) y \( b = 4 \), lo que nos da:

\[
\mathcal{L}\{f(t)\} = 3 \cdot \frac{4}{(s + 2)^2 + 4^2} = \frac{12}{(s+2)^2 + 16}
\]

---

### Ejercicio 2: Transformada Inversa de Laplace

Queremos encontrar la transformada inversa de:

\[
F(s) = \frac{10}{(s+1)(s^2 + 4s + 5)}
\]

Primero, descomponemos en fracciones parciales:

\[
\frac{10}{(s+1)(s^2 + 4s + 5)} = \frac{A}{s+1} + \frac{Bs + C}{s^2 + 4s + 5}
\]

Multiplicamos ambos lados:

\[
10 = A(s^2 + 4s + 5) + (Bs + C)(s+1)
\]

Expandiendo y agrupando términos obtenemos el sistema:

- \( A + B = 0 \)
- \( 4A + B + C = 0 \)
- \( 5A + C = 10 \)

Resolviendo, obtenemos \( A = 5 \), \( B = -5 \), y \( C = -15 \), así que:

\[
\frac{10}{(s+1)(s^2 + 4s + 5)} = \frac{5}{s+1} + \frac{-5s - 15}{s^2 + 4s + 5}
\]

Aplicamos la transformada inversa:

1. Para \( \frac{5}{s+1} \):

\[
\mathcal{L}^{-1}\left\{ \frac{5}{s+1} \right\} = 5 e^{-t}
\]

2. Para \( \frac{-5s - 15}{s^2 + 4s + 5} \):

\[
f(t) = 5 e^{-t} - 5 e^{-2t} \cos(t) - 5 e^{-2t} \sin(t)
\]

---

