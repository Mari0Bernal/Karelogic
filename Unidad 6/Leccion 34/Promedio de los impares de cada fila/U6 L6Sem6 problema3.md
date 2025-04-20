# Promedio de los impares de cada fila(U6 L6Sem6 problema3)

Código del problema: U6 L6Sem6 problema3

**Descripción del problema:**

Leer un valor "m" y un valor "n" maximo de 10k cada uno, "m representa la cantidad de filas y "n" la cantidad de columnas de un arreglo de dos dimensiones". luego leer los m\*n datos numericos enteros, almacenarlos en un arreglo de dos dimensiones de m filas por n columnas. Despues, obtener, de cada fila, el promedio de los valores almacenados en posiciones pares de cada fila , mostrar cada promedio en una nueva linea. Tambien mostrar al final (en una nueva linea) el acumulado de todos los promedios.

**Datos de entrada de ejemplo:**

3 4

2 2 2 2

10 20 10 20

5 10 5 10

**Datos de salida de ejemplo:**

2

10

5

17

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
#include <vector>
#include <iomanip>

using namespace std;
int main(){
	int n,m;
	// Calcular el promedio de las posiciones pares de cada fila
    int suma_promedios = 0;
	/// M son filas y n columnas
	cin >> m >> n;

	if (m > 10000 || n > 10000) {
        cout << "Los valores de m y n no deben exceder 10000." << endl;
        return 1;
    }

    int matriz[m][n];

    // Leer los m*n datos
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < n; j++) {
            cin >> matriz[i][j];
        }
    }

    for (int i = 0; i < m; i++) {
        int suma_pares = 0;
        int cantidad_pares = 0;
        for (int j = 0; j < n; j+=2) {
            suma_pares += matriz[i][j];
            cantidad_pares++;
        }
        int promedio = (cantidad_pares > 0) ? (int)suma_pares / cantidad_pares : 0;
        suma_promedios += promedio;

        // Mostrar el promedio de cada fila
        cout << promedio << endl;
    }

    // Mostrar la suma de todos los promedios
    cout << suma_promedios << endl;
  	return 0;
}
```
