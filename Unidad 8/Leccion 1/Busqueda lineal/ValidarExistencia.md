# Ejemplo

### Descripcion del algoritmo

Si lo que nos interesa es validar la existencia de un elemento dentro del arreglo, simplemente debemos devolver un valor booleano (verdadero o falso) en lugar del índice.

Dado un arreglo cualquiera y un objetivo x por buscar:

- Empezar por el primer elemento del arreglo y comparar cada elemento con el objetivo.
- Si el elemento coincide con el objetivo, devolver true.
- Si el elemento no coincide con el objetivo, intentar con el siguiente elemento.
- Si se llega al final del arreglo sin haber encontrado ninguna coincidencia, devolver false.

**Objetivo**

Los datos de entrada contienen un número entero objetivo y un arreglo de números enteros. Utiliza la búsqueda lineal para determinar si el objetivo existe dentro del arreglo o no.

**Datos de entrada**

-1

4 -2 9 11 13 -1 7 0

**Datos de salida**

El elemento sí existe dentro del arreglo.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
#include <vector>

/**
 * Implementación de búsqueda lineal para validar la existencia de un elemento
 * objetivo.
 *
 * @param arr: Arreglo donde se buscará el objetivo.
 * @param x:   Objetivo que se buscará.
 *
 * @return `true` si el objetivo está dentro del arreglo; `false` de lo contrario.
 */
bool linearSearch(std::vector<int> arr, int x) {
	// Iterar sobre cada elemento del arreglo hasta encontrar el objetivo
	for(int i = 0; i < arr.size(); i++) {
		// Si se encontró, devolver `true`
		if(arr[i] == x) return true;
	}

	// No se encontró el objetivo
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

  	if(linearSearch(arr,x)) {
		std::cout << "El elemento sí existe dentro del arreglo.";
	} else {
		std::cout << "El elemento no existe dentro del arreglo.";
	}

    return 0;
}
```
