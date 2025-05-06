## Bienvenido al mundo magico de la recursividad

# Ejemplo de recursividad simple (U6Lecc37Ejemp1_GRB)

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

Leer un numero entero n y mostrar los valores 1 2 3 ... n en una linea. En otra linea mostrar los valores

n n-1 n-2 n-3 ........... 2 1 ;

Ambas listas de resultados deben ser generados por la misma funcion recursiva

**Datos de ejemplo de entrada:**

9

**Salida:**

1 2 3 4 5 6 7 8 9

9 8 7 6 5 4 3 2 1

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <stdlib.h>
#include <iostream>
#include <iomanip>

using namespace std;

struct Nodo {
    int dato;
    struct Nodo* izquierda;
    struct Nodo* derecha;
};

struct Nodo* crearNodo(int valor) {
    struct Nodo* nuevoNodo = (struct Nodo*)malloc(sizeof(struct Nodo));
    if (nuevoNodo == NULL) {
        cout << "Error: No se pudo asignar memoria" << endl;
        exit(1);
    }
    nuevoNodo->dato = valor;
    nuevoNodo->izquierda = NULL;
    nuevoNodo->derecha = NULL;
    return nuevoNodo;
}

struct Nodo* insertar(struct Nodo* raiz, int valor) {
    // Si el árbol está vacío, crear el primer nodo
    if (raiz == NULL) {
        return crearNodo(valor);
    }

    // Si el valor es menor que el nodo actual, insertarlo en el subárbol izquierdo
    if (valor < raiz->dato) {
        raiz->izquierda = insertar(raiz->izquierda, valor);
    }
    // Si el valor es mayor que el nodo actual, insertarlo en el subárbol derecho
    else if (valor > raiz->dato) {
        raiz->derecha = insertar(raiz->derecha, valor);
    }
    // Si el valor ya existe, simplemente retornar la raíz (no permitimos duplicados)

    return raiz;
}

// Recorrido Inorder (Izquierda-Raiz-Derecha)
void inorder(struct Nodo* raiz) {
    if (raiz != NULL) {
        inorder(raiz->izquierda);  // Recorrer subárbol izquierdo
        cout << raiz -> dato << " "; // Visitar raíz
        inorder(raiz->derecha);     // Recorrer subárbol derecho
    }
}

// Recorrido Preorder (Raiz-Izquierda-Derecha)
void preorder(struct Nodo* raiz) {
    if (raiz != NULL) {
        cout << raiz -> dato << " "; // Visitar raíz
        preorder(raiz->izquierda);  // Recorrer subárbol izquierdo
        preorder(raiz->derecha);    // Recorrer subárbol derecho
    }
}

// Recorrido Postorder (Izquierda-Derecha-Raiz)
void postorder(struct Nodo* raiz) {
    if (raiz != NULL) {
        postorder(raiz->izquierda);  // Recorrer subárbol izquierdo
        postorder(raiz->derecha);    // Recorrer subárbol derecho
        cout << raiz -> dato << " "; // Visitar raíz
    }
}

// Función para liberar la memoria del árbol
void liberarArbol(struct Nodo* raiz) {
    if (raiz != NULL) {
        liberarArbol(raiz->izquierda);
        liberarArbol(raiz->derecha);
        free(raiz);
    }
}

int main() {
    struct Nodo* raiz = NULL;
    int n, valor;

    // Leer la cantidad de nodos
    cin >> n;

    // Leer los valores e insertarlos en el árbol
    for (int i = 0; i < n; i++) {
        cin >> valor;
        raiz = insertar(raiz, valor);
    }

    // Mostrar recorridos
    inorder(raiz);
    cout << endl;

    preorder(raiz);
    cout << endl;

    postorder(raiz);
    cout << endl;

    // Liberar memoria
    liberarArbol(raiz);

    return 0;
}
```
