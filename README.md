# Buscador de Raíces con Métodos de Bisección y Regla Falsa

Este programa en Python permite encontrar la raíz de una función utilizando dos métodos numéricos: **Bisección** y **Regla Falsa (Falsa Posición)**.

## ¿Qué hace el programa?

1. **Entrada de Datos:**
   - **Función:**  
     El usuario ingresa una función en términos de \( x \) utilizando la notación `^` para los exponentes (por ejemplo, `x^3-x-1`). El programa reemplaza internamente `^` por `**` para que la función sea compatible con Python.
   - **Intervalo:**  
     Se solicita al usuario ingresar el intervalo \([a, b]\) en el cual se espera que exista una raíz, asegurándose de que \( a < b \).
   - **Tolerancia:**  
     Se define un valor de tolerancia para determinar la condición de convergencia de los métodos.

2. **Método de Bisección:**
   - El programa divide el intervalo \([a, b]\) en cada iteración calculando el punto medio.
   - Se evalúa la función en este punto y se determina en qué subintervalo continuar, según el cambio de signo de la función.
   - El proceso se repite hasta que el ancho del intervalo (o el valor absoluto de \( f(c) \)) es menor que la tolerancia especificada.
   - Se imprime la información de cada iteración (aproximación, error y \( f(c) \)).

3. **Método de Regla Falsa:**
   - Utiliza la fórmula de la regla falsa para aproximar la raíz:
     \[
     c = b - \frac{f(b) \times (a - b)}{f(a) - f(b)}
     \]
   - Se actualiza el intervalo en cada iteración basado en el signo de \( f(c) \).
   - Se calcula el error como la diferencia entre dos aproximaciones consecutivas.
   - Se imprime la información de cada iteración similar al método de bisección.

4. **Visualización:**
   - Tras calcular las aproximaciones, el programa grafica la función sobre un rango extendido.
   - Se superponen los puntos obtenidos en cada iteración de la **Bisección** (en rojo) y de la **Regla Falsa** (en azul), permitiendo visualizar el proceso de convergencia de cada método.
