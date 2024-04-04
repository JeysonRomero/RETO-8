# RETO-8

<br>
Desarrolle la mayoría de ejercicios en clase. Para cada punto cree un programa individual asimismo cree un notebook con la solución a todos los problemas. Al finalizar suba todo a un repo y subalo al canal reto_8 en slack, para ellos se dispondrá de un listado donde debe pegar el enlace al repo (misma dinámica que con el taller 1).
<br>

### Nota: Todo el código de aquí en adelante debe ir debidamente documentado.

<br>

### 1.Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.

<br>

```
for i in range(1, 101):
    print(f"{i}: {i**2}")

```
<br>
se hizo utilizando un bucle for para iterar a través de los números del 1 al 100 e imprimir cada número junto con su cuadrado

<br>

### 2.Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.

```
#  impares del 1 al 999
print("Números impares del 1 al 999:")
for i in range(1, 1000, 2):
    print(i)

# pares del 2 al 1000
print("\nNúmeros pares del 2 al 1000:")
for i in range(2, 1001, 2):
    print(i)
```
<br>

Se logro ya que el código utiliza dos bucles for para generar listas separadas de números impares y pares. Para los impares, se itera desde 1 hasta 999 con un paso de 2, imprimiendo cada número en el bucle. Para los pares, se itera desde 2 hasta 1000 con un paso de 2 y se imprime cada número. De esta manera, se logra imprimir listados separados de números impares y pares en los rangos especificados.
<br>


### 3.Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado.

<br>

```
n = int(input("Ingrese un número natural n >= 2: "))

if n < 2:
    print("El número ingresado no es válido.")
else:
    print("Números pares descendentes hasta 2:")
    for i in range(n, 1, -2):
        print(i)

```
<br>

 
El código comienza solicitando al usuario que ingrese un número natural 
n≥2. Luego, verifica si el número ingresado es válido. Si lo es, se utiliza un bucle for con un rango descendente desde 
n hasta 2 (exclusivo) con un paso de -2 para iterar a través de los números pares. Dentro del bucle, cada número par 
i se imprime en orden descendente hasta llegar a 2. Este enfoque asegura que solo se impriman los números pares dentro del rango especificado y en orden descendente. Si el número ingresado no es válido, se imprime un mensaje indicando que el número ingresado no es válido.
<br>

### 4.Imprimir los números de 1 hasta un número natural n dado, cada uno con su respectivo factorial.

<br>

```
def factorial(num):
    if num == 0:
        return 1
    else:
        return num * factorial(num - 1)

n = int(input("Ingrese un número natural n: "))

if n < 1:
    print("El número ingresado no es válido.")
else:
    print("Número - Factorial:")
    for i in range(1, n + 1):
        print(f"{i} - {factorial(i)}")


```

<br>
El código comienza definiendo una función factorial(num) que calcula el factorial de un número dado num, utilizando recursión para multiplicar el número actual por el factorial del número anterior hasta llegar a 0, donde devuelve 1. Luego, solicita al usuario que ingrese un número natural 
n, el cual es validado para asegurar que sea mayor o igual a 1. Si la entrada es válida, se imprime un encabezado indicando que se mostrarán los números del 1 hasta 
n junto con sus respectivos factoriales. Posteriormente, se utiliza un bucle for para iterar a través de los números del 1 hasta 
n, calculando y mostrando el factorial correspondiente de cada número utilizando la función factorial() previamente definida. De esta manera, el código genera un listado mostrando cada número natural del 1 hasta 
n con su respectivo factorial.

<br>

### 5.Calcular el valor de 2 elevado a la potencia n usando ciclos for.

<br>

```
n = int(input("Ingrese el valor de n: "))
resultado = 1

for i in range(n):
    resultado *= 2

print(f"El resultado de 2 elevado a la potencia {n} es: {resultado}")

```
<br>

Para calcular 
2 
n
  mediante un ciclo for en Python, primero solicitamos al usuario que ingrese el valor de 
