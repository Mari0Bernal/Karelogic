# Bienvenido a tu entrenamiento de C/C++

Código del problema: U6L34Ejemp4_GRB

Un arreglo de dos dimensiones o matriz es un conjunto de datos que son almacenados en forma de filas y columnas.

En la mayoria de los lenguajes de programacion, los datos de un arreglo de dos dimensiones son del mismo tipo de datos.

Cada elemento de una matriz tiene asignado un número de fila y un numero de columna, que estan numerados desde cero.

A continuacion esta declarado un arreglo de dos dimensiones de 5 filas, y cada fila de cuatro columnas

int matA[5] [4] ; ///El primer indice indica la cantidad de filas, y el segundo indicie indica la cantidad de columnas de cada fila.

Matriz de 5 filas, con 4 columnas cada fila

int matA[5][4] = { {1, 2, 3, 4}, {5, 6, 7, 8}, {9,10,11,12}, {13,14,15,16}, {17, 18, 19, 20} };

![matriz.png](matriz.png?raw=true)

**Datos de entrada:**

No hay datos de entrada

**Salida:**

1 2 3 4

5 6 7 8

9 10 11 12

13 14 15 16

17 18 19 20

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
using namespace std;
int main(){
   int matA[5][4] = { {1, 2, 3, 4}, {5, 6, 7, 8},{9,10,11,12}, {13,14,15,16},
                         {17, 18, 19, 20} };
    for(int i = 0 ; i < 5 ; i++){
        for(int j = 0 ; j < 4 ; j++){
            cout << matA[i][j]<<" ";
        }
        cout << endl;
    }
    return 0;
}
```
