Código del problema: U6L32NB1Ejemp2_JJHB

**Problema:**

El programa deberá leer dos cadenas de caracteres e imprimir "ACEPTADA" (sin comillas) en caso de ser iguales o "NO ACEPTADA" (sin comillas) si no lo son.

**Consideraciones:**

- Las cadenas de caracteres no contienen espacios.
- Utiliza (==) para comparar el valor de dos variables.
- Mostrar en la pantalla del usuario los datos solicitados.

A continuacion puedes ver el codigo del programa que deberas probar en el compilador Codeblocks. Toma en cuenta que lo que aparace despues de tres diagonales (///) son solo comentarios para explicar cada instrucción del programa y facilitar su comprensión.

Te pedimos compilar y luego probar el programa con diferentes datos en la plataforma de Codeblocks.

### Ejemplo:

**Entrada:**

holaMundo

holAmundo

**Salida:**

NO ACEPTADA

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación o preguntale a tu profesor.

```
#include <bits/stdc++.h>
///Autor: Juan José Hernández Beltrán
using namespace std;

int main(){
	///Inicializamos las variables
	string a, b;
	///Leemos la contraseña
	cin>>a;
	///leemos la confirmación de la contraseña
	cin>>b;
	///Dentro de los paréntesis del if ponemos la condicional que se evaluará
	///En este caso la condicional es "a==b", es decir: "la cadena a es igual a la cadena b"
	///Si esta condicional es verdadera se ejecutará lo que está dentro de las llaves del if
	if(a==b){
		///Si son iguales imprimimos "ACEPTADA"
		cout<<"ACEPTADA";
	}
	///Si esta condicional es falsa se ejecutará lo que está dentro de las llaves del else
	else {
		///Si NO son iguales imprimimos "NO ACEPTADA"
		cout<<"NO ACEPTADA";
	}
}
```
