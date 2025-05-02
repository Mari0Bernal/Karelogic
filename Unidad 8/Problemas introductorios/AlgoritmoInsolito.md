# Algoritmo Insolito

Considera un algoritmo que recibe como entrada un entero positivo N. Si N es par, el algoritmo lo dividira entre 2; pero si es impar, multiplicara N por 3 y le sumara 1. El algoritmo continuara repitiendo este proceso hasta que N se vuelva 1.

Por ejemplo, si N = 3, entonces el proceso seria de la siguiente forma:

3 → 10 → 5 → 16 → 8 → 4 → 2 → 1

Tu tarea es simular la ejecucion del algoritmo para un valor dado de N.

### Entrada

Una sola linea que contiene el entero positivo N.

### Salida

Imprime una linea que contiene los valores de N durante la ejecucion del algoritmo.

**Restricciones**

1 ≤ N ≤ 10^6

**Ejemplo**

Entrada:

3

Salida:

3 10 5 16 8 4 2 1

**Explicacion**

Este problema es bastante trivial, la manera de simular el proceso descrito en el problema es usando un "while".

Dentro de la funcion "while", podemos preguntar si N es par o no usando la operacion "%", y cambiamos el valor de N de acuerdo a las reglas del algoritmo.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
///Codigo de Arturo Alejandro Arellano Cruz

#include<bits/stdc++.h>
using namespace std;

int main(){

 long long N; ///Valor de entrada
 cin>>N; ///Leemos el valor de entrada


 cout<<N<<" "; ///Imprimimos N, puesto que el problema tambien nos pide su valor inicial
 while(N!=1){ ///Mientras N sea distinto de 1, checamos la paridad de N

   if(N%2==0) ///Si N es par, lo dividimos entre 2
       N/=2;
   else ///De no ser asi, lo multiplicamos por 3 y le sumamos 1
       N = (N*3)+1;

   cout<<N<<" "; ///Imprimimos el nuevo valor de N
 }

}
```
