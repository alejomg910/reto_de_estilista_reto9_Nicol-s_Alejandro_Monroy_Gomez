# reto_de_estilista_reto9_Nicol-s_Alejandro_Monroy_Gomez

Desarrolle la mayoría de ejercicios en clase. Para cada punto cree un programa individual. Al finalizar suba todo a un repo y subalo al canal reto_10 en slack.

1. Desarrollar un algoritmo que calcule el promedio de un arreglo de reales.

```python
def promedio_lista (arreglo: list): #Creamos una funcion para calcular el promedio de acuerdo a una cantidad ingresada
    suma = 0 #Iniciamos en cero la suma
    for n in arreglo: 
        suma += n #Actualiacion para cada numero del arreglo
    promedio = suma / len(arreglo) #Operacion para el promedio de acuerdo a la cantidad 
    return promedio

if __name__ == "__main__":
    cantidad = int(input("¿De cuantos numeros sera el promedio?: ")) #Ingreso de la cantidad de numeros a los que se le realizara el promedio
    arreglo = [] #Lista vacia para acumular los valores

    for i in range(cantidad): 
        numero = float(input("Ingresa el siguiente numero: ")) #Ingreso de los numeros por consola de acuerdo a los numeros a promediar
        arreglo.append(numero) #Se añade cada numero al final de la lista

total = promedio_lista(arreglo) #Se llma a la función
print("El promedio es de: " + str(total)) #Se imprime el resultado
```

2. Desarrollar un algoritmo que calcule el [producto punto](https://www.cuemath.com/algebra/dot-product/) de dos arreglos de números enteros (reales) de igual tamaño.

```python
def producto_punto (A: list, B: list): #Inicializamos una función para calcular el producto punto
    suma = 0 #Iniciamos su suma en cero
    for n in range(len(A)): #Bucle para cada numero en A
        suma += A[n] * B[n] #Operación para el cálculo del producto punto
    return suma

if __name__ == "__main__":
    cantidad = int(input("¿De cuantos numeros sera cada arreglo?: ")) #Ingresamos la longitud de los arreglos
    A = [] #Lista vacia 1
    B = [] #lista vacia 2

    for i in range(cantidad): #Rango para añadir los valores a A
        numeros_A = float(input("Ingresa el siguiente numero del primer arreglo: ")) #Ingreso de los numeros por consola
        A.append(numeros_A) #Añadimos al final del arreglo cada numero ingresado

    for i in range(cantidad): #Rango para añadir los valores a B
        numeros_B = float(input("Ingresa el siguiente numero del segundo arreglo: ")) #Ingreso de los numeros por consola
        B.append(numeros_B) #Añadimos al final del arreglo cada numero ingresado

resultado = producto_punto(A, B) #Llamamos a la función
print("EL producto punto entre los valores de A y B es de: " + str(resultado)) #Imprimimos el resultado
```

3. Hacer un algoritmo que deje al final de un arreglo de números todos los ceros que aparezcan en dicho arreglo.

```python
def ceros_final(lista1):
    indice_no_cero = 0 #Cuenta para el índice donde se va a colocar el siguiente número distinto a cero
    
    for i in range(len(lista1)): #Bucle para recorrer la lista en busca de los distintos a cero
        if lista1[i] != 0:
            lista1[indice_no_cero] = lista1[i] #El primero distinto a cero lo colocamos en la posicion de indice_no_cero
            indice_no_cero += 1 #Actualización para el siguiente numero

    for i in range(indice_no_cero, len(lista1)): #Completamos la lista con ceros
        lista1[i] = 0

    return lista1

if __name__ == "__main__":
    cantidad = int(input("¿De cuantos numeros sera el arreglo?: ")) #Ingreso de la cantidad de elementos de la lista
    A = [] #Lista donde se acumularan los datos
    
    for i in range(cantidad):  #Rango para añadir los valores a A
        numero_A = float(input("Ingresa el siguiente número del arreglo: "))  #Ingreso de los numeros por consola
        A.append(numero_A)  #Añadimos al final del arreglo cada número ingresado

    arreglo_resultado = ceros_final(A) # Llamamos a la función para mover los ceros al final
    
    print("El arreglo con los ceros al final es: " +str(arreglo_resultado)) #Imprimimos el resultado
```

4. Revisar que son los algoritmos de *sorting*, entender *bubble-sort* ([enlace](https://www.geeksforgeeks.org/bubble-sort/) a implementación).
