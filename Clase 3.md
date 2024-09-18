# Ejercicio: Transformada inversa de Laplace

## Función original
La función a resolver es la siguiente:

\[
F(s) = \frac{s^2+2s+3}{(s^2+2s+2)(s^2+2s+5)}
\]

## 1. Descomposición en fracciones parciales

Queremos expresar la función de la siguiente forma:

\[
F(s) = \frac{As+B}{s^2+2s+2} + \frac{Cs+D}{s^2+2s+5}
\]

Multiplicamos ambos lados por \((s^2 + 2s + 2)(s^2 + 2s + 5)\) para eliminar los denominadores:

\[
s^2 + 2s + 3 = (As+B)(s^2 + 2s + 5) + (Cs+D)(s^2 + 2s + 2)
\]

Expandiendo ambos términos:

\[
s^2 + 2s + 3 = (As^3 + 2As^2 + 5As + Bs^2 + 2Bs + 5B) + (Cs^3 + 2Cs^2 + 2Cs + Ds^2 + 2Ds + 2D)
\]

Agrupamos los términos en potencias de \(s\):

\[
s^2 + 2s + 3 = (A + C)s^3 + (2A + B + 2C + D)s^2 + (5A + 2B + 2C + 2D)s + (5B + 2D)
\]

Comparando los coeficientes con \(s^2 + 2s + 3\):

- Coeficiente de \(s^3\):

\[
A + C = 0
\]

- Coeficiente de \(s^2\):

\[
2A + B + 2C + D = 1
\]

- Coeficiente de \(s\):

\[
5A + 2B + 2C + 2D = 2
\]

- Término constante:

\[
5B + 2D = 3
\]

### Resolviendo el sistema de ecuaciones

De \(A + C = 0\), tenemos que \(C = -A\). Sustituyendo en las otras ecuaciones:

1. \(2A + B + 2(-A) + D = 1 \Rightarrow B + D = 1\)
2. \(5A + 2B + 2(-A) + 2D = 2 \Rightarrow 3A + 2B + 2D = 2\)
3. \(5B + 2D = 3\)

Resolviendo este sistema obtenemos los valores de \(A\), \(B\), \(C\) y \(D\).

## 2. Transformada inversa de Laplace

Después de obtener los coeficientes \(A\), \(B\), \(C\) y \(D\), tomamos la transformada inversa de Laplace de cada término:

\[
L^{-1}\left\{ \frac{As + B}{s^2 + 2s + 2} \right\} + L^{-1}\left\{ \frac{Cs + D}{s^2 + 2s + 5} \right\}
\]

Usamos las tablas de transformadas inversas de Laplace para resolver cada término.

## 3. Verificación con MATLAB

A continuación, te dejo el código en MATLAB para comprobar los resultados:

```matlab
% Definir las funciones simbólicas
syms s t

% Función de transferencia
numerator = s^2 + 2*s + 3;
denominator = (s^2 + 2*s + 2)*(s^2 + 2*s + 5);

% Descomposición en fracciones parciales
F_s = numerator / denominator;
F_s_partial = partfrac(F_s);

% Transformada inversa de Laplace
f_t = ilaplace(F_s);

% Mostrar los resultados
disp('Fracciones parciales:');
disp(F_s_partial);

disp('Transformada inversa:');
disp(f_t);

% Graficar la solución en el dominio del tiempo
fplot(f_t, [0 10]);
xlabel('t');
ylabel('f(t)');
title('Respuesta en el dominio del tiempo');
grid on;

