# Ejercicio 1

Dada la función de transferencia:

(s^2 + 2s + 3) / ((s^2 + 2s + 2)(s^2 + 2s + 5))

La descomposición en fracciones parciales es:

(s^2 + 2s + 3) / ((s^2 + 2s + 2)(s^2 + 2s + 5)) = 2 / (3(s^2 + 2s + 5)) + 1 / (3(s^2 + 2s + 2))

**Transformada inversa de Laplace para cada término**:

1. Para el término `2 / (3(s^2 + 2s + 5))`, la transformada inversa de Laplace es:

    (2 / 3) * e^(-t) * sin(2t)

2. Para el término `1 / (3(s^2 + 2s + 2))`, la transformada inversa de Laplace es:

    (1 / 3) * e^(-t) * sin(t)

La solución final en el dominio del tiempo es la suma de estos dos términos:

f(t) = (2 / 3) * e^(-t) * sin(2t) + (1 / 3) * e^(-t) * sin(t)

---

# Ejercicio 2

Dada la función de transferencia:

(s + 3) / ((s + 1)(s + 2))

La descomposición en fracciones parciales es:

(s + 3) / ((s + 1)(s + 2)) = 2 / (s + 1) - 1 / (s + 2)

**Transformada inversa de Laplace**:

1. Para el término `2 / (s + 1)`, la transformada inversa de Laplace es:

    2 * e^(-t)

2. Para el término `1 / (s + 2)`, la transformada inversa de Laplace es:

    e^(-2t)

La solución final en el dominio del tiempo es:

f(t) = 2 * e^(-t) - e^(-2t)
