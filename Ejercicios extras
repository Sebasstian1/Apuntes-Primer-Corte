## Resolver la ecuación diferencial con la transformada de Laplace

### Ecuación diferencial:
\[
y'' - 4y' + 3y = 4e^{3t}
\]
con las condiciones iniciales:
\[
y(0) = 2, \quad y'(0) = 7
\]

### Paso 1: Aplicar la transformada de Laplace

Aplicamos la transformada de Laplace a ambos lados de la ecuación. Recordemos las propiedades de la transformada de Laplace para derivadas:

- \(\mathcal{L}\{y'(t)\} = sY(s) - y(0)\)
- \(\mathcal{L}\{y''(t)\} = s^2Y(s) - sy(0) - y'(0)\)
- \(\mathcal{L}\{e^{at}\} = \frac{1}{s-a}\)

Aplicando la transformada de Laplace a la ecuación original:

\[
\mathcal{L}\{y'' - 4y' + 3y\} = \mathcal{L}\{4e^{3t}\}
\]

Esto nos da:

\[
(s^2Y(s) - sy(0) - y'(0)) - 4(sY(s) - y(0)) + 3Y(s) = \frac{4}{s - 3}
\]

Sustituyendo las condiciones iniciales \(y(0) = 2\) y \(y'(0) = 7\):

\[
(s^2Y(s) - 2s - 7) - 4(sY(s) - 2) + 3Y(s) = \frac{4}{s - 3}
\]

### Paso 2: Simplificar la ecuación

Expandimos y simplificamos:

\[
s^2Y(s) - 2s - 7 - 4sY(s) + 8 + 3Y(s) = \frac{4}{s - 3}
\]

Agrupamos los términos con \(Y(s)\):

\[
(s^2 - 4s + 3)Y(s) = \frac{4}{s - 3} + 2s - 1
\]

### Paso 3: Resolver para \(Y(s)\)

Ahora despejamos \(Y(s)\):

\[
Y(s) = \frac{\frac{4}{s - 3} + 2s - 1}{s^2 - 4s + 3}
\]

Factorizamos el denominador \(s^2 - 4s + 3 = (s - 1)(s - 3)\), y reescribimos:

\[
Y(s) = \frac{\frac{4}{s - 3} + 2s - 1}{(s - 1)(s - 3)}
\]

Multiplicamos todo por \(s - 3\) para combinar términos:

\[
Y(s) = \frac{4 + (2s - 1)(s - 3)}{(s - 1)(s - 3)}
\]

Expandimos el numerador:

\[
Y(s) = \frac{4 + (2s^2 - 6s - s + 3)}{(s - 1)(s - 3)}
\]
\[
Y(s) = \frac{2s^2 - 7s + 7}{(s - 1)(s - 3)}
\]

### Paso 4: Transformada inversa de Laplace

Finalmente, aplicamos la transformada inversa de Laplace. Para esto, descomponemos en fracciones parciales:

\[
\frac{2s^2 - 7s + 7}{(s - 1)(s - 3)} = \frac{A}{s - 1} + \frac{B}{s - 3}
\]

Multiplicamos por el denominador común:

\[
2s^2 - 7s + 7 = A(s - 3) + B(s - 1)
\]

Resolviendo para \(A\) y \(B\), obtenemos:

\[
A = 1, \quad B = 1
\]

Por lo tanto:

\[
Y(s) = \frac{1}{s - 1} + \frac{1}{s - 3}
\]

### Paso 5: Resultado final

La transformada inversa de Laplace nos da la solución:

\[
y(t) = e^t + e^{3t}
\]

Esta es la solución a la ecuación diferencial dada.
