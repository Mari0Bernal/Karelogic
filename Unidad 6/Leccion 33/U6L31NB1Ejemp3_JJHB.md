Código del problema: U6L31NB1Ejemp3_JJHB

**Problema:**

El programa debera leer dos enteros A y B, e imprimir su mínimo común múltiplo.

**Consideraciones:**

- A y B son enteros (valor numerico sin decimales).
- Utilizar el estatuto de asignacion (=) para asignar a una variable el valor correspondiente.
- Mostrar en la pantalla del usuario los datos solicitados.

A continuacion puedes ver el codigo del programa que deberas probar en el compilador Codeblocks. Toma en cuenta que lo que aparace despues de tres diagonales (///) son solo comentarios para explicar cada instrucción del programa y facilitar su comprensión.

Te pedimos compilar y luego probar el programa con diferentes datos en la plataforma de Codeblocks.

### Ejemplo:

**Entrada:**

77 49

**Salida:**

539

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <bits/stdc++.h>
///Autor: Juan José Hernández Beltrán
using namespace std;

int main(){
	///PARA ENCONTRAR EL MCD UTILIZAREMOS EL "ALGORITMO DE EUCLIDES" Y EN BASE AL MDC ENCONTRAREMOS EL MCM.
	///Inicializamos las variables:
	int a, b, ans, MCD, A, B;
	cin>>a;
	cin>>b;
	///Guardamos una copia de los números originales.
	A=a;
	B=b;
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
	///El mínimo común divisor queda guardado en A y, por orden, la pasamos a MCD.
	MCD=a;
	///Multiplicamos A y B y dividimos entre el MCD para obtener el MCM.
	ans=(A/MCD)*B;
	///lo hacemos en este orden para evitar sobrepasar la capacidad de un int.
	cout<<ans;

	///EXPLICACIÓN DEL ALGORITMO:
	///Dados dos segmentos AB y CD (con AB>CD), restamos CD de AB tantas veces como sea posible. Si no hay residuo, entonces CD es la máxima medida común.
	///Si se obtiene un residuo EA, este es menor que CD y podemos repetir el proceso: restamos EA tantas veces como sea posible de CD. Si al final no queda un residuo, EA es la medida común. En caso contrario obtenemos un nuevo residuo FC menor a EA.
	///El proceso se repite hasta que en algún momento no se obtiene residuo. Entonces el último residuo obtenido es la mayor medida común.
	///Para obtener el mínimo común múltiplo debemos multiplicar ambos números, pero eliminar los factores primos que estén en ambos, es decir, el Mínimo Común Divisor, por lo que dividimos el producto de A y B entre este.
}
```
