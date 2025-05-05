# C/C++, ejemplo básico #5(KO), U6L30NB1Ejemp5_RNC

## Descripcion

Escribe un programa que lea la edad de cada una de dos personas, las convierta a meses y luego calcule la suma de esas edades en meses.

### Ejemplo:

**Entrada:**

10 20

**Salida:**

360

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
    cout << (edad1 + edad2) * 12 << endl;
    return 0;
}
//Observa como el par de parentesis, con la suma dentro de los parentesis,
//le indica a la computadora que primero debe llevar a cabo la suma
//y despues de la suma, el resultado de la suma la debera mutiplicar por el valor 12
//Una vez realizado lo anterior, la computadora, procede a mostar al usuario
//el resultado de las operaciones realizadas.
//Tambien debemos saber, que el usuario de nuestros programas es la persona que va a ver,
//en la ventana de "Salida", los resultados que envia tu programa (con cada instruccion
//"cout<<").
```
