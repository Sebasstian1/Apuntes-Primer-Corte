# Resolución de Ecuaciones por Fracciones Parciales y Transformada Inversa de Laplace

## Ejercicio 1

Dada la función:

\[ \frac{s^2 + 2s + 3}{(s^2 + 2s + 2)(s^2 + 2s + 5)} \]

### Descomposición en Fracciones Parciales

Primero, descomponemos la función en fracciones parciales:

\[ \frac{s^2 + 2s + 3}{(s^2 + 2s + 2)(s^2 + 2s + 5)} = \frac{As + B}{s^2 + 2s + 2} + \frac{Cs + D}{s^2 + 2s + 5} \]

Multiplicamos ambos lados por el denominador común y agrupamos términos similares:

\[ s^2 + 2s + 3 = (As + B)(s^2 + 2s + 5) + (Cs + D)(s^2 + 2s + 2) \]

Resolviendo para \(A\), \(B\), \(C\) y \(D\), obtenemos:

\[ A = 1, \, B = 1, \, C = -1, \, D = 2 \]

Por lo tanto:

\[ \frac{s^2 + 2s + 3}{(s^2 + 2s + 2)(s^2 + 2s + 5)} = \frac{s + 1}{s^2 + 2s + 2} - \frac{s - 2}{s^2 + 2s + 5} \]

### Transformada Inversa de Laplace

Para encontrar la transformada inversa de Laplace, utilizamos tablas estándar:

- Para \( \frac{s + 1}{s^2 + 2s + 2} \), tenemos:
  
  \[ \mathcal{L}^{-1} \left\{ \frac{s + 1}{s^2 + 2s + 2} \right\} = e^{-t} \cos(t) \]

- Para \( \frac{s - 2}{s^2 + 2s + 5} \), tenemos:
  
  \[ \mathcal{L}^{-1} \left\{ \frac{s - 2}{s^2 + 2s + 5} \right\} = e^{-t} \left[ \cos(2t) + \frac{1}{2} \sin(2t) \right] \]

Entonces, la transformada inversa completa es:

\[ \mathcal{L}^{-1} \left\{ \frac{s^2 + 2s + 3}{(s^2 + 2s + 2)(s^2 + 2s + 5)} \right\} = e^{-t} \cos(t) - e^{-t} \left[ \cos(2t) + \frac{1}{2} \sin(2t) \right] \]

## Ejercicio 2

Dada la función:

\[ \frac{s + 3}{(s + 1)(s + 2)} \]

### Descomposición en Fracciones Parciales

Descomponemos la función en fracciones parciales:

\[ \frac{s + 3}{(s + 1)(s + 2)} = \frac{A}{s + 1} + \frac{B}{s + 2} \]

Multiplicamos ambos lados por el denominador común y resolvemos para \(A\) y \(B\):

\[ s + 3 = A(s + 2) + B(s + 1) \]

Resolviendo para \(A\) y \(B\), obtenemos:

\[ A = 1, \, B = 2 \]

Por lo tanto:

\[ \frac{s + 3}{(s + 1)(s + 2)} = \frac{1}{s + 1} + \frac{2}{s + 2} \]

### Transformada Inversa de Laplace

Para encontrar la transformada inversa de Laplace, utilizamos tablas estándar:

- Para \( \frac{1}{s + 1} \), tenemos:
  
  \[ \mathcal{L}^{-1} \left\{ \frac{1}{s + 1} \right\} = e^{-t} \]

- Para \( \frac{2}{s + 2} \), tenemos:
  
  \[ \mathcal{L}^{-1} \left\{ \frac{2}{s + 2} \right\} = 2e^{-2t} \]

Entonces, la transformada inversa completa es:

\[ \mathcal{L}^{-1} \left\{ \frac{s + 3}{(s + 1)(s + 2)} \right\} = e^{-t} + 2e^{-2t} \]
