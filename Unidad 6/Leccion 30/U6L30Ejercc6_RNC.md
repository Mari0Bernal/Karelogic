# C/C++,ejercicio básico, U6L30Ejercc6_RNC

### Edad en Días y en Semanas

## Descripcion

Escribe un programa que lea la edad en años de cada una de dos personas y las muestre en días y en semanas, en una misma linea.

### Ejemplo:

**Entrada:**

10 20

**Salida:**

3650 días, 520 semanas; 7300 días, 1040 semanas

Al enviar los resultados, deberan aparecer tal y como lo ves en la linea anterior

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
    cout << edad1 * 365 << " días, " << edad1 * 52 << " semanas; " << edad2 * 365 << " días, " << edad2 * 52 << " semanas";
    return 0;
}
```
