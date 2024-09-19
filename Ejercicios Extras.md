### Solución de la Ecuación Diferencial

La ecuación diferencial dada es:

\[ y'' - 4y' + 3y = 4e^{3t} \]

Con las condiciones iniciales \( y(0) = 2 \) y \( y'(0) = 7 \), la solución es:

\[ y(t) = \frac{1}{2} e^t + \frac{3}{2} e^{3t} + 2t e^{3t} \]

### Paso a Paso

1. **Aplicar la Transformada de Laplace:**

   Aplicamos la transformada de Laplace a ambos lados de la ecuación diferencial. Usamos las siguientes propiedades:

   \[
   \mathcal{L}\{y''\} = s^2 Y(s) - sy(0) - y'(0)
   \]

   \[
   \mathcal{L}\{y'\} = s Y(s) - y(0)
   \]

   \[
   \mathcal{L}\{y\} = Y(s)
   \]

   \[
   \mathcal{L}\{4e^{3t}\} = \frac{4}{s-3}
   \]

   Sustituyendo en la ecuación:

   \[
   \mathcal{L}\{y''\} - 4 \mathcal{L}\{y'\} + 3 \mathcal{L}\{y\} = \mathcal{L}\{4e^{3t}\}
   \]

   \[
   (s^2 Y(s) - sy(0) - y'(0)) - 4(s Y(s) - y(0)) + 3Y(s) = \frac{4}{s-3}
   \]

   Con \( y(0) = 2 \) y \( y'(0) = 7 \):

   \[
   s^2 Y(s) - 2s - 7 - 4(s Y(s) - 2) + 3Y(s) = \frac{4}{s-3}
   \]

   Simplificando:

   \[
   s^2 Y(s) - 2s - 7 - 4s Y(s) + 8 + 3Y(s) = \frac{4}{s-3}
   \]

   \[
   (s^2 - 4s + 3) Y(s) - 2s + 1 = \frac{4}{s-3}
   \]

   Despejando \( Y(s) \):

   \[
   Y(s) = \frac{4}{(s-3)(s^2 - 4s + 3)} + \frac{2s - 1}{s^2 - 4s + 3}
   \]

2. **Descomposición en Fracciones Parciales:**

   Factorizamos el denominador \( s^2 - 4s + 3 \):

   \[
   s^2 - 4s + 3 = (s-1)(s-3)
   \]

   Entonces:

   \[
   Y(s) = \frac{4}{(s-3)^2(s-1)} + \frac{2s - 1}{(s-1)(s-3)}
   \]

   Descomponemos \( \frac{2s - 1}{(s-1)(s-3)} \) en fracciones parciales:

   \[
   \frac{2s - 1}{(s-1)(s-3)} = \frac{A}{s-1} + \frac{B}{s-3}
   \]

   Multiplicamos por el denominador común \( (s-1)(s-3) \):

   \[
   2s - 1 = A(s-3) + B(s-1)
   \]

   Comparando coeficientes, encontramos:

   \[
   2s - 1 = (A + B)s - (3A + B)
   \]

   Resolviendo para \( A \) y \( B \):

   \[
   A + B = 2
   \]

   \[
   -3A - B = -1
   \]

   Resolviendo el sistema:

   \[
   A = 1, \quad B = 1
   \]

   Entonces:

   \[
   \frac{2s - 1}{(s-1)(s-3)} = \frac{1}{s-1} + \frac{1}{s-3}
   \]

   Para \( \frac{4}{(s-3)^2(s-1)} \):

   Descomponemos en fracciones parciales:

   \[
   \frac{4}{(s-3)^2(s-1)} = \frac{A}{s-1} + \frac{B}{s-3} + \frac{C}{(s-3)^2}
   \]

   Multiplicamos por el denominador común:

   \[
   4 = A(s-3)^2 + B(s-3)(s-1) + C(s-1)
   \]

   Comparando coeficientes, encontramos:

   \[
   A = 2, \quad B = 0, \quad C = -2
   \]

   Entonces:

   \[
   \frac{4}{(s-3)^2(s-1)} = \frac{2}{(s-3)^2} - \frac{2}{s-1}
   \]

   Finalmente:

   \[
   Y(s) = \frac{2}{(s-3)^2} - \frac{2}{s-1} + \frac{1}{s-1} + \frac{1}{s-3}
   \]

   Simplificando:

   \[
   Y(s) = \frac{2}{(s-3)^2} - \frac{1}{s-1} + \frac{1}{s-3}
   \]

3. **Transformada Inversa de Laplace:**

   La transformada inversa para cada término es:

   \[
   \mathcal{L}^{-1}\left\{\frac{2}{(s-3)^2}\right\} = 2t e^{3t}
   \]

   \[
   \mathcal{L}^{-1}\left\{\frac{1}{s-1}\right\} = e^t
   \]

   \[
   \mathcal{L}^{-1}\left\{\frac{1}{s-3}\right\} = e^{3t}
   \]

   Entonces:

   \[
   y(t) = 2t e^{3t} + e^t + e^{3t}
   \]

   Simplificando:

   \[
   y(t) = \frac{1}{2} e^t + \frac{3}{2} e^{3t} + 2t e^{3t}
   \]
