## Bienvenido al mundo magico de la recursividad

# Ejemplo-Ejercicio de recursividad (U6Lecc37EjempEjercc1_GRB)

C/C++ permite la recursividad. La recursividad consiste en que una funcion se puede llamar asi misma desde adentro de esa misma funcion. Cada vez que se llama a una función a si misma, se carga a la memoria RAM otra copia de esa funcion, la copia actual la deja pendiente de procesar (pero la computadora se va acordar a donde regresa a esa copia para teminar de procesarla) , y ademas se crea otro juego de variables locales, y las almacena en la pila de la computadora junto con el valor actual de todas sus variables locales y sus parametros. Si la función hace una llamada a si misma, se guardan sus variables y parámetros, usando la pila, y la nueva instancia o copia de la función trabajará con su propia copia de las variables locales. Cuando la computadora termina de procesar una ultima copia de la funcion, regresa a la copia anterior, y recupera las variables y los parámetros de la pila y continua la ejecución en el punto en que había sido llamada o invocada. Eso mismo hace con cada copia que fue quedando pendiente de terminar de procesar.

Por ejemplo:

Prodríamos crear una función recursiva para calcular el factorial de un número entero.

El factorial se simboliza como n!, se lee como "n factorial", y la definición es:

n! = \* x (n-1) \* (n-2) \* ... \* 1

Hay algunas limitaciones:

- No es posible calcular el factorial de números negativos, no está definido.
- El factorial de cero es 1.

De modo que una función recursiva debería incluir un control para esos casos especiales, si fuera el caso:

```
/* Función recursiva para calcular el factorial de un numero entero */
int factorial(int n) {
   if(n < 0) return 0;
   else if(n > 1) return n*factorial(n-1); /* Recursividad */
                  //Se llama asi misma y quedara pendiente la operacion de multiplicar por "n"
                  //Y tambien quedaria pendiente la operacion de "return"
   return 1; /* Condición de terminación, cuando n == 1 */
//Esta instruccion de "return 1" se ejecutara en la ultima copia, donde la variable n ya es igual a 1
}
```

Lo anterior es un ejemplo. Ahora se te pide resolver el problema siguiente:

Se te pide ingresar al siguiente enlace sobre el tema de crear y recorrer un arbol binario de busqueda.

[Crear y recorrer un arbol binario de busqueda con apuntadores](https://eduarmandov.wordpress.com/wp-content/uploads/2017/05/datastructures-arboles-binarios-de-bc3basqueda-en-c-alumnos.pdf)

En el enlace anterior esta la explicacion correspondiente a este tema, tambien se encuentra todo el codigo en C/C++ que deberan probar en la solucion de este ejercicio, para crear y mostrar la secuencia de los nodos del arbol binario, generando los recorridos "Inorder", "Preorder" y "Posorder".

Solo que al ingresar en esta plataforma, el programa del enlace anterior no van a incluir los mensajes para solicitar datos al usuario, solamente las instrucciones de entrada para leer cada uno de los n datos numerico entero y para mostrar las secuencias correspondeintes de los tres recorridos del arbol binario.

**Ejemplo de entrada (primero leer el valor de n , y luego los n datos numericos enteros )**

10

100 200 150 80 40 300 180 20 240 60

**Salida:**

20 40 60 80 100 150 180 200 240 300

100 80 40 20 60 200 150 180 300 240

20 60 40 80 180 150 240 300 200 100

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
#include <iomanip>

using namespace std;

void imprimirSecuencia(int inicio, int fin, int paso){

    if(inicio == fin + paso){
        return;
    }

    cout << inicio << " ";

    imprimirSecuencia(inicio + paso, fin, paso);
}

int main(){

    int n;

    cin >> n;


    imprimirSecuencia(1, n, 1);
    cout << endl;

    imprimirSecuencia(n, 1, -1);
    return 0;
}
```
