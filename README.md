# RETO-8

<br>
Desarrolle la mayoría de ejercicios en clase. Para cada punto cree un programa individual asimismo cree un notebook con la solución a todos los problemas. Al finalizar suba todo a un repo y subalo al canal reto_8 en slack, para ellos se dispondrá de un listado donde debe pegar el enlace al repo (misma dinámica que con el taller 1).
<br>

### Nota: Todo el código de aquí en adelante debe ir debidamente documentado.
<br>

### 1.Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.

<br>

```

```
<br>

<br>

### 2.

```

```



<br>


### 3.

<br>

```

```
<br>

 
<br>

### 4.

<br>

```

```

<br>


<br>

### 5.

<br>

```

```
<br>



<br>

### 6.

<br>

```


```
<br>



<br>

### 7.
<br>

```

```
<br>


<br>

### 8.
<br>

```
def es_primo(numero):
    if numero <= 1:
        return False
    for i in range(2, int(numero ** 0.5) + 1):
        if numero % i == 0:
            return False
    return True

def numeros_primos_hasta_100():
    print("Números primos del 1 al 100:")
    for i in range(1, 101):
        if es_primo(i):
            print(i, end=" ")

numeros_primos_hasta_100()

```

<br>

Este código consta de dos funciones:

1. La función es_primo(numero) verifica si un número dado es primo. Comienza verificando si el número es menor o igual a 1, en cuyo caso no es primo. Luego, itera desde 2 hasta la raíz cuadrada del número, verificando si el número es divisible por algún número en ese rango. Si es divisible por algún número, no es primo. Si no es divisible por ninguno, es primo.

2. La función numeros_primos_hasta_100() imprime todos los números primos del 1 al 100 utilizando la función es_primo(numero).

El resultado será la impresión de todos los números primos del 1 al 100.

 COMO SE HIZO

-  Función para verificar si un número es primo (es_primo(numero)): Esta función determina si un número dado es primo o no. Itera sobre los números desde 2 hasta la raíz cuadrada del número y verifica si es divisible por alguno de ellos. Si no es divisible por ninguno, es primo.

- Función para encontrar los números primos del 1 al 100 (numeros_primos_hasta_100()): Utiliza la función anterior para imprimir todos los números primos del 1 al 100.

- Llamada a la función principal: Se llama a la función principal para ejecutar el programa y mostrar los números primos del 1 al 100.












