# Tipo de triangulo

**Problema:**

El programa debe leer 3 valores, y determinar si puede formar un triangulo y su tipo

**Consideraciones:**

- El programa debe leer tres enteros positivos que representan los lados de un triángulo.
- Usar if-else para verificar si los valores ingresados pueden formar un triángulo:
  - Es un triángulo si la suma de dos lados siempre es mayor que el tercer lado.
  - Es equilátero si los tres lados son iguales.
  - Es isósceles si dos lados son iguales.
  - Es escaleno si los tres lados son diferentes.
  - Si no es un triángulo, imprimir "NO ES TRIANGULO".

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación o preguntale a tu profesor.

```
#include <bits/stdc++.h>	// Incluye todas las bibliotecas estándar de C++.

using namespace std;	// Usa el espacio de nombres std para evitar escribir std::.

int main() {

	int a, b, c;	// Declara tres variables enteras para los lados del triángulo.

	cin >> a >> b >> c;	// Lee los valores de los lados desde la entrada estándar.

	// Un triángulo es válido si la suma de dos lados es mayor que el tercer lado.

	if (a + b > c && a + c > b && b + c > a) {

	// Determina el tipo de triángulo.

	if (a == b && b == c) {

		cout << "EQUILATERO";	// Todos los lados son iguales.

		} else if (a == b || a == c || b == c) {

			cout << "ISOSCELES";	// Dos lados son iguales.

		} else {

			cout << "ESCALENO";	// Todos los lados son diferentes.

		}

	} else {

		cout << "NO ES TRIANGULO";	// Si no cumple la condición, no es un triángulo válido.

		}


		return 0;	// Indica que el programa terminó correctamente.

}
```
