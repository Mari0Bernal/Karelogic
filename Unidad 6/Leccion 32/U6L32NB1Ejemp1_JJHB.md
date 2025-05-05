Código del problema: U6L32NB1Ejemp1_JJHB

**Problema:**

El programa debera leer un entero N e imprimir "PAR" (sin comillas), si se trata de un número par o "IMPAR" (sin comillas), si se trata de un número impar.

**Consideraciones:**

- N es un entero positivo (valor numerico sin decimales).
- Utilizar el estatuto de asignacion (=) para asignar a una variable el valor correspondiente.
- Mostrar en la pantalla del usuario los datos solicitados.

A continuacion puedes ver el codigo del programa que deberas probar en el compilador Codeblocks. Toma en cuenta que lo que aparace despues de tres diagonales (///) son solo comentarios para explicar cada instrucción del programa y facilitar su comprensión.

Te pedimos compilar y luego probar el programa con diferentes datos en la plataforma de Codeblocks.

### Ejemplo:

**Entrada:**

7894

**Salida:**

PAR

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <bits/stdc++.h>
///Autor: Juan José Hernández Beltrán
using namespace std;

int main(){
	///Inicializamos las variables
	int n, aux;
	///Leemos n
	cin>>n;
	///Guardamos en aux el residuo de dividir n entre 2
	aux=n%2;
	///Dentro de los paréntesis del if ponemos la condicional que se evaluará
	///En este caso la condicional es "aux==0", es decir: "auxiliar es igual a cero"
	///Si esta condicional es verdadera se ejecutará lo que está dentro de las llaves del if
	if(aux==0){
		///Si el residuo es 0, entonces n es par, e imprimimos "PAR"
		cout<<"PAR";
	}
	///Si esta condicional es falsa se ejecutará lo que está dentro de las llaves del else
	else {
		///Si el residuo es 1, entonces n es impar, e imprimimos "IMPAR"
		cout<<"IMPAR";
	}
}.
```
