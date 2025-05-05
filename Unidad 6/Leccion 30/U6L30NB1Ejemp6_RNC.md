# C/C++, ejemplo básico #6(KO), U6L30NB1Ejemp6_RNC

### Diferencia de Edades en Meses

## Descripcion

Escribe un programa que lea la edad de dos personas y muestre la diferencia de sus edades en meses.

Recuerda que el usuario de nuestro programa es la persona que ve,
en la ventana de "Salida", los resultados que envia tu programa solucion
(con cada instruccion "cout<<").

### Ejemplo:

**Entrada:**

18 12

**Salida:**

72

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.
> Te sugerimos probar cada ejemplo y cada ejercicio con diferentes datos de casos de prueba de entrada.
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
#include <cmath>
using namespace std;

int main() {
    int edad1, edad2;
    cin >> edad1 >> edad2;

    cout << abs((edad1 - edad2) * 12) << endl;
//La funcion nativa "abs(expresion)" calcula el valor absoluto del resultado
//de evaluar la expresion aritmetica que esta entre parentesis
    return 0;
}
//Recuerda que el usuario de nuestro programa es la persona que ve,
//en la ventana de "Salida", los resultados que envia tu programa solucion
//(con cada instruccion "cout<<").
```