n. Luego, inicializamos una variable llamada resultado a 1. A continuación, utilizamos un bucle for para multiplicar resultado por 2 
n veces. En cada iteración del bucle, multiplicamos resultado por 2. Finalmente, mostramos el resultado obtenido. De esta manera, logramos calcular eficientemente 
2 
n
  utilizando un ciclo for.
  
<br>

### 6.Leer un número natural n, leer otro dato de tipo real x y calcular x^n usando ciclos for. Disclaimer: Trate de no utilizar el operador de potencia (**).

<br>

```
n = int(input("Ingrese un número natural n: "))
x = float(input("Ingrese un número real x: "))

resultado = 1

for i in range(n):
    resultado *= x

print(f"{x} elevado a la potencia {n} es igual a: {resultado}")


```
<br>

En este código, primero leemos dos valores del usuario: el número natural 
n y el número real 
x. Luego, inicializamos la variable resultado a 1. Utilizamos un bucle for que itera 
n veces. En cada iteración, multiplicamos resultado por x. Después de que el bucle haya terminado, imprimimos el resultado. Este enfoque nos permite calcular 
x sobre n
sin utilizar el operador de potencia

<br>

### 7.Diseñe un programa que muestre las tablas de multiplicar del 1 al 9.

<br>

```
for tabla in range(1, 10):  # Bucle para las tablas del 1 al 9
    print(f"Tabla del {tabla}:")
    for multiplicador in range(1, 11):  # Bucle para los multiplicadores del 1 al 10
        producto = tabla * multiplicador
        print(f"{tabla} x {multiplicador} = {producto}")
    print()  # Línea en blanco entre cada tabla

```
<br>
se utilizo un bucle for para recorrer cada tabla, del 1 al 9. Dentro de este bucle exterior, se coloca otro bucle for que recorre los multiplicadores del 1 al 10, para generar las multiplicaciones correspondientes. Por cada iteración de los bucles anidados, se calcula el producto del número de la tabla actual y el multiplicador actual. Luego, se imprime esta multiplicación junto con los valores de la tabla y el multiplicador. Finalmente, se agrega una línea en blanco después de imprimir cada tabla para mejorar la legibilidad de la salida. Este proceso se repite para cada tabla de multiplicar del 1 al 9

<br>

### 8.Diseñar una función que permita calcular una aproximación de la función exponencial alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Maclaurin. Nota: use math para traer la función exponencial y mostrar la diferencia entre el valor real y la aproximación.
$$e^x \approx exp(x,n) \approx \sum_{i=0}^{n}\frac{x^i}{i!}$$
<br>

```
import math

def exp_aprox(x, n):
    approx = 0
    for i in range(n):
        approx += x ** i / math.factorial(i)
    return approx

x = float(input("Ingrese el valor de x: "))
n = int(input("Ingrese el número de términos (n): "))

real_value = math.exp(x)
approx_value = exp_aprox(x, n)

print(f"Valor real de e^{x}: {real_value}")
print(f"Aproximación con los primeros {n} términos: {approx_value}")
print(f"Diferencia: {abs(real_value - approx_value)}")

```
<br>

El código comienza importando el módulo math, que proporciona funciones matemáticas, incluida exp, para calcular la función exponencial. Luego, define una función llamada exp_aprox(x, n) que calcula una aproximación de la función exponencial alrededor de 0 utilizando los primeros n términos de la serie de Maclaurin. Esta función itera a través de los términos de la serie y los suma para obtener la aproximación. Después, solicita al usuario que ingrese el valor de x para el cual quiere aproximar la función exponencial y el número de términos n que desea utilizar en la aproximación. Utilizando estos valores, calcula el valor real de 
e sobre x utilizando la función exp del módulo math, y la aproximación utilizando la función exp_aprox. Finalmente, imprime el valor real, la aproximación y la diferencia absoluta entre ellos para evaluar la precisión de la aproximación. Este enfoque permite calcular y comparar fácilmente el valor real de 
e sobre x con su aproximación basada en la serie de Maclaurin.
<br>

