## Resolver la ecuación diferencial con la transformada de Laplace

### Ecuación diferencial:
$$
y'' - 4y' + 3y = 4e^{3t}
$$
con las condiciones iniciales:
$$
y(0) = 2, \quad y'(0) = 7
$$

### Paso 1: Ecuación homogénea
La ecuación homogénea es:
$$
y_h'' - 4y_h' + 3y_h = 0
$$
El polinomio característico es:
$$
r^2 - 4r + 3 = 0
$$
Las raíces son \(r_1 = 1\) y \(r_2 = 3\), por lo que la solución homogénea es:
$$
y_h(t) = C_1 e^t + C_2 e^{3t}
$$

### Paso 2: Solución particular
Proponemos una solución particular de la forma:
$$
y_p(t) = At e^{3t}
$$
Sustituyendo en la ecuación original y resolviendo para \(A\), obtenemos:
$$
A = 2
$$
Por lo tanto, la solución particular es:
$$
y_p(t) = 2t e^{3t}
$$

### Paso 3: Solución general
La solución general de la ecuación es la suma de la solución homogénea y la particular:
$$
y(t) = C_1 e^t + C_2 e^{3t} + 2t e^{3t}
$$

### Paso 4: Aplicar condiciones iniciales
Usamos las condiciones iniciales \(y(0) = 2\) y \(y'(0) = 7\):

1. Para \(y(0) = 2\):
   $$
   C_1 + C_2 = 2
   $$

2. Para \(y'(0) = 7\):
   $$
   C_1 + 3C_2 + 2 = 7 \quad \Rightarrow \quad C_1 + 3C_2 = 5
   $$

Resolviendo el sistema de ecuaciones:
$$
C_1 = \frac{1}{2}, \quad C_2 = \frac{3}{2}
$$

### Solución final:
$$
y(t) = \frac{1}{2} e^t + \frac{3}{2} e^{3t} + 2t e^{3t}
$$
