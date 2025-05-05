# Bienvenido a tu tutor de Programacion en C/C++

Codigo del ejemplo: U6L30NB1Ejemp4_GRB

## Ejemplo basico de lectura de datos y operaciones basicas:

El problema a resolver es:

El programa debera leer tres numeros enteros y calcular el doble producto de su suma.

**Consideraciones**

- Leer del teclado tres numeros enteros (valores numericos sin decimales)
- Utilizar el estatuto de asignacion (=) para asignar a una variable el resultado de calcular el doble producto de la suma de los tres numeros leidos.
- Mostrar en la pantalla del usuario el resultado.

A continuacion puedes ver el codigo del programa que deberas probar en el compilador de Codeblocks. Toma en cuenta que lo que aparace despues de tres diagonales son solo comentarios para que veas lo que significa cada instruccion del programa.

Te pedimos compilar y luego probar el programa con diferentes datos en la plataforma de Codeblocks.

Recuerda que el usuario de nuestro programa es la persona que ve,
en la ventana de "Salida", los resultados que envia tu programa solucion
(con cada instruccion "cout<<").

### Ejemplo:

**Entrada:**

10 20 30

**Salida:**

120

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
using namespace std;
///El objetivo de este ejemplo es mostrar al usuario como leer tres datos
///Y asignar a otra variable el doble producto de la suma de los tres numeros.
int main(){
/// Primero debemos declarar cada variable  que usaremos
  int dato1, dato2, dato3, resultado;///Declaramos cuatro variables de tipo entero
///son cuatro variables donde podemos almacenar
///un valor a la vez que sea numerico de tipo entero, es decir sin decimales
  cin>>dato1>>dato2>>dato3; ///el programa lee del teclado tres datos de entrada,
///y cada dato sera almacenado en variable diferente
  resultado = 2 * (dato1+dato2+dato3);///asignamos a "resultado" el resultado
///de la expresion aritmetica 2 * (dato1+dato2+dato3)
  cout<<resultado<<endl;///El programa muestra en la pantalla del usuario 
///el contenido de la variable "resultado"
  return 0;
}
//Recuerda que el usuario de nuestro programa es la persona que ve,
//en la ventana de "Salida", los resultados que envia tu programa solucion
//(con cada instruccion "cout<<").
```
