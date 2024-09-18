# Resolución de Ecuaciones por Fracciones Parciales y Transformada Inversa de Laplace

## Ejercicio 1

Dada la función:

    (s^2 + 2s + 3) / [(s^2 + 2s + 2)(s^2 + 2s + 5)]

### Descomposición en Fracciones Parciales

Descomponemos la función en fracciones parciales:

    (s^2 + 2s + 3) / [(s^2 + 2s + 2)(s^2 + 2s + 5)] = (As + B) / (s^2 + 2s + 2) + (Cs + D) / (s^2 + 2s + 5)

Multiplicamos ambos lados por el denominador común:

    s^2 + 2s + 3 = (As + B)(s^2 + 2s + 5) + (Cs + D)(s^2 + 2s + 2)

Resolviendo para A, B, C y D:

    A = 1
    B = 1
    C = -1
    D = 2

Por lo tanto:

    (s^2 + 2s + 3) / [(s^2 + 2s + 2)(s^2 + 2s + 5)] = (s + 1) / (s^2 + 2s + 2) - (s - 2) / (s^2 + 2s + 5)

### Transformada Inversa de Laplace

Para encontrar la transformada inversa de Laplace:

- Para (s + 1) / (s^2 + 2s + 2):

    L^-1{(s + 1) / (s^2 + 2s + 2)} = e^(-t) * cos(t)

- Para (s - 2) / (s^2 + 2s + 5):

    L^-1{(s - 2) / (s^2 + 2s + 5)} = e^(-t) * [cos(2t) + (1/2) * sin(2t)]

Entonces, la transformada inversa completa es:

    L^-1{(s^2 + 2s + 3) / [(s^2 + 2s + 2)(s^2 + 2s + 5)]} = e^(-t) * cos(t) - e^(-t) * [cos(2t) + (1/2) * sin(2t)]

## Ejercicio 2

Dada la función:

    (s + 3) / [(s + 1)(s + 2)]

### Descomposición en Fracciones Parciales

Descomponemos la función en fracciones parciales:

    (s + 3) / [(s + 1)(s + 2)] = A / (s + 1) + B / (s + 2)

Multiplicamos ambos lados por el denominador común y resolvemos para A y B:

    s + 3 = A(s + 2) + B(s + 1)

Resolviendo para A y B:

    A = 1
    B = 2

Por lo tanto:

    (s + 3) / [(s + 1)(s + 2)] = 1 / (s + 1) + 2 / (s + 2)

### Transformada Inversa de Laplace

Para encontrar la transformada inversa de Laplace:

- Para 1 / (s + 1):

    L^-1{1 / (s + 1)} = e^(-t)

- Para 2 / (s + 2):

    L^-1{2 / (s + 2)} = 2 * e^(-2t)

Entonces, la transformada inversa completa es:

    L^-1{(s + 3) / [(s + 1)(s + 2)]} = e^(-t) + 2 * e^(-2t)
