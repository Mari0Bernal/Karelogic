# ESTO ES UN EJEMPLO DE COMO TRABAJAR CON UN ARREGLO DE DOS DIMENSIONES

Código del problema: U6L35Ejercc1_GRB

Un arreglo de dos dimensiones o matriz es un conjunto de datos que son almacenados en forma de filas y columnas. En la mayoria de los lenguajes de programacion, los datos de un arreglo de dos dimensiones son del mismo tipo de datos. Cada elemento de una matriz tiene asignado un número de fila y un numero de columna, que estan numerados desde cero.

Como un ejemplo ilustrativo, a continuacion esta declarado un arreglo de dos dimensiones de 5 filas, y cada fila de cuatro columnas:

int matA[5] [4] ; ///El primer indice indica la cantidad de filas, y el segundo indicie indica la cantidad de columnas de cada fila. Por lo que se trata de un arreglo de 5 filas por 4 columnas.

Matriz de 5 filas, con 4 columnas cada fila, a continuacion les asignamos valores iniciales, por fila

int matA[5][4] = { {1, 2, 3, 4}, {5, 6, 7, 8}, {9,10,11,12}, {13,14,15,16}, {17, 18, 19, 20} };

![L35E1.png](L35E1.png?raw=true)

Ahora se te pide resolver el siguiente problema de matrices.

Leer dos valores m y n, el valor m representara la cantidad de filas y n la cantidad de columnas, de una matriz de datos enteros. Luego leer m\*n datos enteros para almacenarlos en un arreglo de dos dimensiones maximo de 100 X 100. Despues intercambiar de lugar aquellos valores que sean posibles de los pares por los impares.

Y despues mostrar la nueva matriz de datos, de n valores en cada linea nueva

**Datos de ejemplo de entrada:**

5 4

1 2 3 4

5 6 7 8

9 10 11 12

13 14 15 16

17 18 19 20

**Salida:**

2 1 4 3

6 5 8 7

10 9 12 11

14 13 16 15

18 17 20 19

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
using namespace std;

int main() {
    // TODO poner codigo aqui
    int m, n;
    cin >> m >> n;
    int arr[100][100];
    for(int i = 0 ; i < m ; i++){
        for(int j = 0 ; j < n ; j++){
            cin >> arr[i][j];
        }
    }
    for(int i = 0 ; i < m ; i++){
        for(int j = 0 ; j < n - 1 ; j++){
            if(arr[i][j] % 2 == 0 && arr[i][j + 1] % 2 != 0){
                swap(arr[i][j], arr[i][j + 1]);
            }
            else if(arr[i][j] % 2 != 0 && arr[i][j + 1] % 2 == 0){
                swap(arr[i][j], arr[i][j + 1]);
            }
        }
    }
   for(int i = 0 ; i < m ; i++){
        for(int j = 0 ; j < n ; j++){
            cout << arr[i][j] << " ";
        }
        cout << endl;
    }
    return 0;

}
```
