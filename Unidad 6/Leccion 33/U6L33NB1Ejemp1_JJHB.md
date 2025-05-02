Código del problema: U6L33NB1Ejemp1_JJHB

**Problema:**

El programa debera leer un entero N de 4 cifras e imprimir el dígito en sus millares, centenas, decenas y unidades en ese orden y en lineas separadas.

**Consideraciones:**

- N es un entero de 4 cirfras (valor numerico sin decimales).
- Utilizar el estatuto de asignacion (=) para asignar a una variable el valor correspondiente.
- Mostrar en la pantalla del usuario los datos solicitados.

A continuacion puedes ver el codigo del programa que deberas probar en el compilador Codeblocks. Toma en cuenta que lo que aparace despues de tres diagonales (///) son solo comentarios para explicar cada instrucción del programa y facilitar su comprensión.

Te pedimos compilar y luego probar el programa con diferentes datos en la plataforma de Codeblocks.

### Ejemplo:

**Entrada:**

3412

**Salida:**

3

4

1

2

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <bits/stdc++.h>
///Autor: Juan José Hernández Beltrán
using namespace std;

int main(){
	///Definimos los enteros que usaremos en el programa:
	///n para el número original, m para los millares, c para las centenas, d para las decenas, u para las unidades
	int n, m, c, d, u;
	///Leemos n
	cin>>n;
	///El operador '/' devuelve el cociente y el operador '%' (módulo) devuelve el residuo
	///Por ejemplo: 7%4 devuelve el residuo de dividir 7 entre 4, es decir, devuelve 3.
	m=n/1000;
	///Al dividir entre 1000 obtenemos el número sin los últimos 3 dígitos, solo los millares.
	n=n%1000;
	///Después aplicar módulo 1000 nos quedamos solo con los últimos tres dígitos.
	c=n/100;
	///Al dividir entre 100 obtenemos el número sin los últimos 2 dígitos, y como ya solo teníamos tres, nos queda el dígito de las centenas.
	n=n%100;
	///Con el módulo 100 nos quedamos solo con los últimos dos dígitos.
	d=n/10;
	///Al dividir entre 10 quitamos el último dígito, por lo que dejamos solo las decenas.
	n=n%10;
	///Al aplicar módulo 10 dejamos solo las unidades.
	u=n;
	///Igualamos u a las unidades.

	///Imprimimos m, c, d, u saltando linea entre cada uno; esto último se hace imprimiendo "\n"
	cout<<m<<"\n";
	cout<<c<<"\n";
	cout<<d<<"\n";
	cout<<u<<"\n";

	///NOTA: Se requiere que se use un entero para guardar n para que este algoritmo funcione, ya que, de lo contrario, no se eliminarían los últimos dígitos al dividir.
}
```
