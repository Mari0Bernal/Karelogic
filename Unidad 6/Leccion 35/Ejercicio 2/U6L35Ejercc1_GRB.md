# ESTO ES UN EJEMPLO DE COMO TRABAJAR CON UN ARREGLO DE UNA DIMENSION

## Ejemplo, leer y trabajar con un vector

Código del problema: U6L35Ejercc1_GRB

Un arreglo de una dimensión o vector es un conjunto de datos que son almacenados en forma continua dentro de la memoria del programa. Todos los datos de un mismo vector son del mismo tipo de dato (int, char, float, string, .... , etc.).

![L35E2.png](L35E2.png?raw=true)

Cada elemento del vector tiene asignado un número de posición o de índice, y son numerados comenzando desde cero [0] hasta el número [n-1], la imagen que vemos arriba es un vector de 5 elementos, por lo tanto, sus elementos están numerados desde 0 hasta n-1, es decir, desde 0 hasta 4, eso significa que tendremos la posibilidad de almacenar y manipular cinco datos o valores, posiblemente diferentes. Un vector es una “variable” como cualquier otra, que declaramos de algún tipo de dato, con la particularidad de que en ella podemos almacenar un número “n” de valores, posiblemente diferentes, pero del mismo tipo de dato. El número de “índice” o número de posición, en nuestro ejemplo de arriba del 0 al 4, lo utilizamos para poder hacer referencia o acceder directamente al contenido de un elemento específico del vector.

**Descripcion del ejemplo:**

Leer un número entero n, despues leer n numeros y almacenarlos en un vector. Posteriormente, trabajar con el vector y mostrar cada uno de sus valores ya aumentado con el valor 2, mostrar los resultados en una misma linea cada uno separado por un espacio.

2 < n < 101

**Datos de entrada de ejemplo:**

7

10 20 30 40 50 60 70

**Datos de salida de ejemplo:**

12 22 32 42 52 62 72

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
using namespace std;

int main (){

    int n;
    cin >> n;
    if(n < 2 || n > 101){
        cout << "ERROR";
        return 1;
    }

    int arr[n];
    for(int i = 0; i < n; i++){
        cin >> arr[i];
        arr[i] = arr[i] + 2;
    }

    for(int i = 0; i < n; i++){
        cout << arr[i] << " ";
    }

	return 0;
}
```
