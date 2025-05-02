# Ejercicio

### Objetivo

Los datos de entrada contienen un número entero objetivo y un arreglo ordenado de mayor a menor de números enteros. Utiliza la búsqueda binaria para determinar el índice del objetivo dentro del arreglo.

**Datos de entrada**

-9

15 13 7 4 1 0 -4 -9 -20

**Datos de salida**

7

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
#include <vector>

/**
 * Implementación de búsqueda binaria para encontrar el índice de un elemento
 * objetivo.
 *
 * @param arr: Arreglo ordenado de mayor a menor donde se buscará el objetivo.
 * @param x:   Objetivo que se buscará.
 *
 * @return El índice del objetivo dentro del arreglo si se encontró; si no se
 *         encontró, -1.
 */
int binarySearch(std::vector<int> arr, int x) {
    //TODO
	int low = 0;
	int high = arr.size() - 1;

	while(low <= high){
	    int mid = low + (high - low)  / 2;

	    if(arr[mid] == x) return mid;


		if(arr[mid] > x) {
			low = mid + 1;
		}else {
			high = mid - 1;
		}
	}

	return -1;
}

int main() {
    int x = 0;
    int tmp = 0;
    std::vector<int> arr;

    std::cin >> x;
    while(std::cin >> tmp) {
        arr.push_back(tmp);
    }

    std::cout << binarySearch(arr, x);

    return 0;
}
```
