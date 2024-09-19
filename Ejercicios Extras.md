### Solución de la Ecuación Diferencial 1

La ecuación diferencial dada es:

    y'' - 4y' + 3y = 4e^(3t)

Con las condiciones iniciales `y(0) = 2` y `y'(0) = 7`, la solución es:

    y(t) = (1/2)e^t + (3/2)e^(3t) + 2t e^(3t)

### Paso a Paso

1. **Aplicar la Transformada de Laplace:**

   La transformada de Laplace de la ecuación diferencial es:

    L{y''} - 4 L{y'} + 3 L{y} = L{4e^(3t)}

   Donde:

    L{y''} = s^2 Y(s) - sy(0) - y'(0)
    L{y'} = s Y(s) - y(0)
    L{y} = Y(s)
    L{4e^(3t)} = 4 / (s - 3)

   Sustituyendo en la ecuación:

    (s^2 Y(s) - s*2 - 7) - 4(s Y(s) - 2) + 3Y(s) = 4 / (s - 3)

   Simplificando:

    s^2 Y(s) - 2s - 7 - 4s Y(s) + 8 + 3Y(s) = 4 / (s - 3)
    (s^2 - 4s + 3) Y(s) - 2s + 1 = 4 / (s - 3)

   Despejando Y(s):

    Y(s) = [4 / (s - 3)] / [(s - 1)(s - 3)^2] + (2s - 1) / [(s - 1)(s - 3)]

2. **Descomposición en Fracciones Parciales:**

   Factorizamos el denominador:

    s^2 - 4s + 3 = (s - 1)(s - 3)

   Entonces:

    Y(s) = 4 / [(s - 3)^2(s - 1)] + (2s - 1) / [(s - 1)(s - 3)]

   Para descomponer (2s - 1) / [(s - 1)(s - 3)]:

    (2s - 1) / [(s - 1)(s - 3)] = A / (s - 1) + B / (s - 3)

   Multiplicamos por el denominador común (s - 1)(s - 3):

    2s - 1 = A(s - 3) + B(s - 1)

   Resolviendo para A y B:

    A + B = 2
    -3A - B = -1

   Solucionando:

    A = 1
    B = 1

   Entonces:

    (2s - 1) / [(s - 1)(s - 3)] = 1 / (s - 1) + 1 / (s - 3)

   Para 4 / [(s - 3)^2(s - 1)]:

    4 / [(s - 3)^2(s - 1)] = A / (s - 1) + B / (s - 3) + C / (s - 3)^2

   Multiplicamos por el denominador común:

    4 = A(s - 3)^2 + B(s - 3)(s - 1) + C(s - 1)

   Resolviendo para A, B y C:

    A = 2
    B = 0
    C = -2

   Entonces:

    4 / [(s - 3)^2(s - 1)] = 2 / (s - 3)^2 - 2 / (s - 1)

   Finalmente:

    Y(s) = 2 / (s - 3)^2 - 2 / (s - 1) + 1 / (s - 1) + 1 / (s - 3)
    Y(s) = 2 / (s - 3)^2 - 1 / (s - 1) + 1 / (s - 3)

3. **Transformada Inversa de Laplace:**

   La transformada inversa para cada término es:

    L^(-1){2 / (s - 3)^2} = 2t e^(3t)
    L^(-1){1 / (s - 1)} = e^t
    L^(-1){1 / (s - 3)} = e^(3t)

   Entonces:

    y(t) = 2t e^(3t) + e^t + e^(3t)

   Simplificando:

    y(t) = (1/2)e^t + (3/2)e^(3t) + 2t e^(3t)


### Solución de la Ecuación Diferencial 2

La ecuación diferencial dada es:

    y'' + y = e^(-2t) sin(t)

Con las condiciones iniciales `y(0) = 0` y `y'(0) = 0`, la solución es:

    y(t) = -1/8 cos(t) + 1/8 sin(t) + 1/8 e^(-2t) cos(t) + 1/8 e^(-2t) sin(t)

### Paso a Paso

1. **Aplicar la Transformada de Laplace**

   Aplicamos la transformada de Laplace a la ecuación diferencial:

    L{y''} + L{y} = L{e^(-2t) sin(t)}

   Sabemos que:

    L{y''} = s^2 Y(s) - sy(0) - y'(0)
    L{y} = Y(s)
    L{e^(-2t) sin(t)} = 1 / [(s + 2)^2 + 1]

   Dado que `y(0) = 0` y `y'(0) = 0`, obtenemos:

    s^2 Y(s) + Y(s) = 1 / [(s + 2)^2 + 1]
    (s^2 + 1) Y(s) = 1 / [(s + 2)^2 + 1]
    Y(s) = 1 / [(s^2 + 1) [(s + 2)^2 + 1]]

2. **Descomposición en Fracciones Parciales**

   Descomponemos:

    1 / [(s^2 + 1) [(s + 2)^2 + 1]] = (As + B) / (s^2 + 1) + (Cs + D) / [(s + 2)^2 + 1]

   Multiplicamos por el denominador común:

    1 = (As + B) [(s + 2)^2 + 1] + (Cs + D) (s^2 + 1)

   Expandimos y agrupamos términos para comparar coeficientes:

    A = -1/8
    B = 0
    C = 1/8
    D = 1/8

   Por lo tanto:

    Y(s) = -1/8 [1 / (s^2 + 1)] + 1/8 [(s + 2) / [(s + 2)^2 + 1]]

3. **Transformada Inversa de Laplace**

   Aplicamos la transformada inversa:

    L^(-1){-1/8 [1 / (s^2 + 1)]} = -1/8 sin(t)
    L^(-1){1/8 [(s + 2) / [(s + 2)^2 + 1]]} = 1/8 e^(-2t) cos(t) + 1/8 e^(-2t) sin(t)

   Por lo tanto, la solución es:

    y(t) = -1/8 cos(t) + 1/8 sin(t) + 1/8 e^(-2t) cos(t) + 1/8 e^(-2t) sin(t)
