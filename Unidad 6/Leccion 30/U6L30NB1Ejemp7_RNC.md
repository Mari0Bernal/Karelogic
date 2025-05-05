# C/C++, ejemplo básico #7(KO), U6L30NB1Ejemp7_RNC

### Mayor Edad en Meses

## Descripcion

Escribe un programa que lea la edad de dos personas y muestre la mayor edad en meses.

### Ejemplo:

**Entrada:**

18 24

**Salida:**

288

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
    //Para tener el concepto bien claro de lo que es el estatuto de control
    //condicional "if" y temas relacionados, te pedimos estudiar las paginas
    //de la 37 a la 49, del libro de C/C++ del profesor Gilberto Reyes.
    //El libro lo puedes descargar del siguiente enlace
    // https://drive.google.com/file/d/1N5ahvk7Ekdl_ijsOGTIXZKKXfcKhtv5L/view
    if(edad1 > edad2){
	     cout<<edad1 * 12 ;
	}
    else{
         cout<<edad2 * 12;
    }
    // tambien se puede utilizar la funcion nativa
    //"max" para calcular el valor mayor de dos variables.
    //y entonces utilizar un solo "cout<<"
    //y sin necesidad de utiliar ei "if-else"
    //cout << max(edad1, edad2) * 12 << endl;

    return 0;
}
```
