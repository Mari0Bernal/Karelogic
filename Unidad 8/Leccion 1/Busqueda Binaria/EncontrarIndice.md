# Ejemplo

### Descripcion del algoritmo

La búsqueda binaria es un algoritmo eficaz para encontrar un elemento objetivo dentro de un arreglo ordenado. Funciona dividiendo repetidamente el rango de búsqueda a la mitad hasta que se encuentre el objetivo o el rango esté vacío.

A diferencia de la búsqueda lineal, que se ejecuta en tiempo lineal O(n), la búsqueda binaria se ejecuta en tiempo logarítmico O(log n), por lo que es más efectivo y rápido para encontrar elementos dentro de arreglos grandes. Sin embargo, es necesario que el arreglo esté ordenado antes de aplicar la búsqueda binaria, algo que no es necesario para la búsqueda lineal.

Dado un arreglo ordenado de menor a mayor y un objetivo x por buscar:

1. Empezar por el elemento central del rango de búsqueda.
2. Si el elemento central coincide con el objetivo, devolver el índice.
3. Si el objetivo es más pequeño que el elemento central, ajustar el rango de búsqueda para buscar en la mitad izquierda.
4. Si el objetivo es más grande que el elemento central, ajustar el rango de búsqueda para buscar en la mitad derecha.
5. Repetir desde el inicio hasta encontrar el objetivo o hasta que el rango de búsqueda esté vacío.

**Objetivo**

Los datos de entrada contienen un número entero objetivo y un arreglo ordenado de menor a mayor de números enteros. Utiliza la búsqueda binaria para determinar el índice del objetivo dentro del arreglo.

**Datos de entrada**

9

-2 -1 0 3 4 4 9 11

**Datos de salida**

6

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
 * @param arr: Arreglo ordenado de menor a mayor donde se buscará el objetivo.
 * @param x:   Objetivo que se buscará.
 *
 * @return El índice del objetivo dentro del arreglo si se encontró; si no se
 *         encontró, -1.
 */
int binarySearch(std::vector<int> arr, int x) {
	// Rango de búsqueda inicial: [0, n - 1]
	int low = 0;
	int high = arr.size() - 1;

	while(low <= high) {
		// Elemento central del rango de búsqueda, formulado para prevenir
		// un desbordamiento aritmético (integer overflow)
		int mid = low + (high - low) / 2;

		// Se encontró el objetivo
		if(arr[mid] == x) return mid;

		// Nuevo rango de búsqueda: [mid + 1, high]
		if(arr[mid] < x) {
			low = mid + 1;
		}

		// Nuevo rango de búsqueda: [low, mid - 1]
		else {
			high = mid - 1;
		}
	}

	// No se encontró el objetivo
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
