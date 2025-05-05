# Bienvenido a tu tutor de Programacion en C/C++

Codigo del ejemplo: U6L16NB1Ejemp3_GRB

**Veremos un ejemplo donde:**

- Declaramos dos variables de tipo entero (int edadAnios, edadMeses)
- El programa va a leer un dato que sera ingresado desde el teclado, y que sera almacenado en la variable que escribamos a la derecha de la instruccion "cin>>" (cin>>edadAnios;)
- Asignamos a otra variable el resultado de una expresion aritmetica (edadMeses = edadAnios \* 12;)
- Mostramos el contenido de la variable "edadMeses" (cout<< edadMeses)

**Descripcion del problema ejemplo:**

El objetivo de este programa de ejemplo es calcular la edad en meses, a partir de una variable en donde esta el valor de una edad en años. Mostrar el resultado de la edad en meses.

Recuerda que el usuario de nuestro programa es la persona que ve,
en la ventana de "Salida", los resultados que envia tu programa solucion
(con cada instruccion "cout<<").

### Ejemplo:

**Entrada:**

10

**Salida:**

120

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
using namespace std;
///El objetivo de este programa de ejemplo es mostrar al usuario el contenido de
///una variable "edadMeses" en donde se asigno el resultado de una expresion aritmetica.
int main(){
    /// Primero debemos declarar cada variable  que usaremos
	int edadAnios, edadMeses;///Declaramos dos variables de tipo entero
                             ///son dos variables donde podemos almacenar
                             ///un valor a la vez que sea numerico
                             ///de tipo entero, es decir sin decimales
    cin>>edadAnios; ///el programa va a leer un dato de entrada, que sera ingresado desde
                    ///el teclado, y sera almacenado en la variable "edadAnios"
	edadMeses = edadAnios * 12;///asignamos a la variable edadMeses el resultado
                               ///de la expresion aritmetica "edadAnios * 12"
    cout<<edadMeses<<endl;///El programa muestra en la pantalla del usuario
                          ///el contenido de la variable "edadMeses"
    return 0;
}
//Recuerda que el usuario de nuestro programa es la persona que ve,
//en la ventana de "Salida", los resultados que envia tu programa solucion
//(con cada instruccion "cout<<").
```
