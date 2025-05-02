# Ejemplo

### Descripcion del algoritmo

La búsqueda lineal es un algoritmo simple para encontrar un elemento objetivo dentro de un arreglo. Funciona verificando cada uno de los elementos dentro del arreglo hasta que se encuentre el objetivo o se llegue al final del arreglo.

La búsqueda lineal es fácil de implementar, funciona con arreglos no ordenados y puede llegar a ser eficaz para arreglos pequeños.

Dado un arreglo cualquiera y un objetivo x por buscar:

- Empezar por el primer elemento del arreglo y comparar cada elemento con el objetivo.
- Si el elemento coincide con el objetivo, devolver el índice.
- Si el elemento no coincide con el objetivo, intentar con el siguiente elemento.
- Si se llega al final del arreglo sin haber encontrado ninguna coincidencia, devolver -1.

**Objetivo**

Los datos de entrada contienen un número entero objetivo y un arreglo de números enteros. Utiliza la búsqueda lineal para determinar el índice del objetivo dentro del arreglo.

**Datos de entrada**

-1

4 -2 9 11 13 -1 7 0

**Datos de salida**

5

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
#include <vector>

/**
 * Implementación de búsqueda lineal para encontrar el índice de un elemento
 * objetivo.
 *
 * @param arr: Arreglo donde se buscará el objetivo.
 * @param x:   Objetivo que se buscará.
 *
 * @return El índice del objetivo dentro del arreglo si se encontró; si no se
 *         encontró, -1.
 */
int linearSearch(std::vector<int> arr, int x) {
	// Iterar sobre cada elemento del arreglo hasta encontrar el objetivo
	for(int i = 0; i < arr.size(); i++) {
		// Si se encontró, devolver el índice actual
		if(arr[i] == x) return i;
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

    std::cout << linearSearch(arr, x);

    return 0;
}
```
