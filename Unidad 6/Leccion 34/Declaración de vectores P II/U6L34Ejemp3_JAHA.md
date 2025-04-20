# Bienvenido a tu entrenamiento de C/C++

Código del problema: U6L34Ejemp3_JAHA

UAl momento de crear un vector le podemos asignar valores iniciales, que
después, dentro del programa, podemos cambiar uno o más de esos valores,
dependiendo de lo que estemos resolviendo con nuestro programa(Cómo en el ejemplo anterior)

Otra opción de asignarle valores a un vector es que el usuario del programa
este ingresando cada uno de los datos o valores que estaremos almacenando en
cada una de las localidades o posiciones de un vector.

### Ejemplo:

Se monstrará un programa para la asignacion de valores a un vector por el usuario, luego se sumarán y se imprimirá el resultado de esta suma.

**Entrada:**

2 4 6 8 10

**Salida:**

30

**Explicacion**

Conforme el usuario ingresa los valores al vector, estos estan siendo almacenados en el vector de datos.

Despues con otro estatuto de control de repeticion "for", el programa estara sumando cada valor del vecto, para finalmente mostrar al usuario el resultado de la suma.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
using namespace std;

int main(){
	int vector[5], suma = 0;
///las posiciones del vector estan numeradas de la 0 al 4
  	for(int i = 0; i < 5; i++){
	 	cin >> vector[i];
	}
    for(int i = 0; i < 5; i++){
		suma = suma + vector[i];
	}
  	cout << suma;
  	return 0;
}
```
