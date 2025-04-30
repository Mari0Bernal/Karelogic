Código del problema: U6L36Ejercc2_GRB

Un arreglo de dos dimensiones o matriz es un conjunto de datos que son almacenados en forma de filas y columnas. En la mayoria de los lenguajes de programacion, los datos de un arreglo de dos dimensiones son del mismo tipo de datos. Cada elemento de una matriz tiene asignado un número de fila y un numero de columna, que estan numerados desde cero.

Como un ejemplo ilustrativo, a continuacion esta declarado un arreglo de dos dimensiones de 5 filas, y cada fila de cuatro columnas:

int matA[5] [4] ; ///El primer indice indica la cantidad de filas, y el segundo indicie indica la cantidad de columnas de cada fila. Por lo que se trata de un arreglo de 5 filas por 4 columnas.

Matriz de 5 filas, con 4 columnas cada fila, a continuacion les asignamos valores iniciales, por fila

int matA[5][4] = { {1, 2, 3, 4}, {5, 6, 7, 8}, {9,10,11,12}, {13,14,15,16}, {17, 18, 19, 20} };

![img36.png](img36.png?raw=true)

Ahora se te pide resolver el siguiente problema de matrices (arreglos de dos dimensiones).

Leer dos valores m y n, el valor m representara la cantidad de filas y n la cantidad de columnas, de una matriz de datos enteros. Luego leer m\*n datos enteros para almacenarlos en un arreglo de dos dimensiones maximo de 100 X 100. Despues, obtener el promedio de todos los valores impares de la matriz, arreglo de dos dimensiones, redondeado al entero anterior.

**Datos de ejemplo de entrada:**

2 3

4 2 3

5 6 7

**Salida:**

5

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
#include <iomanip>

using namespace std;

int main(){
    int n,m;
    int promedioImpares = 0;
    int cantidadImpares = 0;
    /// M son filas y n columnas
	cin >> m >> n;
	if (m > 100 || n > 100) {
        cout << "Los valores de m y n no deben exceder 100." << endl;
        return 1;
    }

    ///Matriz
    int matriz[m][n];

    // Leer los m*n datos
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < n; j++) {
            cin >> matriz[i][j];
        }
    }

    for(int i=0; i < m; i++){
        for(int j=0; j < n; j++){
            if(matriz[i][j] % 2 == 1){
                promedioImpares+= matriz[i][j];
                cantidadImpares++;
            }
        }
    }

    if(cantidadImpares > 0){
        cout << promedioImpares/cantidadImpares << endl;
    } else {
        cout << "No hay Impares" << endl;
    }



    return 0;
}
```
