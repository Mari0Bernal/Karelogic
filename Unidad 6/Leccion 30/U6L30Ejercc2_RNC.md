# C/C++, ejercicio básico, U6L30Ejercc2_RNC

## Descripcion del problema a resolver

Leer la edad de cada una de dos personas, convertir a meses cada edad (mostrar ambos resultados al usuario en la misma línea), y obtener el promedio en meses de las dos edades, mostrar ese nuevo resultado en una línea nueva.

Entrada:
Dos números enteros separados por un espacio, representando las edades de dos personas en años.

Salida:
En la primera línea, dos números enteros separados por un espacio, representando las edades en meses.

En la segunda línea, un número entero, que es el promedio de las edades en meses.

### Ejemplo:

**Entrada:**

30 40

**Salida:**

360 480

420

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.
> Te sugerimos probar cada ejemplo y cada ejercicio con diferentes datos de casos de prueba de entrada.
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>

using namespace std;

int main( ){

    int edad1, edad2, meses1, meses2, promedio;

    cin>>edad1>>edad2;

    meses1 = 12 * edad1;
    meses2 = 12 * edad2;

    promedio = (meses1+meses2)/2;
    cout<<meses1<<" "<< meses2<<endl;
    cout<<promedio<<endl;
     return 0;
}
//Recuerda que el usuario de nuestro programa es la persona que ve,
//en la ventana de "Salida", los resultados que envia tu programa solucion
//(con cada instruccion "cout<<").
```
