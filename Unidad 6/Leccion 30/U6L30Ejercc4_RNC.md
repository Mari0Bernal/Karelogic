# C/C++,ejercicio básico, U6L30Ejercc4_RNC

### Edad en Semanas

## Descripcion

Escribe un programa que lea la edad de dos personas y las convierta a semanas.

### Ejemplo:

**Entrada:**

10 20

**Salida:**

520 1040

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.
> Te sugerimos probar cada ejemplo y cada ejercicio con diferentes datos de casos de prueba de entrada.
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
using namespace std;

int main() {
   int edad1, edad2;
   cin >> edad1 >> edad2;
   cout << edad1 * 52 <<' '<< edad2 * 52;
    return 0;
}
```
