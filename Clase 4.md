# Dinámica de sistemas

En esta clase se aborda la dinámica de sistemas mecánicos, la cual estudia el comportamiento de sistemas físicos bajo la acción de fuerzas. Utilizaremos modelos de masa-resorte y analizaremos las ecuaciones de movimiento para describir el comportamiento dinámico de estos sistemas. Se introducen también conceptos como MISO (Multiple Input, Single Output) y SISO (Single Input, Single Output), utilizados en el análisis de sistemas.

## 1. Modelado de sistemas mecánicos

Un sistema mecánico puede representarse mediante modelos de masa-resorte como se muestra en la siguiente figura:

- \( M_1 \) y \( M_2 \) son las masas en el sistema.
- \( K_1 \), \( K_2 \) y \( K_3 \) representan las constantes de los resortes.
- Las fuerzas \( F_{K1} \), \( F_{K2} \) y \( F_{R} \) actúan sobre las masas.

## 2. Definiciones

> 🔑 *Sistema mecánico*: conjunto de componentes físicos (masas, resortes, amortiguadores) que interactúan bajo la influencia de fuerzas externas y cumplen con las leyes del movimiento.

> 🔑 *MISO*: (*Multiple Input, Single Output*) se refiere a un sistema con múltiples entradas y una sola salida.

> 🔑 *SISO*: (*Single Input, Single Output*) se refiere a un sistema con una entrada y una salida.

## 3. Ecuaciones del sistema

Para un sistema de masa-resorte, las ecuaciones de movimiento se derivan de la segunda ley de Newton. Las ecuaciones que describen el movimiento de las masas \( M_1 \) y \( M_2 \) son las siguientes:

💡 **Ejemplo 1**:

Las ecuaciones de movimiento para \( M_1 \) y \( M_2 \) se expresan como:

$$
M_1 \ddot{x_1} = F_1 - F_{K1} - F_{R}
$$

$$
M_2 \ddot{x_2} = F_{K2} - F_R
$$

Donde \( F_1 \) es la fuerza externa aplicada, \( F_{K1} \), \( F_{K2} \) son las fuerzas elásticas de los resortes, y \( F_R \) es la fuerza de fricción.

---

### 3.1 Ecuaciones de equilibrio

Para el equilibrio del sistema, las fuerzas deben balancearse. Esto da lugar a las siguientes ecuaciones:

💡 **Ejemplo 2**:

Para \( M_1 \):

$$
M_1 \ddot{x_1} = K_1 x_1 + K_2 (x_1 - x_2) - b = 0
$$

Para \( M_2 \):

$$
M_2 \ddot{x_2} = K_2 (x_1 - x_2) + K_3 x_2 = 0
$$

Donde \( b \) es el coeficiente de fricción, \( K_1 \), \( K_2 \), \( K_3 \) son las constantes de los resortes, y \( x_1 \), \( x_2 \) son los desplazamientos de las masas.

---

## 4. Figuras

![Diagrama de sistema mecánico](../images/sistema_mecanico.png)

Figura 1. Representación del sistema mecánico.

## 5. Ejercicios

📚 **Ejercicio 1**: Calcular el movimiento de las masas \( M_1 \) y \( M_2 \) para un sistema donde \( K_1 = 5 \, \text{N/m} \), \( K_2 = 3 \, \text{N/m} \), \( K_3 = 4 \, \text{N/m} \), y no hay fricción (\( b = 0 \)).

**Solución**:

Para \( M_1 \):

$$
M_1 \ddot{x_1} = 5 x_1 + 3 (x_1 - x_2)
$$

Para \( M_2 \):

$$
M_2 \ddot{x_2} = 3 (x_1 - x_2) + 4 x_2
$$

📚 **Ejercicio 2**: Determinar si el sistema tiene una solución en equilibrio, considerando que las masas \( M_1 = M_2 = 1 \, \text{kg} \).

**Solución**:

Para el equilibrio, \( \ddot{x_1} = \ddot{x_2} = 0 \). Las ecuaciones se simplifican a:

$$
5 x_1 + 3 (x_1 - x_2) = 0
$$

$$
3 (x_1 - x_2) + 4 x_2 = 0
$$

Resolviendo el sistema de ecuaciones simultáneas:

$$
x_1 = x_2 = 0
$$

Esto indica que el sistema está en equilibrio cuando ambas masas están en reposo.

---

## 6. Conclusiones

En esta clase hemos aprendido a modelar sistemas mecánicos utilizando ecuaciones de movimiento para masas conectadas por resortes. Hemos visto cómo derivar las ecuaciones de equilibrio y analizar las condiciones bajo las cuales el sistema puede estar en reposo. Además, hemos aplicado estas ecuaciones a ejemplos numéricos para entender mejor el comportamiento dinámico del sistema.

## 7. Referencias

1. "Dinámica de sistemas mecánicos", Autor Desconocido.
2. "Modelado y Simulación de Sistemas Mecánicos", por X Autor.
