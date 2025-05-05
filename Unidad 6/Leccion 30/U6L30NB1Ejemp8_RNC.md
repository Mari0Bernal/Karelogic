# C/C++, ejemplo básico #8, U6L30NB1Ejemp8_RNC

### Promedio de Edad en Años y Meses, de dos personas

## Descripcion

Escribe un programa que calcule el promedio de la edad de dos personas, y que el resultado lo muestre en años y meses.

### Ejemplo:

**Entrada:**

10 20

**Salida:**

15 años y 0 meses

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

    int totalMeses = (edad1 + edad2) * 12 ;
    cout << totalMeses / 12 / 2 << " años y " << totalMeses % 12 << " meses" << endl;
    //En la linea anterior lo dividimos entre 2, porque nos piden el promedio de dos edades
    //El operador Modulo "%" regresa como resultado el residuo (es decir, lo que sobra)
    //de dividir dos valores numericos enteros, en este caso
    //es lo que sobra de dividir "totalMeses" entre el valor 12
    return 0;
}
```
