# Ejercicio

### Objetivo

Los datos de entrada contienen un número entero objetivo y un arreglo ordenado de números enteros. Utiliza la búsqueda binaria para determinar si el objetivo existe dentro del arreglo o no. Los datos deberan estar siendo leidos, mientar se encuentre un dato mas a la entrada.

**Datos de entrada**

-1

-2 -1 0 4 7 9 11 13

**Datos de salida**

El elemento sí existe dentro del arreglo.

Se el dato no existe el mensaje debe ser el siguiente

"El elemento no existe dentro del arreglo" sin las comillas

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
#include <vector>

/**
 * Implementación de búsqueda binaria para validar la existencia de un elemento
 * objetivo.
 *
 * @param arr: Arreglo ordenado de menor a mayor donde se buscará el objetivo.
 * @param x:   Objetivo que se buscará.
 *
 * @return `true` si el objetivo está dentro del arreglo; `false` de lo contrario.
 */
bool binarySearch(std::vector<int> arr, int x) {
	// TODO
	int low = 0;
	int high = arr.size() - 1;

	while(low <= high){
	    int mid = low + (high - low)  / 2;

	    if(arr[mid] == x) return true;


		if(arr[mid] < x) {
			low = mid + 1;
		}else {
			high = mid - 1;
		}
	}

	return false;
}

int main() {
    int x = 0;
    int tmp = 0;
    std::vector<int> arr;

    std::cin >> x;
    while(std::cin >> tmp) {
        arr.push_back(tmp);
    }

  	if(binarySearch(arr,x)) {
		std::cout << "El elemento sí existe dentro del arreglo.";
	} else {
		std::cout << "El elemento no existe dentro del arreglo.";
	}

    return 0;
}
```
