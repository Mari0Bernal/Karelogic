# Año Bisiesto

**Problema:**

El programa debera leer un entero N y determinar si un año dado es bisiesto o no.

**Consideraciones:**

- El programa debe leer un año (entero positivo).
- Usar if-else para verificar si el año es bisiesto.
- Un año es bisiesto si es divisible por 4
- Imprimir "BISIESTO" si el año es bisiesto, de lo contrario imprimir "NO BISIESTO".

A continuacion puedes ver el codigo del programa que deberas probar en el compilador Codeblocks. Toma en cuenta que lo que aparace despues de tres diagonales (///) son solo comentarios para explicar cada instrucción del programa y facilitar su comprensión.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación o preguntale a tu profesor.

```
#include <bits/stdc++.h>	// Incluye todas las bibliotecas estándar de C++.

using namespace std;	// Usa el espacio de nombres std para evitar escribir std::.

int main() {

	int anno;	// Declara una variable entera llamada "anno".

	cin >> anno;	// Lee el valor de "anno" desde la entrada estándar.

	// Condición para verificar si el anno es bisiesto:

	// 2. Si es divisible por 4

	if (anno % 4 == 0)	{	//Verifica si el valor es modulo(lo restante de una división) de 4

		cout << "BISIESTO";	//Si es bisiesto, imprime "BISIESTO".

	} else {

		cout << "NO BISIESTO";	// Si no es bisiesto, imprime "NO BISIESTO".

	}

	return 0;	// Indica que el programa terminó correctamente.

}
```
