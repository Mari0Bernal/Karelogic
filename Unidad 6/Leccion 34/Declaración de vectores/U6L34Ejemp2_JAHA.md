# Bienvenido a tu entrenamiento de C/C++

Código del problema: U6L34Ejemp2_JAHA

Un arreglo de una dimensión o vector es un conjunto de datos que son almacenados en
forma continua dentro de la memoria del programa. Todos los datos de un mismo
vector son del mismo tipo de dato

Cada elemento del vector tiene asignado un número de posición o de índice, y son
numerados comenzando desde cero [0] hasta el número [n-1]

![ejemplo.png](ejemplo.png?raw=true)

El número de “índice” o número de posición, en nuestro ejemplo de arriba del 0 al 4,
lo utilizamos para poder hacer referencia o acceder directamente al contenido de un
elemento específico del vector.

En el siguiente ejemplo se declarará un vector con sus valores y se imprimirán.

### Ejemplo:

**Entrada:**

No hay datos de entrada, es decir que el programa no va leer datos del usuario.

**Salida:**

1 2 3 4 5

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
using namespace std;

int main(){
	int arreglo[5] = {1, 2, 3, 4, 5};
  	for(int i = 0; i < 5; i++){
  		cout << arreglo[i] << " ";
	}
	return 0;
}
```
