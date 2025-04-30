Código del problema: U6L35Ejemp1_GRB

Un arreglo de dos dimensiones o matriz es un conjunto de datos que son almacenados en forma de filas y columnas. En la mayoria de los lenguajes de programacion, los datos de un arreglo de dos dimensiones son del mismo tipo de datos. Cada elemento de una matriz tiene asignado un número de fila y un numero de columna, que estan numerados desde cero.

Como un ejemplo ilustrativo, a continuacion esta declarado un arreglo de dos dimensiones de 5 filas, y cada fila de cuatro columnas:

int matA[5] [4] ; ///El primer indice indica la cantidad de filas, y el segundo indicie indica la cantidad de columnas de cada fila. Por lo que se trata de un arreglo de 5 filas por 4 columnas.

Matriz de 5 filas, con 4 columnas cada fila, a continuacion les asignamos valores iniciales, por fila

int matA[5][4] = { {1, 2, 3, 4}, {5, 6, 7, 8}, {9,10,11,12}, {13,14,15,16}, {17, 18, 19, 20} };

![img36.png](img36.png?raw=true)

Ahora se te pide probar y estudiar la solucion del siguiente problema de ejemplo de matrices (arreglos de dos dimensiones).

Leer dos valores m y n, el valor m representara la cantidad de filas y n la cantidad de columnas, de una matriz de datos enteros. Luego leer m\*n datos enteros para almacenarlos en un arreglo de dos dimensiones maximo de 100 X 100. Despues, de cada valor de la matriz, generar la sumatoria de 1+2+3+.......+mat[i][j]. Todos estos resultados deben estar siendo mostrados al usuario de n datos por linea.

**Datos de ejemplo de entrada:**

2 3

4 2 3

5 6 7

**Salida:**

10 3 6

15 21 28

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>

using namespace std;

int main(){
    int n,m, mat[100][100], sumatoria = 0;
    cin>>m>>n;
  //Primero leemos los m*n datos, para almacenarlos en la matriz
  //(arreglo de dos dimensiones)
    for(int i = 0 ; i < m ; i++){
        for(int j = 0 ; j < n ; j++){
            cin>>mat[i][j];
        }
    }
  //Vamos a recorrer o procesar la matriz de datos por fila
    for(int i = 0 ; i < m ; i++){
        for(int j = 0 ; j < n ; j++){
            sumatoria = 0;//Inicializamos a cero el acumulador
		    //antes de comenzar a generar la sumatoria del siguiente
		    //elemento del arreglo de dos dimensiones
		    //Con el siguiente for generamos la sumatoria de 1+2+3+...+mat[i][j]
            for(int k = 1 ; k <= mat[i][j] ; k++){
                sumatoria = sumatoria + k ;
            }
            cout<<sumatoria<<" ";
        }
        cout<<endl;//Salto de linea para que la siguiente fila de resultados
	    //se muestre en una nueva linea
    }
    return 0;
}
```
