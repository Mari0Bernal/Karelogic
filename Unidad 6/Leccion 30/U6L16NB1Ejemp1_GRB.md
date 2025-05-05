# Bienvenido a tu tutor de Programacion en C/C++

Codigo del ejemplo: U6L16NB1Ejemp1_GRB

Veremos el primer ejemplo de un programa en C/C++, donde usaremos el estatuto de salida (cout<<"Mensaje para el usuario"<< endl <<;), para que el programa se comunique con el usuario y le envie comentarios.

**Descripcion del problema ejemplo:**

El objetivo del problema-ejemplo es mostrar el mensaje de "Hola, bienvenido este tu programa"

### Ejemplo:

**Entrada:**

<< no hay datos de entrada >>

**Salida:**

Hola, bienvenido a este tu programa

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
/// Mi primer programa en C/C++
#include <iostream>
using namespace std;
int main(){
  cout << "Hola, bienvenido a este tu programa"<<endl;///el "endl" es para salto de linea
  ///Este mensaje sera el que le aparezca al usuario cuando ejecute este programa;
  return 0;
}
//Recuerda que el usuario de nuestros programas es la persona que va a ver, en la ventana de 
//"Salida", los resultados que envia nuestro programa (con cada instruccion "cout<<").
```