### 9.Diseñar una función que permita calcular una aproximación de la función seno alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Maclaurin. Nota: use math para traer la función seno y mostrar la diferencia entre el valor real y la aproximación.
$$sin(x) \approx sin(x,n) \approx \sum_{i=0}^{n} (-1)^i \frac{x^{2i+1}}{(2i+1)!}$$
<br>

```
import math

def sin_aprox(x, n):
    approx = 0
    for i in range(n):
        coeficiente = (-1) ** i
        numerador = x ** (2 * i + 1)
        denominador = math.factorial(2 * i + 1)
        term = coeficiente * numerador / denominador
        approx += term
    return approx

x = float(input("Ingrese el valor de x: "))
n = int(input("Ingrese el número de términos (n): "))

real_value = math.sin(x)
approx_value = sin_aprox(x, n)

print(f"Valor real de sin({x}): {real_value}")
print(f"Aproximación con los primeros {n} términos: {approx_value}")
print(f"Diferencia: {abs(real_value - approx_value)}")

```
<br>
El código comienza importando el módulo math para usar la función seno. Luego, define una función sin_aprox(x, n) que calcula una aproximación del seno alrededor de 0 utilizando los primeros n términos de la serie de Maclaurin. Solicita al usuario que ingrese el valor de x y el número de términos n. Calcula el valor real del seno utilizando la función math.sin(x) y luego llama a sin_aprox(x, n) para obtener la aproximación. Finalmente, muestra el valor real del seno, la aproximación y la diferencia entre ellos. Esto permite comparar la aproximación con el valor real del seno y evaluar su precisión.

<br>

### 10.Diseñar una función que permita calcular una aproximación de la función arcotangente alrededor de 0 para cualquier valor x en el rango [-1, 1], utilizando los primeros n términos de la serie de Maclaurin. Nota: use math para traer la función arctan y mostrar la diferencia entre el valor real y la aproximación.
$$arctan(x) \approx arctan(x,n) \approx \sum_{i=0}^{n} (-1)^i \frac{x^{2i+1}}{(2i+1)}$$
<br>

**Disclaimer:** Para las aproximaciones de series determine con que valor n se obtiene menos del 0.1% de error.

<br>

```
import math

def arctan_aprox(x, n):
    approx = 0
    for i in range(n):
        coeficiente = (-1) ** i
        numerador = x ** (2 * i + 1)
        denominador = 2 * i + 1
        term = coeficiente * numerador / denominador
        approx += term
    return approx

x = float(input("Ingrese el valor de x en el rango [-1, 1]: "))
if abs(x) > 1:
    print("El valor de x debe estar en el rango [-1, 1].")
else:
    n = int(input("Ingrese el número de términos (n): "))

    real_value = math.atan(x)
    approx_value = arctan_aprox(x, n)

    print(f"Valor real de arctan({x}): {real_value}")
    print(f"Aproximación con los primeros {n} términos: {approx_value}")
    print(f"Diferencia: {abs(real_value - approx_value)}")

```
<br>

El código comienza importando el módulo math, que contiene la función atan para calcular la arcotangente de un valor. Luego, se define una función llamada arctan_aprox(x, n) que calcula una aproximación de la arcotangente alrededor de 0 para un valor 
x en el rango [-1, 1], utilizando los primeros 
n términos de la serie de Maclaurin. Esta función itera a través de los términos de la serie, calculando cada término y sumándolos para obtener la aproximación. Se solicita al usuario que ingrese el valor de 
x en el rango [-1, 1] y el número de términos 
n que desea utilizar en la aproximación. Luego, se calcula el valor real de 
arctan(x) utilizando la función math.atan(x) y se llama a arctan_aprox(x, n) para obtener la aproximación. Finalmente, se imprime el valor real de la arcotangente, la aproximación y la diferencia absoluta entre ellos, permitiendo evaluar la precisión de la aproximación.


<br>













