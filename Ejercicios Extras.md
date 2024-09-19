### Solución de la Ecuación Diferencial

La ecuación diferencial dada es:

\[ y'' - 4y' + 3y = 4e^{3t} \]

Con las condiciones iniciales \( y(0) = 2 \) y \( y'(0) = 7 \), la solución es:

\[
y(t) = \frac{1}{2} e^t + \frac{3}{2} e^{3t} + 2t e^{3t}
\]

### Paso a Paso

1. **Transformada de Laplace:**

   Aplicamos la transformada de Laplace a ambos lados de la ecuación diferencial:

   \[
   s^2 Y(s) - sy(0) - y'(0) - 4(s Y(s) - y(0)) + 3Y(s) = \frac{4}{s-3}
   \]

   Sustituyendo \( y(0) = 2 \) y \( y'(0) = 7 \):

   \[
   s^2 Y(s) - 2s - 7 - 4(s Y(s) - 2) + 3Y(s) = \frac{4}{s-3}
   \]

   Simplificando:

   \[
   (s^2 - 4s + 3)Y(s) - 2s + 1 = \frac{4}{s-3}
   \]

   Despejando \( Y(s) \):

   \[
   Y(s) = \frac{4}{(s-3)^2(s-1)} + \frac{2s - 1}{(s-1)(s-3)}
   \]

2. **Descomposición en Fracciones Parciales:**

   Para la fracción:

   \[
   \frac{2s - 1}{(s-1)(s-3)} = \frac{1}{s-1} + \frac{1}{s-3}
   \]

   Y:

   \[
   \frac{4}{(s-3)^2(s-1)} = \frac{2}{(s-3)^2} + \frac{1}{s-1}
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
