# Ejercicio 1

Dada la función de transferencia:

\[
\frac{s^2+2s+3}{(s^2+2s+2)(s^2+2s+5)}
\]

La descomposición en fracciones parciales es:

\[
\frac{s^2+2s+3}{(s^2+2s+2)(s^2+2s+5)} = \frac{2}{3(s^2 + 2s + 5)} + \frac{1}{3(s^2 + 2s + 2)}
\]

**Transformada inversa de Laplace para cada término**:

1. Para el término \(\frac{2}{3(s^2 + 2s + 5)}\), la transformada inversa de Laplace es:

\[
L^{-1} \left[ \frac{2}{3(s^2 + 2s + 5)} \right] = \frac{2}{3} e^{-t} \sin(2t)
\]

2. Para el término \(\frac{1}{3(s^2 + 2s + 2)}\), la transformada inversa de Laplace es:

\[
L^{-1} \left[ \frac{1}{3(s^2 + 2s + 2)} \right] = \frac{1}{3} e^{-t} \sin(t)
\]

La solución final en el dominio del tiempo es la suma de estos dos términos:

\[
f(t) = \frac{2}{3} e^{-t} \sin(2t) + \frac{1}{3} e^{-t} \sin(t)
\]

---

# Ejercicio 2

Dada la función de transferencia:

\[
\frac{s+3}{(s+1)(s+2)}
\]

La descomposición en fracciones parciales es:

\[
\frac{s+3}{(s+1)(s+2)} = \frac{2}{s+1} - \frac{1}{s+2}
\]

**Transformada inversa de Laplace**:

1. Para el término \(\frac{2}{s+1}\), la transformada inversa de Laplace es:

\[
L^{-1} \left[ \frac{2}{s+1} \right] = 2 e^{-t}
\]

2. Para el término \(\frac{1}{s+2}\), la transformada inversa de Laplace es:

\[
L^{-1} \left[ \frac{1}{s+2} \right] = e^{-2t}
\]

La solución final en el dominio del tiempo es:

\[
f(t) = 2 e^{-t} - e^{-2t}
\]



