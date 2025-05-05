# Sumatoria

Código del problema: U6L31NB1Ejemp2_JJHB

**Problema:**

El programa debera leer dos enteros N y M e imprimir el resultado de la suma de los números enteros consecutivos desde N hasta M.

**Consideraciones:**

- N y M son enteros (valores numericos sin decimales).
- M es mayor o igual que N.
- Utilizar el estatuto de asignacion (=) para asignar a una variable el valor correspondiente.
- Mostrar en la pantalla del usuario los datos solicitados.

A continuacion puedes ver el codigo del programa. Toma en cuenta que lo que aparace despues de tres diagonales (///) son solo comentarios para explicar cada instrucción del programa y facilitar su comprensión

Te pedimos compilar y luego probar el programa con diferentes datos en la plataforma de Codeblocks.

### Ejemplo:

**Entrada:**

6 11

**Salida:**

51

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <bits/stdc++.h>
#include <iostream>
///Autor: Juan José Hernández Beltrán
using namespace std;

int main(){
	///Definimos las variables a utilizar
	int n, m, ans=0;
	///Leemos las dos variables
	cin>>n;
	cin>>m;
	///La función for repetirá un conjunto de instrucciones:
	///En el primer parámetro se incializan las variables locales del for
	///En el segundo parámetro se colocará la condición que debe cumplirse para que las instrucciones que están dentro del for se sigan repitiendo.
	///En el tercer parámetro se coloca la instrucción que se ejecutará al finalizar las instrucciones que están dentro del for en cada iteración.
	for(int i=n; i<=m; i++){
		////Este for se repetirá mientras la i sea menor o igual que m; i originalmente es igual que n, por lo que i tomará todos los valores enteros desde n hasta m, tal como pide el problema.
		ans = ans + i;
		///En cada iteración ans va a aumentar i, lo que equivale a
	    //sumar todos los números de n hasta m.
	}
	///Imprimimos la respuesta, que está guardada en ans.
	cout<<ans;
}
```
