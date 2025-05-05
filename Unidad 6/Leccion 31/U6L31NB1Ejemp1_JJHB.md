# Series Numéricas

Código del problema: U6L31NB1Ejemp1_JJHB

**Problema:**

El programa debera leer dos enteros N y M e imprimir los primeros M términos consecutivos de la serie numérica de N, inciando en N, uno en cada linea.

**Consideraciones:**

- N y M son enteros (valores numericos sin decimales).
- Utilizar el estatuto de asignacion (=) para asignar a una variable el valor correspondiente.
- Mostrar en la pantalla del usuario los datos solicitados.

A continuacion puedes ver el codigo del programa. Toma en cuenta que lo que aparace despues de tres diagonales (///) son solo comentarios para explicar cada instrucción del programa y facilitar su comprensión

Te pedimos compilar y luego probar el programa con diferentes datos en la plataforma de Codeblocks.

### Ejemplo:

**Entrada:**

3 5

**Salida:**

3

6

9

12

15

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <bits/stdc++.h>
///Autor: Juan José Hernández Beltrán
using namespace std;

int main(){
	///Definimos las variables a utilizar
	int n, m;
	///Leemos las dos variables
	cin>>n;
	cin>>m;
	///La función for repetirá un conjunto de instrucciones:
	///En el primer parámetro se incializan las variables locales del for
	///En el segundo parámetro se colocará la condición que debe cumplirse para que las instrucciones que están dentro del for se sigan repitiendo.
	///En el tercer parámetro se coloca la instrucción que se ejecutará al finalizar las instrucciones que están dentro del for en cada iteración.
	for(int i=1; i<=m; i++){
		///Imprimimos el (i_esimo)término i de la sucesión, que podemos generar
	    ///multiplicando n por el número del término, es decir: i.
		cout<<n*i<<endl;
		///Después de imprimir va a sumarle 1 a la variable i.
		///Esto se repetirá mientras i sea menor o igual que m, es decir: "i<=m".
	}
}
```
