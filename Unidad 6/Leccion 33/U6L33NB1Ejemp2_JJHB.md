Código del problema: U6L33NB1Ejemp2_JJHB

**Problema:**

El programa debera leer dos enteros A y B, e imprimir su máximo común divisor.

**Consideraciones:**

- A y B son enteros (valor numerico sin decimales).
- Utilizar el estatuto de asignacion (=) para asignar a una variable el valor correspondiente.
- Mostrar en la pantalla del usuario los datos solicitados.

A continuacion puedes ver el codigo del programa que deberas probar en el compilador Codeblocks. Toma en cuenta que lo que aparace despues de tres diagonales (///) son solo comentarios para explicar cada instrucción del programa y facilitar su comprensión.

Te pedimos compilar y luego probar el programa con diferentes datos en la plataforma de Codeblocks.

### Ejemplo:

**Entrada:**

98 56

**Salida:**

14

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <bits/stdc++.h>
///Autor: Juan José Hernández Beltrán
using namespace std;

int main(){
	///PARA ENCONTRAR EL MCD UTILIZAREMOS EL "ALGORITMO DE EUCLIDES"
	///Inicializamos las variables:
	int a, b, ans;
	cin>>a;
	cin>>b;
	//Mientras A sea diferente de B.
	while(a!=b){
		//Restará el más pequeño al más grande tanto como sea posible.
	    if(a>b){
	    	a=a-b;
	    }
	    else{
	    	b=b-a;
	    }
	}
	//La respuesta queda guardada en A y por orden, la pasamos a ans, e imprimimos este valor.
	ans=a;
	cout<<ans;

	///EXPLICACIÓN DEL ALGORITMO:
	///Dados dos segmentos AB y CD (con AB>CD), restamos CD de AB tantas veces como sea posible. Si no hay residuo, entonces CD es la máxima medida común.
	///Si se obtiene un residuo EA, este es menor que CD y podemos repetir el proceso: restamos EA tantas veces como sea posible de CD. Si al final no queda un residuo, EA es la medida común. En caso contrario obtenemos un nuevo residuo FC menor a EA.
	///El proceso se repite hasta que en algún momento no se obtiene residuo. Entonces el último residuo obtenido es la mayor medida común.
}
```
